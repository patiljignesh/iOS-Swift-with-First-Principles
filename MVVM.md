
## Design Pattern : MVVM 

MVVM (Model-View-ViewModel) is a design pattern used in software development for structuring the code in a way that separates the logic of the user interface from the business logic.

- Model: This represents the data and the business logic of your application. It’s where your data processing and network requests happen. The model is independent of the user interface.
- ViewModel: This layer acts as an intermediary between the Model and the View. It receives data from the Model, processes it (e.g., formatting), and prepares observable outputs that can be bound to the View. The ViewModel doesn’t directly reference the View.
-	View: This is the user interface of your application. In iOS, it’s typically composed of view controllers, views, and storyboards. The View observes the ViewModel and updates itself when the data changes.

```
import Foundation
import UIKit

// Model
struct User {
    let name: String
    let age: Int
}

// ViewModel
class UserViewModel {
    private var user: User

    var name: String {
        return user.name
    }

    var ageText: String {
        return "Age: \(user.age)"
    }

    init(user: User) {
        self.user = user
    }
}

// View (ViewController)
class UserViewController: UIViewController {
    var viewModel: UserViewModel!

    override func viewDidLoad() {
        super.viewDidLoad()
        // Assuming you have labels for name and age in your storyboard
        nameLabel.text = viewModel.name
        ageLabel.text = viewModel.ageText
    }
}
```

In this simple example:

- The User struct represents the Model.
-	UserViewModel prepares and formats the data for display.
-	UserViewController displays the data.

##  MVVM with Data binding using Combine framework

Here we are using MVVM with data binding in Swift, utilizing the Combine framework. This example will expand on the previous one, adding observable properties to the ViewModel and subscribing to these properties in the ViewController

```
import UIKit
import Combine

// Model
struct User {
    let name: String
    let age: Int
}

// ViewModel
class UserViewModel {
    private var user: User
    private var cancellables = Set<AnyCancellable>()

    // Published properties
    @Published var name: String = ""
    @Published var ageText: String = ""

    init(user: User) {
        self.user = user
        setupBindings()
    }

    private func setupBindings() {
        // Update name and ageText whenever the user's properties change
        $user.map { $0.name }
            .assign(to: \.name, on: self)
            .store(in: &cancellables)

        $user.map { "Age: \($0.age)" }
            .assign(to: \.ageText, on: self)
            .store(in: &cancellables)
    }
}

// View (ViewController)
class UserViewController: UIViewController {
    var viewModel: UserViewModel!
    private var cancellables = Set<AnyCancellable>()

    @IBOutlet weak var nameLabel: UILabel!
    @IBOutlet weak var ageLabel: UILabel!

    override func viewDidLoad() {
        super.viewDidLoad()
        bindViewModel()
    }

    private func bindViewModel() {
        viewModel.$name
            .receive(on: RunLoop.main)
            .sink { [weak self] name in
                self?.nameLabel.text = name
            }
            .store(in: &cancellables)

        viewModel.$ageText
            .receive(on: RunLoop.main)
            .sink { [weak self] ageText in
                self?.ageLabel.text = ageText
            }
            .store(in: &cancellables)
    }
}
```

In above example:

- The UserViewModel has @Published properties for the user’s name and age text. These properties are automatically updated whenever the user object changes.
- The UserViewController subscribes to these @Published properties and updates the UI accordingly.
- Both the ViewModel and ViewController use a Set<AnyCancellable> to store the subscriptions, which is crucial to prevent memory leaks.

This example demonstrates how you can use Combine for data binding in an MVVM architecture in Swift. The ViewModel exposes the data needed by the View in a way that can be observed, and the View binds to these observable properties to update the UI automatically when the data changes.

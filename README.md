# iOS Swift using First Principles

## Topics

###### Auto layout 
1. It's about setting rules for the UI elements
2. Size Classes
   - Size Classes are at the bottom where all the device at listed   
4. Orientation
5. Applying Constraints
6. Alignment
7. [SSL Pinning](https://github.com/SSL%2520Pinning.md)
8. Using Containers
9. StackViews
   - View embeded with other views

10. MVC - Design Pattern
    - Model: Logic & Data
      - Sends data to the Controller    
    - View: User Interface 
      - View send the input events to the Controller    
    - Controller: Mediator
      - Makes the request to the Model
      - Modifies the View    
    - View and Model will never talk to each other
    - View and Model will always use Controller to communicate with either one

11. Mutating Methods within Struct
    - Enable changes to the variable within the Struct when invoking 
    - "The problem is that when you create the struct Swift has no idea whether you will use it with constants or variables, so by default it takes the safe approach: Swift won’t let you write methods that change properties unless you specifically request it." ~ HackingWithSwift

12. Setting current Button Title via code:
`button.setTitle("my text here", forState: .normal)`

13. Rounding off a Float or other value:
`print(String(format: "%.2f", sender.value))`

14. Struct vs Classes
    - Structs are passed around by Value
    - Classes are passed around by Reference
    - Structs are immutable 
    - Classes have ingeritance 
    - Ref Reading: [https://docs.swift.org/swift-book/LanguageGuide/ClassesAndStructures.html] 

15. `CGRect` : Core Graphics Rectangle 

16. Adding to View by code/ Programatically:
```
// Inside viewDidLoad()
view.backgroundColor = .red        
let label = UILabel()
label.text = "Hello Second View controller"
label.frame = CGRect(x: 0, y: 0, width: 100, height: 50)
view.addSubview(label)
```
17. Downcasting
`let destinationVC = segue.destination as! ResultViewController`

18. String 
`let str = String(format: "%.2f", 1.2334)`
`RESULT: 1.23`

19. UIViewController Nagivation:
```
override func prepare(for segue: UIStoryboardSegue, sender: Any?) {
    if segue.identifier == "MySegueId" {
        if let nextViewController = segue.destination as? NextViewController {
                nextViewController.valueOfxyz = "XYZ" //Or pass any values
                nextViewController.valueOf123 = 123
        }
    }
}
```
20. Scalar Images vs Vector Images

![rastervsvector](https://user-images.githubusercontent.com/3880915/124241088-bad42f80-db1b-11eb-9bd8-4c55d4d0326b.png)

21. Dismiss the keyboard: `searchTextField.endEditing(true)`

22. Type Alias: 
- Example: Codable is a type alias for the Encodable and Decodable protocols. When you use Codable as a type or a generic constraint, it matches any type that conforms to both protocols.

23. Defining Extension
```
extension SomeType {
   // Add new functionality
   // It could extention to a class, struct, protocol
}

```

24. Create sections in the file:
` //MARK: - {Secion Name} `  

25. [Control flow](https://docs.swift.org/swift-book/LanguageGuide/ControlFlow.html)

26. Localized is referenced to local language that the user has selected. 
Eg. localizedDescription is a description which will be displayed in user's local device language which has been set by the user.

27. [weak self]
   - [Besher Al Maleh on [weak self]](https://medium.com/flawless-app-stories/you-dont-always-need-weak-self-a778bec505ef)
   - [Quora: what does [weak self] mean in a closure?](https://www.quora.com/What-does-weak-self-mean-in-a-Swift-Closure)
   - [weak self and unowned self explained by Antoine Van Der Lee](https://www.avanderlee.com/swift/weak-self/)
  
28. [Type Properties vs Instant Properties](https://docs.swift.org/swift-book/LanguageGuide/Properties.html#ID264)
- > There will only ever be one copy of these properties, no matter how many instances of that type you create. These kinds of properties are called type properties.

29. `is` is used for Type Checking

30. `as!` is used for Forced Downcast

31. `as?` is used for Safe Downcast 

32. `as` is used for Upcasting. From subclass to superclass.
 
33. [Understanding App Lifecyle](https://developer.apple.com/documentation/uikit/app_and_environment/managing_your_app_s_life_cycle)

34. Local Data Persistance using User Defaults, Core Data and Realm

35. [Core Data and more]()

36. Ternary Operator

```
value = condition ? valueIfTrue : valueIfFalse`

Example:

cell.accessoryType = item.done == true ? .checkmark : .none

```

37. Concurrency and Asynchronous Programming:
   - **Swift Concurrency:** With the introduction of async/await in Swift 5.5, handling asynchronous tasks has become more straightforward.
   - **Combine:** Apple's framework for handling asynchronous events with a declarative approach, which can be beneficial in networking scenarios

## DispatchQueue
- An object that manages the execution of tasks serially or concurrently on your app's main thread or on a background thread.

## Design Pattern: MVC
## UI Element Positioning

### Defining Structure

Snippet of Info:

```
1. IBOutlet - Interface Builder Outlet 
2. Who.What = Value
3. IBOutlet = Actions are from Code to Design
4. IBAction = Actions are from Design to Code 
5. Random Number = **Int.random(in: 0...5)** 
6. Random Element in an ``` Array = arrayVar.randomElement()
7. func myFunction(parameter: DataType) { ... } 
```

## Design Pattwr : MVVM 

MVVM (Model-View-ViewModel) is a design pattern used in software development for structuring the code in a way that separates the logic of the user interface from the business logic.

	1.	Model: This represents the data and the business logic of your application. It’s where your data processing and network requests happen. The model is independent of the user interface.
	2.	ViewModel: This layer acts as an intermediary between the Model and the View. It receives data from the Model, processes it (e.g., formatting), and prepares observable outputs that can be bound to the View. The ViewModel doesn’t directly reference the View.
	3.	View: This is the user interface of your application. In iOS, it’s typically composed of view controllers, views, and storyboards. The View observes the ViewModel and updates itself when the data changes.

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

	•	The User struct represents the Model.
	•	UserViewModel prepares and formats the data for display.
	•	UserViewController displays the data.




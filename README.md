# iOS-Swift-with-First-Principles

## Topics

###### Auto layout 
1. It's about setting rules for the UI elements
2. Size Classes
   - Size Classes are at the bottom where all the device at listed   
4. Orientation
5. Applying Constraints
6. Alignment
7. Pinning
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

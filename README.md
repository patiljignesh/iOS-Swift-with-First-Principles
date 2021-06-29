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
14. Structs are passed around by Value
15. Classes are passed around by Reference 

###### DispatchQueue
- An object that manages the execution of tasks serially or concurrently on your app's main thread or on a background thread.

###### Design Pattern: MVC
###### UI Element Positioning

###### Defining Structure

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

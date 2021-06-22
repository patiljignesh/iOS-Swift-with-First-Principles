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

###### DispatchQueue
- An object that manages the execution of tasks serially or concurrently on your app's main thread or on a background thread.

###### Design Pattern: MVC
###### UI Element Positioning

###### Defining Structure
- ` struct MyStruct {...} `
- Call/Initialise by: ` MyStruct()`
- Has to start with a Capital Letter since we are defining our own Data Type
- Struct can have properties and it can have behaviours 
  - Properties: ` let name, var citizen, var resources `
  - Behaviour: ` func doSomething() {...} `
- Example:
```
struct Town {
   let name: "Paris Land"
   var citizen = ["PersonOne","PersonTwo","PersonThree"]
   var resources = ["Grain" : 100, "Ore" : 42, "Wool" : 75 ]
   
   func doSomething() {
      print("Defences increased!")
   }
```
- Initialise by: 
` var myTown = Town()`

- Access the elements of Struct:
``` 
print(myTown.citizen)
_______RESULT_______
["PersonOne","PersonTwo","PersonThree"]
```
- Append Elements:
`myTown.citizen.append("PersonFour")`

- Call Method in Struct:
` myTown.doSomething() `

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

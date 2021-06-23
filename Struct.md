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

###### Creating a struct blueprint 
```
struct Town {
   let name: String
   var citizen = [String]
   var resources = [String : Int ]
   
   init(townName: String, people: [String], stats: [String: Int]) {
      name = townName
      citizen = people
      resources = stats
   }
   
   func doSomething() {
      print("Defences increased!")
   }
```
- To initialise another town:
 ` var anotherTown = Town(townName: "Somewhere", people: ["John Doe"], stats: ["Cards" : 40])`

- Access the `anotherTown`:

```
anotherTown.citizen.append("Wilson")
print(anotherTown.citizen)

```

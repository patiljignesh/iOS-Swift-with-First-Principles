## Struct vs Classes

- Structs are passed around by Value
- Classes are passed around by Reference
- Structs are immutable
- Classes have ingeritance
- (Ref Reading)[https://docs.swift.org/swift-book/LanguageGuide/ClassesAndStructures.html]

In Swift, both class and struct are ways to define custom data types, but they have some key differences:

	1.	Class:
	•	Classes are reference types. This means when you assign a class instance to a variable or constant, or pass it to a function, you are working with a reference to the same instance.
	•	Classes can inherit from other classes, meaning they can inherit properties and methods from other classes.
	•	Classes have deinitializers, which are called when a class instance is deallocated.
	•	Classes can allow more than one reference to the instance, so changes in one place can affect the instance in another place.
Example:

'''
class Car {
    var make: String
    var model: String

    init(make: String, model: String) {
        self.make = make
        self.model = model
    }
}

let car1 = Car(make: "Toyota", model: "Camry")
let car2 = car1 // car2 is now a reference to the same instance as car1
car2.model = "Corolla"
print(car1.model) // Outputs "Corolla"
'''

	2.	Struct:
	•	Structs are value types. When you assign a struct instance to a variable or constant, or pass it to a function, it’s actually a copy that’s being passed around.
	•	Structs do not support inheritance.
	•	Structs are generally used for smaller, simpler data structures that encapsulate a few values.
	•	Each instance keeps a unique copy, so changing one won’t affect another.
Example:

struct Point {
    var x: Int
    var y: Int
}

var point1 = Point(x: 1, y: 2)
var point2 = point1 // point2 is now a copy of point1
point2.x = 3
print(point1.x) // Outputs 1



In summary, use classes when you need complex data structures with inheritance and deinitializers, and use structs for simpler data structures where each instance should
# Singleton

> There is only one copy of it that can be shared across all the classes and objects. 

```
import UIKit

class Car {
    
    var colour = "Red"
    
    static let singtonCar = Car() //New object initialised from Car
}

let myCar = Car.singtonCar
myCar.colour = "Blue"

let yourCar = Car.singtonCar
print(yourCar.colour)

// Example: Multiple Classes

class A {
    init() {
        Car.singtonCar.colour = "Brown"
    }
}

class B {
    init() {
        print(Car.singtonCar.colour)
    }
}

let a = A()
let b = B()

// PRINT -------
Blue 
Brown
// _______

```

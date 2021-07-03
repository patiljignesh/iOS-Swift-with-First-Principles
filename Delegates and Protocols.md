# Communication Patterns:
###### There are two ways two views can communicate with each other.

## Notification and Observers
###### Relationship is: 1 to Many

## Deligates and Protocols 
###### Relationship is: 1 to 1

## What are Protocols?

- It is like having a certification 
-

1. Defining the Protocols
- Name of the protocol always start with a Capital Letter

```
protocol MyProtocol {
  // Define requirements 
}

```

2. Adopting the Protocol

```
struct MyStructt: MyProtocol {}
class MyClass: MyProtocol {}

```

## What does Protocols enable for us?

## Clean Architecture + MVVM + Modular Architecture

- [Modular Architecture in iOS](https://medium.com/@leandromperez/a-modular-architecture-in-swift-aafd9026aa99)
- [Clean Architecture and MVVM on iOS](https://tech.olx.com/clean-architecture-and-mvvm-on-ios-c9d167d9f5b3)
- [Coordinator Pattern](https://medium.com/swift2go/refactoring-ios-app-with-coordinator-pattern-for-navigation-alfian-losari-50081bfa7a4a)


### Clean Architecure in a nutshell

1. Clean Architecture Concept: Clean architecture is a software design philosophy that separates code into layers with distinct responsibilities, improving maintainability and testability.
2. Layers in Clean Architecture: Typically includes domains, data, and presentation layers, each with specific roles and isolated from changes in other layers.
3. MVVM Pattern: Model-View-ViewModel (MVVM) is a structural design pattern used in software development for separating logic and user interface, especially in iOS apps.
4. Benefits of MVVM: Enhances code reusability, simplifies testing, and separates business logic from UI code, making it easier to manage and evolve.
5. Data Binding in MVVM: In iOS, data binding between View and ViewModel facilitates automatic UI updates when data changes, often achieved through frameworks like Combine or ReactiveCocoa.
6. Testability: Clean architecture and MVVM together enhance the testability of iOS applications by isolating business logic, allowing for more effective unit testing.
7. Dependency Management: These architectures often employ dependency injection to manage dependencies between components, improving modularity and flexibility.
8. Use Cases in Clean Architecture: They encapsulate specific business rules and are typically located in the domain layer, promoting a single responsibility principle.
9. Repositories and Data Sources: In the data layer, repositories abstract the data source from the rest of the app, allowing for easier changes to data storage and retrieval mechanisms.

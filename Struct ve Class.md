In Swift, both structs and classes are used to create complex data types, but they have some key differences:

1. **Value Types vs. Reference Types**:
   - **Structs** are *value types*. When you assign a struct to a variable or pass it to a function, it is copied. Each instance keeps a unique copy of its data.
   - **Classes** are *reference types*. When you assign a class instance to a variable or pass it to a function, it is shared. Multiple references can point to the same instance.

2. **Inheritance**:
   - **Structs** cannot inherit from other structs or classes.
   - **Classes** can inherit from other classes, enabling polymorphism and reusability.

3. **Initializers**:
   - **Structs** automatically receive a memberwise initializer if they don’t define any of their own.
   - **Classes** don’t receive a default memberwise initializer and must provide their own initializers.

4. **Mutability**:
   - With **structs**, if an instance is declared as a constant (`let`), its properties cannot be modified. This is because structs are value types.
   - With **classes**, even if an instance is declared as a constant, its properties can still be modified (unless they themselves are constants).

5. **Deinitializers and ARC**:
   - **Classes** can have deinitializers (`deinit`) which are called when an instance of the class is deallocated. Classes are subject to Automatic Reference Counting (ARC) for memory management.
   - **Structs** do not have deinitializers and are not subject to ARC since they are copied rather than referenced.

6. **Identity Operators**:
   - Since **classes** are reference types, you can use identity operators (`===` and `!==`) to check if two variables refer to the same instance.
   - This concept does not apply to **structs** because each struct has its own unique copy of its data.

In Swift, the choice between using a struct or a class can affect the performance and functionality of your code. Structs are generally preferred for small, simple data structures that encapsulate a few values, while classes are more suited for complex data structures that need to be shared across different parts of a program.
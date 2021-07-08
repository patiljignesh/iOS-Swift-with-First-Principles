# Internal and External Parameter Names:

###### Defining the Function:

```
   // External Parameter
   // name: this parameter is referenced when calling the function
   
   // Intername Parameter
   // eman: this parameter is referenced when calling within the function
   
   func myFunc(name eman: Type) {
      print(eman)
   }
```

###### Calling the Function:

```
   myfunc(name: value)
```

 ## Alternative way/ Apple way of using External and Internal Parameter
 
###### Defining the Function
```
   // External Parameter
   // name: this parameter is replaced by an _ (underscore) 
   //       which means when calling this function, no parameter name is needed
   
   // Intername Parameter
   // eman: this parameter is referenced when calling within the function
   
   func myFunc(_ eman: Type) {
      print(eman)
   }
```

###### Calling the Function:

```
   myfunc(value)
```

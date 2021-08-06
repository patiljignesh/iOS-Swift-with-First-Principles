
# Clousures
- Clousures are reference types
- Functions without a name
- Anonymous functions 
- [Ref to Map function](https://developer.apple.com/documentation/swift/array/3017522-map)
- [Ref to Clousures](https://docs.swift.org/swift-book/LanguageGuide/Closures.html)
- [More Details](https://learnappmaking.com/closures-swift-how-to/)

## Typical way of passing functions around

```
func calculator(n1: Int, n2: Int, operation: (Int, Int) -> Int) -> {
  return operation(n1, n2)
}

fun multiply(no1: Int, no2: Int) -> Int {
  return no1 * no2
}

calculator(n1: 2, n2: 3, operation: multiply)
```

## Closure way

###### Example 1

```
func calculator(n1: Int, n2: Int, operation: (Int, Int) -> Int) -> {
  return operation(n1, n2)
}

let result = calculator(n1: 2, n2: 3) {$01 * $1})
print(result)
```

###### Example 2

```
// Add one to each element 
let array = [6, 2, 3, 9, 4, 1]

array.map({$0 + 1})
```

## Closure Expression Syntax
###### Closure expression syntax has the following general form:

```
{ (parameters) -> return_type in
    statements
}

```

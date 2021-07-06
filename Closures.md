
# Clousures
- Functions without a name
- Anonymous functions 

```
func calculator(n1: Int, n2: Int, operation: (Int, Int) -> Int) -> {
  return operation(n1, n2)
}

fun multiply(no1: Int, no2: Int) -> Int {
  return no1 * no2
}

calculator(n1: 2, n2: 3, operation: multiply)
```

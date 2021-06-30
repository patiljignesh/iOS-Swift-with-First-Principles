1.	Forcing Unwrapping
```
optional!

```

2.	Checking for nil Value

```
if optional != nil {
  optional!
}
```

3.  Optional Binding

```
if let safeOptional = optional {
  safeOptional
}
```

4.  Nil Coalescing Operator: This would be the preferred way, when possible 

```
optional ?? defaultValue
```

5.  Optional Chanining

```
optional?.property
optional?.method()
```

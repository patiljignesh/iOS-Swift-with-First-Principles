# Computed Properties

###### Example 1

```
var aProperty: Int { // 2. It will set this property once the computation has been completed. 
    return 2 + 1 // 1. it will compute
}
```

###### Example 2
```
    var conditionName: String {
        switch conditionId {
        case  200...299 :
            return "cloud.bolt.rain"
        case  300...399 :
            return "cloud.drizzle"
        case  400...499 :
            return "cloud.rain"
        case  600...699 :
            return "cloud.snow"
        case  700...799 :
            return "sun.haze"
        case  800:
            return "sun.max"
        case  801...899 :
            return "cloud.fill"
        default:
            return "None"
        }
    }
    
```

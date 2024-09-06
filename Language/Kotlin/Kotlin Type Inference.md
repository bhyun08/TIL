Kotlin's Type Inference is a feature that infers the type of variable. By using this, we can reduce code lines. You can specify the type, but you don't have to specify it because the compiler will infers the type.      
# How work Type Inference?
Type Inference work on compile time. Compiler infers variable's assigned value.      
```kotlin
var hello = "hello" // As value is String, infer String
var a = 1495 // As value is Int, inference Int
var babo = true // As value is boolean, infer boolean
```
Because Type Inference can infers return type. Type Inference also work function.     
```kotlin
fun add(a: Int, b: Int) = a + b // As a + b is Int, return type is Int So, infer return type int
```

---
Reference link 🙂       
https://yoonda.tistory.com/17       
https://medium.com/@mobiledev4you/kotlin-type-inference-type-check-smartcast-49c5f98fac1b
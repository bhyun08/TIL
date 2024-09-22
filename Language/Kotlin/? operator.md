In Kotlin, the `?` operator is an operator used for several functions related to **null-safety**. There are many different types of `?` operators, and the correct operators can be used depending on the situation.
## Nullable Type (`?`)
Kotlin's variable is can't be null basically. But if use `?` operator behind variable name , that variable is changed nullable type. 
```kotlin
val name: String? = null
```
## Safe Call (`?.`)
Check that the variable is null and call the property or function only if it is not null. If it is null, the result of the entire expression is null.
```kotlin
val length = name?.length
```
## Elvis Operator (`?:`)
Operator that provides the default value if null for the nullable variable. Returns the value after the preceding expression if null.
```kotlin
val length = name?.length ?: 0
```
## Non-null Assertion (`!!`)
Used when you are sure that the variable is not null. If a variable with this operator has a null value, a `NullPointerException` happens. (*Prohibition of actual business use*)
```kotlin
val length = name!!.length
```

---
Reference link 🙂       
https://growth-coder.tistory.com/28
Kotlin Type Casting is a feature so that we can change variable's **data type**. Kotlin Type Casting is smarter than other programming language. So, we can use this efficiently.
# How work Type Casting
Kotlin Type Casting available using **is Operator** and **as Operator**.
## is Operator
is Operator use in situation that you want to check data type check.         
Write variable name In front of is Operator and write data type behind is Operator. is Operator returns true if the variable data type matches the check data type. if not matches, return false.    
So, is Operator can returns only boolean type.         

**Example**
```kotlin
var dat:String = "hello"

dat is Int // return false
dat is String // return true
```
## as Operator
as Operator use in situation that you want to change data type. But, as Operator can applies to only [[Kotlin Any]] data type. However, if it is not a variable, as Operator can use to class, interface and so on.

**Example**
```kotlin
val any: Any = "Hello" 
if (any is String) { 
	val str: String = any as String // any variable transform to string
}
```
## as? Operator
If as Operator fail to change data type, as Operator returns `ClassCastException`.           
as? Operator is feature in order to prevent this Exception.          
as? Operator returns `null` if fail to change data type.

---
Reference link 🙂       
https://thdev.tech/kotlin/2020/10/20/kotlin_effective_07/
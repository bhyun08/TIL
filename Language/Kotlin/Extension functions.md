Extensions function is the ability to add new features to an existing class, allowing you to extend the function(method) without modifying the source code of the class. This extension is called for an instance of a particular class type, but was not actually added inside that class.
```kotlin
fun MutableList<Int>.swap(index1: Int, index2: Int) { 
	val tmp = this[index1] // 'this' corresponds to the list 
	this[index1] = this[index2] 
	this[index2] = tmp 
}
```
Extensions are defined outside the class, but are called as if they are members of the class. Extensions define the function after specifying the type of receiver object.

---
Reference link 🙂       
https://kotlinlang.org/docs/extensions.html#extension-functions
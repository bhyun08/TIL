Data class is class that have methods to handle data conveniently. When create data class, use `data` keyword in front of `class` keyword. If declare data class, Kotlin compiler automatically create useful methods. 
# Data class methods
The compiler automatically derives the following members from all properties declared in the primary constructor.
#### `equals()`
Compare whether two objects have the same property value. 
#### `hashCode()`
Generates a hash code for the object.
#### `toString()`
Returns the contents of an object as a string.
#### `componentN()`
componentN() is able to **Destructuring Declarations**. Destructuring Declaration is feature that to break down properties into individual items. componentN() divide and returns by work Destructuring Declarations.
#### `copy()`
 Can change the value of some properties while copying objects.

---
Reference link 🙂       
https://kotlinlang.org/docs/data-classes.html
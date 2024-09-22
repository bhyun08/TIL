A higher-order function is a function that takes functions as parameters, or returns a function. High-order function be mostly used in [[Functional programming]].

**Example**
```kotlin
fun operateOnNumbers(a: Int, b: Int, operation: (Int, Int) -> Int): Int {
    return operation(a, b)
}

fun main() { 
	val sum = operateOnNumbers(5, 10) { x, y -> x + y } 
	println(sum) // 15 
}
```
This function is receiving function as parameters. In the example above, the operationOnNumber function receives two Int values and receives a function in the form of `(Int, Int) -> Int` as a factor. This function receives two numbers and returns the result of processing them with the operation function. 

```kotlin
fun getOperationFunction(operation: String): (Int, Int) -> Int {
    return when (operation) {
        "add" -> { x, y -> x + y }
        "subtract" -> { x, y -> x - y }
        else -> throw IllegalArgumentException("Invalid operation")
    }
}

fun main() { 
	val addFunction = getOperationFunction("add") 
	println(addFunction(5, 10)) // 15 
}
```
In the above example, a higher-order function called getOperationFunction returns a function in the form of `(Int, Int) -> Int` depending on the string received as input.

---
Reference link 🙂      
https://kotlinlang.org/docs/lambdas.html#higher-order-functions
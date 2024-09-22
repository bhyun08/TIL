Kotlin's Lambda expressions and Anonymous functions are a method of defining functions anonymously. Lambda expressions and Anonymous functions are also **Function Literals**. Function Literal is a function that is not declared but is immediately passed by expression. 
# Lambda expressions
Lambda is a type of anonymous functions. Lambda is one of the key elements in support of functional programming. Lambda is basically a function, unnamed, and easily defined.
```kotlin
val sum: (Int, Int) -> Int = { x: Int, y: Int -> x + y }
```
This is lambda expressions. `val sum: (Int, Int) -> Int` is to define a function type. `sum` variable means that it has a function type that takes two **Int** parameters and returns **Int**. `{ x: Int, y: Int -> x + y }` is lambda expressions. `x` and `y` is parameters. And `->`'s role is connecting parameters and function body. `x + y` is function body. This lambda expressions returns `x + y`.

If you leave all the optional annotations out, what's left looks like this:
```kotlin
val sum = { x: Int, y: Int -> x + y }
```
### Lambda Capture
Lambda expressions can capture outside variables. In other words, lambda can access and modify the variables outside in the lambda interior.
```kotlin
var count = 0
val increment = { count += 1 }

increment()
println(count)  // print: 1
```
### Multiple lines of expression inside Lambda
When you have multiple lines of code in a lambda, you can include multiple lines using braces. The last line is returned.
```kotlin
val printMessage = { message: String ->
    println("Message length: ${message.length}")
    println("Message content: $message")
    "Processed"
}

val result = printMessage("Hello, Kotlin!")
println(result)  // print: Processed
```
# Anonymous functions
Anonymous Function is an unnamed function that uses the `fun` keyword when defining a function in Kotlin, but allows you to omit the name of the function. 
```kotlin
val anonymousFunc = fun(x: Int, y: Int): Int { 
	return x + y 
}
```
This is Anonymous function. Anonymous function use `fun` keyword but function name is omit. But Anonymous function also have to include parameters and return type like general functions.
# Difference between Lambda expressions and Anonymous functions
Both anonymous functions and lambda expressions play similar roles as anonymous functions, but there are some important differences.
## Return's work
- **Lambda** : In the lambda expression, the function enclosing the lambda can be terminated when the return keyword is used. Thus, the syntax with label can only be terminated for a specific lambda.
- **Anonymous functions** : When you use the return keyword, return only works for the anonymous function itself and ends that function.
## Type inference
 - **Lambda** : If Compiler can inference type, can omit parameter type.
 - **Anonymous functions** : Always specify a parameter type.

---
Reference link 🙂       
https://kotlinlang.org/docs/lambdas.html#underscore-for-unused-variables
https://medium.com/@yangweigbh/how-kotlin-lambda-capture-variable-ef90e11e531d
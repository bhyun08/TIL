In the Go language, variables refer to the memory space for storing values, and you can store data for a specific type. It is also possible to **infer** types when declaring variables. 
# Go variable role
1. Variable names can only begin with a letter or _.  
2. You can then use all numbers and letters, _.  
3. Case-sensitive.  
4. Golang's keyword is not available.  
5. There is no length limit.
# var declaring
In Go language, when declare variable, normally use `var` keyword.
```go
var number int // only declaring
var rabbit string = bunny // assign a value while declaring
```
# Group declaring
It is also possible to declare variables grouped together at once.
```go
var dog, cat, people int // only declaring
var dog, cat, people int = 1, 2, 3 // assign a value while declaring

var(
	dog int
	cat bool
	people string
)
```
# Type Inference
Go even gives you type inference.
### var type inference
```go
var a = 10 // compiler auto type infer

func main() {
	z := "hello" // compiler auto type infer but not use 'var'
}
```
In the Golang, we can use type inference to way that use `var`, use `:=`.

First, If the variable is declared var and the type is not specified, the assigned value is viewed and the type is automatically specified. However, if the value is not assigned, the compiler will cause an error.       
Second, Inside the function, type inference is possible using the ':=' operator. In this case, the var keyword is not required, and the type is also inferred from the assigned value.

| **Sortation**      | **`var a = 10`** | **`g := "Go language"`** |
| ------------------ | ---------------- | ------------------------ |
| **Type Inference** | auto             | auto                     |
| **Scope**          | global variable  | only in a function       |
| **Code brevity**   | longer           | more concise             |

---
Reference link 🙂    
https://341123.tistory.com/25
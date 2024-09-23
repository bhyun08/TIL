Functional programming is a programming paradigm based on the concept of a mathematical function. Functional programming's major purpose is avoid status change and to use pure function. And also use higher-order function etc. to consist programming logic.
# Type of Function
Key Concepts and Features of Functional Programming
### Pure Function
Functions that must always return the same value to the same input. Characterized by not relying on external conditions or variables and not causing side effects. Namely, the input is processed and only the result is returned without changing the state outside the function.
### Stateless, Immutability
In Functional Programming, data must keep immutability that not change. If it is necessary to change the data, make a copy of the data without changing the original data structure, change some of it, and proceed with the work using the changed copy. (Capture)
### Expressions
Command-type programming pays attention to what and how to do it, and [[Declarative Programming]] pays attention to what to do.
### Fist-class & High-order-function
A function can be treated as a first-class object and assigned to a variable or passed to another function's factor. This allows the function to be treated like a value. Also High-order-function is function that receive one or more functions as parameters, or return functions as results. In this way, functions can combine like lego.
# Functional programming's Pros and Cons
### Pros
- High level Abstraction
- Easy to reuse code in function
- Aiming for immutability
### Cons
- The recursive code style may fall into an infinite loop
- It may be easy to use pure functions, but it is not easy to combine them

---
Reference link 🙂     
https://jongminfire.dev/%ED%95%A8%EC%88%98%ED%98%95-%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%EC%9D%B4%EB%9E%80
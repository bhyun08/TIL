Declarative Programming is a programming paradigm that to  specify "what to want" better than explain "how". Namely, program express working result or purpose that program have to perform and It's up to the language or the system to decide how that will be done.
# Declarative Programming character
- Goal-centric: articulate what you want to achieve, and do not describe the process one by one.  
- No order of instructions required: the system handles it without the need for the programmer to specify a specific order.  
- State change management: The system manages it on its own rather than explicitly dealing with state changes.
# SQL vs HTML (Best Example)
**SQL**: A database query language that describes what data you want rather than how to retrieve it.
```sql
SELECT name FROM users WHERE age > 30;
```
**HTML**: A language that describes the structure of a web page, declaring what elements are displayed and how.
```html
<h1>Hello, World!</h1>
```
# Pros and Cons
### Pros
- Simplicity: It specifies the objectives of the task, so the code is clear and concise.
- Maintenance: Manage detailed implementations of tasks within the system, making re-factoring easier when changing code.
- Ease of parallel processing: It is better suited for parallel processing environments because it does not rely on state changes or order.
### Cons
- Difficulty representing complex tasks: tasks that require complex control flows may not be intuitive compared to imperative programming.

---
Reference link 🙂     
https://velog.io/@jelkov/%EC%84%A0%EC%96%B8%ED%98%95-declarative-programming%EA%B3%BC-%EC%A0%88%EC%B0%A8%ED%98%95-imperative-programming%EC%9D%98-%EC%B0%A8%EC%9D%B4
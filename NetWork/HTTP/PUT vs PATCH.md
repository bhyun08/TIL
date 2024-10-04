Both PUT and PATCH are HTTP methods used to update the server's resources, but there are important differences in how they behave.
# PUT
- Replace the entire resource.  
- The client must send the entire data of the resource to the server, which completely replaces the existing resource with the new resource.  
- If only some fields are sent, the **remaining fields are deleted**.

**Example**
- Existing Resources
```json
{ 
	"name": "Alice", 
	"age": 25, 
	"city": "New York" 
}
```
- PUT Request
```http
PUT /users/1
Content-Type: application/json

{
  "name": "Alice",
  "age": 26
}
```
- Result
```json
{
  "name": "Alice",
  "age": 26,
  "city": null  // "city" field deleted
}
```
# PATCH
- Partially modify the resource.
- The client sends only some of the fields that you want to change, and the rest of the fields remain the same.

**Example**
- Existing Resources
```json
{ 
	"name": "Alice", 
	"age": 25, 
	"city": "New York" 
}
```
- PUT Request
```http
PATCH /users/1
Content-Type: application/json

{
  "age": 26
}
```
- Result
```json
{
  "name": "Alice", // still live
  "age": 26,
  "city": "New York"  // still live
}
```

---
Reference link 🙂     
https://programmer93.tistory.com/39
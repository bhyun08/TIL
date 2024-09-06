HTTP is an abbreviation of **Hypertext Transfer Protocol**. As you can also know from the name, HTTP is Communication Protocol. So, HTTP is communication **rule**. Because HTTP is text, We can read communication status easily. 

HTTP is consist of **Request** and **Response**.

These messages are called **HTTP message**.
# HTTP Message
HTTP Message divide Request and Response.
## HTTP Request
HTTP Request is the way Internet communications platforms such as web browsers ask for the information they need to load a website. In other word, It means that the client sends a message to the server.

HTTP Request is contains these information.
1. HTTP Version
2. Request Target (`path to send a request`)
3. HTTP Method
4. HTTP Request header
5. Optional HTTP body

To send these information, HTTP Request divide into three main categories.
### Start line
Start line contains HTTP Version, HTTP Method, Request Target    
ex) `GET /hello.htm HTTP/1.1`
### Headers
HTTP Request headers communicate core information, such as what browser the client is using and what data is being requested.
![](https://www.cloudflare.com/img/learning/ddos/glossary/hypertext-transfer-protocol-http/http-request-headers.png)
### Body
The body of an HTTP request contains any information being submitted to the web server.      
Body is can non-existent.

Example
```json
{
	"name":"hello",
	"age":"12",
	"gender":"man"
}
```
## HTTP Response
HTTP Response is what client receive from an Internet server in answer to an HTTP request.    

HTTP Response contains these information.      
1. HTTP status code
2. HTTP response headers
3. Optional HTTP body

To send these information, HTTP Response also divide into three main categories.    
### Status line
Status line contains HTTP status and HTTP Version      
ex) `HTTP/1.1 200 OK`
### Headers
Much like an HTTP request, an HTTP response comes with headers that convey important information such as the language and format of the data being sent in the response body.
![](https://www.cloudflare.com/img/learning/ddos/glossary/hypertext-transfer-protocol-http/http-response-headers.png)
### Body
Successful HTTP responses to ‘GET’ requests generally have a body which contains the requested information.

---
Reference link 🙂     
https://velog.io/@wlwl99/HTTP        
https://www.cloudflare.com/learning/ddos/glossary/hypertext-transfer-protocol-http/
DispatcherServlet is in Spring Web MVC control the overall processing process. Spring Web MVC is a kind of like servlet, but, isn't servlet class. It just use servlet. The key class that serves as a servlet in Spring Web MVC is the **DispatcherServlet**, which serves as an entry point for all requests in Spring Web MVC and is at the heart of the web application. Because DispatcherServlet is Servlet class, DispatcherServlet to be included Servlet Container(ex. Tomcat).
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F2236F14757BBD25119)
This is Spring Framework Web Server Structure. DispatcherServlet is one of Servlet Class.
# DispatcherServlet Flow
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F21121346579D543324)
If come client's request, DispatcherServlet receives request first. And DispatcherServlet is involved in every work, through method.

---
Reference link 🙂     
https://docs.spring.io/spring-framework/reference/web/webmvc/mvc-servlet.html            
https://jojoldu.tistory.com/28               
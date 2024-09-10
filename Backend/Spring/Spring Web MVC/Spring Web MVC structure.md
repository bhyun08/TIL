Spring Web MVC is divide several classes. And each class is in charge of role that to receive the web request and to send web response. To effectively manage roles, Classes are divided based on MVC.
## Spring Web MVC Work Flow
![](https://terasolunaorg.github.io/guideline/1.0.1.RELEASE/en/_images/RequestLifecycle.png)
Spring Web MVC work like these flow. Each Class organically going to be combined.
1. `DispatcherServlet` receives the request.
2. `DispatcherServlet` dispatches the task of selecting an appropriate `controller` to `HandlerMapping`. `HandlerMapping` selects the controller which is mapped to the incoming request URL and returns the`(selected Handler)` and `Controller` to `DispatcherServlet`.
3. `DispatcherServlet` dispatches the task of executing of business logic of `Controller` to `HandlerAdapter`.
4. `HandlerAdapter` calls the business logic process of `Controller`.
5.  `Controller` executes the business logic, sets the processing result in `Model` and returns the logical name of view to `HandlerAdapter`.
6. `DispatcherServlet` dispatches the task of resolving the `View` corresponding to the View name to `ViewResolver`. `ViewResolver` returns the `View` mapped to View name.
7. `DispatcherServlet` dispatches the rendering process to returned `View`.
8. `View` renders `Model` data and returns the response.
## [[DispatcherServlet]] 
- also called a front controller
- control the overall processing process
## HandlerMapping
- find a controller to handle the request directly
## HandlerAdapter
- request execution of mapped controller
## Controller
- performs the HTTP request delivered by `DispatcherServlet` and stores the result in the `Model`
- executes the request directly, and returns the execution result
- controllers are classes that developers have to develop themselves
## ModelAndView
- `ModelAndView` is an object from which the `Model` and `View` returned by the `Controller` are Wrapped.
## View Resolver
- after checking the `View Name`, search for a `View file (jsp)` that reflects the logic processing results received from the actual controller.
## View
- generates a final screen reflecting the logic execution result.
---
Reference link 🙂           
https://terasolunaorg.github.io/guideline/1.0.1.RELEASE/en/Overview/SpringMVCOverview.html     
https://velog.io/@do_dam/Spring-MVC란-무엇인가-스프링-MVC-구조-이해#spring-mvc
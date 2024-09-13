**Inversion of Control (IoC)** is a phenomenon that transfers the control of objects or portions of a program to a container or framework. We most often use it in the context of object-oriented programming. So, Spring framework also have this mechanism.

By reversing the dependence of objects, the degree of coupling between objects can be reduced.
# How to work IoC in Spring?
![](https://i0.wp.com/javaconceptoftheday.com/wp-content/uploads/2023/08/Spring_IoC_Container.png?fit=1015%2C507&ssl=1)       
This is Spring IoC's work flow. Spring IoC most is worked by [[IoC Container]],  [[Bean]] and [[Dependency Injection (DI)]]. 

If you register object as a bean, It's happening **IoC**. And bean object is managed by IoC container. The bean registration of the object itself should be done by the developer, but the act of managing the bean object is managed by the framework due to the IoC phenomenon.

---
Reference link 🙂       
https://www.baeldung.com/inversion-control-and-dependency-injection-in-spring            
https://javaconceptoftheday.com/spring-ioc-container/                     

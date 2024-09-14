IoC Container is container that manage [[Bean]] registering object by [[Inversion of Control (IoC)]]. [[Dependency Injection (DI)]] also work by IoC container. IoC container uses configuration metadata to manage the beans. IoC container also called Spring container. Because, Spring's major feature is IoC, many Spring Developers call like that.
# Bean Factory vs Application Context
![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*aZL8-0kNSgKyef9QGwgk4g.jpeg)             
Spring manages these IoC containers as interface. Spring's IoC container is divide two class that Bean Factory and Application Context.
## Bean Factory
It refers to the most basic IoC container and class responsible for creating beans and establishing dependencies. It is the top-level interface for accessing spring bin containers.
- as an IoC container, it is also responsible for managing and inquiring about spring bins
- bean creating is worked by **Lazy Loading**.
- created at the time of import, not at the time of registering the bean

**Example**
```java
@Test
public void whenBFInitialized_thenStudentInitialized() {
    Resource res = new ClassPathResource("ioc-container-difference-example.xml");
    BeanFactory factory = new XmlBeanFactory(res);
    Student student = (Student) factory.getBean("student"); // bean created

    assertTrue(Student.isBeanInstantiated());
}
```
## Application Context
It's an expanded version of the `Bean Factory`. Expand your Bean Factory, providing more features and making it easier to use.
- use a **Eager Loading**
- load all beans at runtime

**Example**
```java
@Test
public void whenAppContInitialized_thenStudentInitialized() {
    ApplicationContext context = new ClassPathXmlApplicationContext("ioc-container-difference-example.xml"); // bean created

    assertTrue(Student.isBeanInstantiated());
}
```

---
Reference link 🙂     
https://medium.com/@ravichandola/spring-ioc-invert-control-simplify-development-in-nutshell-5aaf8eaa5b72            
https://www.baeldung.com/spring-beanfactory-vs-applicationcontext           
https://velog.io/@saint6839/BeanFactory-와-ApplicationContext의-차이                
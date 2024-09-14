Bean is object that is managed by Spring Container(IoC Container). When object register bean, Spring Framework manage object. Because the Spring Framework manages objects, it can perform functions such as dependency injection.
# How to register object as a bean?
We can have 3 way that register object as a bean.
### XML
Register a bin with XML using the `<bean>` tag.

**Example**
```xml
<bean id="exampleBean" class="examples.ExampleBean"/> 
<bean name="anotherExample" class="examples.ExampleBeanTwo"/>
```
###  `@Bean` annotation
A method of writing a `@Bean` annotation to a method to register the return value of the method as a Bean. And use `@Configuration` to be can scan bean.

**Example**
```kotlin
@Configuration 
class AppConfig { 
	@Bean 
	fun transferService() = TransferServiceImpl() 
}
```
### Component Scan
This is how to attach stereotyped annotations such as `@Component`, `@Service`, `@Repository`, `@Controller` to classes so that the Spring container automatically registers as a bean.

**Example**
```java
@Service
public class UserService { 
	public void Login(LoginRequest loginRequest) {
		System.out.println("bean login!");
	}
}
```

---
Reference link 🙂     
https://docs.spring.io/spring-framework/reference/core/beans/definition.html                   
https://dev-wnstjd.tistory.com/440#:~:text=빈(Bean)은%20스프링%20컨테이너,를%20스프링%20빈이라고%20한다.
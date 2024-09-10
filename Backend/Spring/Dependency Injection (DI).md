Dependency Injection(DI) is to define relationships between objects. When Spring Container makes bean object, Spring Container inject dependency between objects. In this situation, happen [[Inversion of Control (IoC)]] phenomenon.

**The object does not look up its dependencies and does not know the location or class of the dependencies.**

If use DI, code is cleaner than before and the relationship between objects is weaker than before.
# How to Inject Dependency
To Inject Dependency way is divided 3 ways.
## Constructor Inject
Constructor Injection is way that class that Inject Dependency add constructor that include dependency class.

**Example**
```java
public class ExampleBean { 

	private final String ultimateAnswer; 
	private final UserRepository userRepository;
	
	public ExampleBean(String ultimateAnswer, UserRepository userRepository) { 
		this.userRepository = userRepository;
		this.ultimateAnswer = ultimateAnswer; 
	}
}
```
## Setter Inject
Setter Injection is way that class that Inject Dependency add set-Method that include dependency class.

**Example**
```java
public class ExampleBean { 

	private Movie movie;
	
	public void setMovie(Movie movie) {
		this.movie = movie;
	}
}
```
## Field Inject
Field Inject is way that class that Inject Dependency add to field that dependency class. But, Field Inject way can't work on one's own. It have to use `@Autowired` annotation.

> What is `@Autowired` annotation?
> `@Autowired` is annotation that is used in Spring Framework. In order to use inject Dependency, It is mainly use to constructor, fields, and setter methods to automatically inject dependencies into those locations.

**Example**
```java
public class ExampleBean { 

	@Autowired
	private UserEntity userEntity;
}
```

---
Reference link 🙂      
https://docs.spring.io/spring-framework/reference/core/beans/dependencies/factory-collaborators.html
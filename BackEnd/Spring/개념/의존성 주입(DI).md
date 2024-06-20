의존성 주입은 IoC(Inversion of Control) 원칙을 구현하는 핵심 기술입니다. 의존성 주입에서는 객체가 필요로 하는 의존 객체를 외부에서 주입받는다.

이를 통해 객체 간의 결합도를 낮추고 유연성을 높일 수 있다. 의존성 주입은 객체 간의 관계를 런타임에 동적으로 주입하여 결합도를 낮추고 유연성을 높이는 디자인 패턴이다.

스프링에서는 IoC 컨테이너가 의존성 주입을 담당한다. 개발자는 XML, Java 코드, 어노테이션 등을 통해 Bean 정보를 제공하면, IoC 컨테이너가 이를 바탕으로 객체를 생성하고 의존성을 구성한다.

### 의존성 주입 방법

1. 생성자 주입
	
	```java
public class UserService {
    private final UserRepository userRepository; 

    public UserService(UserRepository userRepository) {
        this.userRepository = userRepository; // UserRepostiory 클래스를 의존한다.
    }

    public void createUser(User user) {
        userRepository.save(user);
    }
}
```
	생성자 주입은 생성자를 통해 의존 객체를 주입받는 방식이다. 생성자에서 필요한 의존 객체를 받아 필드에 할당한다. 이를 통해 UserService 클래스는 UserRepository 클래스에 대한 의존성을 가지게 된다. 생성자 주입은 필수적인 의존성을 명시적으로 드러낼 수 있다.
	
2. 수정자(Setter) 주입
	
	```java
public class UserService {
    private UserRepository userRepository;

    public void setUserRepository(UserRepository userRepository) {
        this.userRepository = userRepository; // UserRepostiory 클래스를 의존한다.
    }

    public void createUser(User user) {
        userRepository.save(user);
    }
}
```
	수정자 주입은 Setter 메서드를 통해 의존 객체를 주입받는 방식이다. Setter 메서드를 통해 UserRepository 객체를 주입받습니다. 이 방식은 생성자 주입에 비해 의존성이 명확하지 않지만, 선택적인 의존성을 처리할 때 유용하다.
	
3. 필드 주입
	
	```java
public class UserService {
    @Autowired 
    private UserRepository userRepository; // UserRepostiory 클래스를 의존한다.

    public void createUser(User user) {
        userRepository.save(user);
    }
}
```
	필드 주입은 필드에 직접 의존 객체를 주입받는 방식이다. @Autowired 어노테이션을 사용하여 스프링 컨테이너가 UserRepository 객체를 주입한다.


[[@Autowired]]
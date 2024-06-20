빈(Bean)이란 스프링 컨테이너에 의해 관리되는 자바 객체이다. 스프링 빈은 스프링 IoC(Inversion of Control) 컨테이너에 의해 관리된다.

### 빈의 특징

1. **IoC(Inversion of Control) 컨테이너에 의해 관리된다**
    - 스프링 빈은 스프링 IoC 컨테이너에 의해 생성, 관리, 소멸된다.
    - 개발자가 직접 객체를 생성하고 관리하는 것이 아니라 컨테이너가 대신 수행한다.
    
2. **의존관계 주입(Dependency Injection, DI)**
    - 스프링 빈 간의 의존관계는 컨테이너가 자동으로 주입해준다.
    - 개발자는 필요한 의존 객체를 선언하기만 하면 된다.
	
3. **싱글톤(Singleton) 스코프**
    - 기본적으로 스프링 빈은 싱글톤 스코프를 가진다.
    - 즉, 하나의 빈 인스턴스만 생성되어 공유된다.
    
4. **라이프사이클 관리**
    - 스프링 컨테이너는 빈의 생성, 의존관계 설정, 초기화, 소멸 등의 전체 생명주기를 관리한다.
    - 개발자는 빈의 라이프사이클에 직접 개입할 수 있다.
    
5. **다양한 스코프**
    - 싱글톤 외에도 프로토타입, 요청, 세션, 애플리케이션 등 다양한 스코프를 지원한다.
    - 빈의 사용 목적에 따라 적절한 스코프를 선택할 수 있다.
    
6. **설정 메타데이터**
    - 스프링 빈은 XML, Java 코드, 어노테이션 등을 통해 설정 메타데이터로 정의된다.
    - 이 메타데이터에는 빈의 ID, 클래스, 의존관계, 스코프 등의 정보가 포함된다.
    
7. **빈 후처리**
    - 빈 인스턴스가 생성된 후 추가적인 사용자 정의 로직을 적용할 수 있다.
    - BeanPostProcessor 인터페이스를 구현하여 빈 후처리기를 등록할 수 있다.


### 빈 등록

1. 컴포넌트 스캔을 통한 자동 등록
```java
@Component
public class MyBean {
    // 빈 정의 코드
}
```
`@Component` 어노테이션을 클래스에 붙이면 스프링 컨테이너가 자동으로 해당 클래스를 빈으로 등록한다. 이때 빈의 이름은 클래스명의 첫 글자를 소문자로 바꾼 것이 된다.

2. 수동 등록 - XML 설정
```xml
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
                           https://www.springframework.org/schema/beans/spring-beans.xsd">

    <bean id="myBean" class="com.example.MyBean">
        <!-- 빈 정의 코드 -->
    </bean>
</beans>
```

XML 설정 파일에서 `<bean>` 태그를 사용하여 빈을 수동으로 등록할 수 있다. `id` 속성으로 빈의 이름을 지정하고, `class` 속성으로 빈의 클래스 경로를 지정한다.

3. 수동 등록 - Java 구성 클래스
```java
@Configuration
public class AppConfig {
    @Bean
    public MyBean myBean() {
        return new MyBean();
    }
}
```
자바 구성 클래스에서 `@Configuration` 어노테이션을 사용하고, `@Bean` 어노테이션이 붙은 메서드를 통해 빈을 수동으로 등록할 수 있다. 메서드 이름이 빈의 이름이 된다.

4. 자동 의존관계 설정
```java
@Service
public class MyService {
    private final MyBean myBean;

    public MyService(MyBean myBean) {
        this.myBean = myBean;
    }
}
```
`@Autowired` 어노테이션을 사용하지 않고도, 생성자 주입을 통해 자동으로 의존관계를 설정할 수 있다. 스프링 컨테이너가 알아서 `MyBean` 타입의 빈을 찾아 주입한다.

[[IoC]]
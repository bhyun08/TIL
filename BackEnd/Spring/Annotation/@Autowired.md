`@Autowired` : 어노테이션은 스프링 프레임워크에서 의존성 주입(Dependency Injection)을 위해 사용된다. 이 어노테이션을 사용하면, 스프링이 자동으로 해당 필드, 생성자, 또는 메서드에 적절한 빈(bean)을 주입해준다. 
### 주입 방식

1. **필드 주입(Field Injection)**: 필드에 `@Autowired`를 적용하면, 해당 필드에 적절한 타입의 빈이 자동으로 주입된다.
	
	~~~java
	public class MyService { 
		@Autowired 
		private MyRepository myRepository; 
	}
	~~~
    
2. **생성자 주입(Constructor Injection)**: 생성자에 `@Autowired`를 적용하면, 스프링이 생성자를 통해 의존성을 주입한다. 생성자가 하나일 경우, `@Autowired` 어노테이션을 생략할 수도 있다.
	
    ~~~java
    public class MyService { 
	    private final MyRepository myRepository; 
	    
	    @Autowired 
	    public MyService(MyRepository myRepository) { 
			this.myRepository = myRepository; 
	    } 
    }
    ~~~
    
3. **메서드 주입(Method Injection)**: 메서드에 `@Autowired`를 적용하면, 스프링이 해당 메서드를 호출하면서 인자로 적절한 빈을 주입한다.
~~~java
public class MyService { 
	private MyRepository myRepository; 
	
	@Autowired 
	public void setMyRepository(MyRepository myRepository) { 
			this.myRepository = myRepository; 
		} 
	}
~~~
### 동작 원리
- **타입 기반 매칭**: 기본적으로 `@Autowired`는 타입을 기준으로 매칭하여 적절한 빈을 찾는다. 동일한 타입의 빈이 여러 개 있는 경우, `@Primary` 어노테이션이 붙은 빈이 우선적으로 주입된다.

- **필수 여부**: `@Autowired`의 기본 동작은 필수(required)이다. 만약 주입될 빈이 없으면 애플리케이션 컨텍스트 초기화 시점에 예외가 발생합니다. 이를 방지하려면 `@Autowired(required = false)`로 설정할 수 있다.

- **Qualifier**: 동일한 타입의 빈이 여러 개 있는 경우, `@Qualifier` 어노테이션을 함께 사용하여 특정 빈을 명시적으로 지정할 수 있다.

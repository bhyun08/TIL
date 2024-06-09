`@Getter` :  Lombok 라이브러리에서 제공하는 어노테이션으로, 해당 클래스의 필드에 대한 getter 메서드를 자동으로 생성해주는 역할 이 어노테이션을 사용하면 getter 메서드를 직접 작성할 필요가 없어진다.

ex)
```java
import lombok.Getter; 

@Getter 
public class MyClass { 
	private String name; 
	private int age; 
}
```

위 코드에서 `@Getter`가 지정된 `MyClass` 클래스는 `getName()`과 `getAge()` 메서드를 자동으로 생성
이렇게 생성된 getter 메서드를 사용하여 클래스의 필드에 접근이 가능하다

`@Getter`는 클래스의 모든 필드에 대해 getter 메서드를 생성한다. 만약 특정 필드에 대해서만 getter 메서드를 생성하고 싶은 경우에는 `@Getter` 어노테이션에 `@Getter(AccessLevel.NONE)`과 같이 접근 수준을 지정 해야한다. 또한 `@Getter` 어노테이션을 필드 레벨에 사용하여 특정 필드에만 getter 메서드를 생성하도록 지정할 수도 있다.

[[Getter 메서드]]
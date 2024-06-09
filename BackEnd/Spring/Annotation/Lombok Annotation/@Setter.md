`@Setter` : 주로 Java나 Kotlin에서 사용되며, Lombok 라이브러리에서 제공하는 어노테이션, 이 어노테이션을 사용하면 클래스의 필드에 대해 자동으로 setter 메서드를 생성한다. 

ex)
~~~java
import lombok.Setter;

@Setter
public class Person {
    private String name;
    private int age;
}
~~~
위의 코드에서 `Person` 클래스의 `name`과 `age` 필드에 대한 setter 메서드가 자동으로 생성된다.


- `@Setter` 어노테이션을 무분별하게 사용하면, 불변성을 유지하기 어렵고, 객체의 상태 변경이 어디서든 가능해지므로 주의가 필요하다.
- Lombok의 `@Setter` 어노테이션은 매우 편리하지만, 적절히 사용하여 코드의 가독성과 유지보수성을 높이는 것이 목적이 되어야한다.


[[Setter 메서드]]
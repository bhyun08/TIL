Getter 메서드는 객체 지향 프로그래밍에서 클래스의 필드 값을 외부에서 읽을 수 있도록 제공하는 메서드이다. 일반적으로 클래스의 필드는 캡슐화(encapsulation)를 통해 외부로부터 직접 접근할 수 없도록 **private**으로 선언된다. 이때 getter 메서드를 사용하면 이러한 필드의 값을 안전하게 읽을 수 있다.

### Getter 메서드의 특징

1. **데이터 캡슐화**: 객체의 필드를 외부에서 직접 접근할 수 없도록 하여 데이터를 보호한다.
2. **읽기 전용**: 필드 값을 반환하지만 수정하지 않는다.
3. **규약**: 일반적으로 메서드 이름은 `get` 접두사와 필드 이름을 결합하여 만든다. 예를 들어, 필드 이름이 `name`이면 getter 메서드 이름은 `getName`이 된다.

### 예제
~~~java
public class Person {
    private String name;
    private int age;

    // 생성자
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Name의 Getter 메소드 
    public String getName() {
        return name;
    }

    // Age의 Getter 메소드
    public int getAge() {
        return age;
    }

    // Main method
    public static void main(String[] args) {
        Person person = new Person("John Doe", 30);
        System.out.println("Name: " + person.getName());
        System.out.println("Age: " + person.getAge());
    }
}
~~~
- 위의 예제에서, `Person` 클래스는 `name`과 `age`라는 두 개의 private 필드를 가지고 있다. 
- `getName`과 `getAge`라는 두 개의 getter 메서드를 통해 이 필드들의 값을 읽을 수 있다.

### Getter 메서드를 사용하는 이유

1. **캡슐화**: 내부 구현 세부 사항을 숨기고 필드의 직접적인 접근을 제한하여 데이터를 보호
2. **유연성**: 필드 값을 반환하기 전에 추가적인 처리를 하거나 변환을 적용
3. **변경 용이성**: 클래스의 내부 구현이 변경되더라도 getter 메서드의 인터페이스를 유지하면 외부 코드에 영향을 주지 않고 변경이 가능
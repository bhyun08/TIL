Setter 메서드는 객체 지향 프로그래밍에서 클래스의 필드 값을 외부에서 수정할 수 있도록 제공하는 메서드이다. Getter 메서드와 마찬가지로, Setter 메서드는 데이터 캡슐화를 유지하면서도 필드의 값을 안전하게 변경할 수 있는 방법을 제공한다.

### Setter 메서드의 특징

1. **데이터 캡슐화**: 객체의 필드를 외부에서 직접 접근할 수 없도록 하여 데이터를 보호한다.
2. **쓰기 가능**: 필드 값을 수정할 수 있다.
3. **규약**: 일반적으로 메서드 이름은 `set` 접두사와 필드 이름을 결합하여 만든다. 예를 들어, 필드 이름이 `name`이면 setter 메서드 이름은 `setName`이 된다.

### 예제
~~~ java
public class Person {
    private String name;
    private int age;

    // 생성자
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Getter for name
    public String getName() {
        return name;
    }

    // Setter for name
    public void setName(String name) {
        this.name = name;
    }

    // Getter for age
    public int getAge() {
        return age;
    }

    // Setter for age
    public void setAge(int age) {
        if (age > 0) {  // Example validation
            this.age = age;
        }
    }

    // Main method 
    public static void main(String[] args) {
        Person person = new Person("John Doe", 30);
        System.out.println("Name: " + person.getName());
        System.out.println("Age: " + person.getAge());

        person.setName("Jane Doe");
        person.setAge(25);
        System.out.println("Updated Name: " + person.getName());
        System.out.println("Updated Age: " + person.getAge());
    }
}
~~~

- 위의 예제에서, `Person` 클래스는 `name`과 `age`라는 두 개의 private 필드를 가지고 있다. 
- `getName`과 `getAge`라는 두 개의 getter 메서드와 `setName`과 `setAge`라는 두 개의 setter 메서드를 통해 이 필드들의 값을 읽고 수정할 수 있다.

### Setter 메서드를 사용하는 이유

1. **캡슐화**: 필드의 직접적인 접근을 제한하고, 필드 값을 변경할 때 추가적인 로직(유효성 검사 등)을 추가할 수 있다.
2. **유연성**: 필드 값을 설정하기 전에 추가적인 처리를 하거나 검증을 수행할 수 있다.
3. **변경 용이성**: 클래스의 내부 구현이 변경되더라도 setter 메서드의 인터페이스를 유지하면 외부 코드에 영향을 주지 않고 변경할 수 있다.
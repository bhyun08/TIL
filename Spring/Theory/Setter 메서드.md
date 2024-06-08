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

도트 연산자(.)란 객체와 클래스에 대한 접근을 제공하는 연산자이다. 도트 연산자는 인스턴스 변수와 메서드를 구분하고, 패키지의 하위 패키지와 클래스에 접근하며, 클래스나 패키지의 멤버에 접근하는 데 사용된다.

### 사용
- 인스턴스 변수와 메서드 구분: "객체변수.필드_명" 또는 "객체변수.메서드_명()"
- 패키지의 하위 패키지와 클래스 접근: "패키지명.하위패키지명.클래스명"
- 클래스나 패키지의 멤버 접근: "클래스명.멤버변수" 또는 "클래스명.메서드명()"
### 예제
1. 객체 생성과 필드, 메서드 접근
	```java
// 클래스 정의
class Person {
    String name;
    int age;

    void introduce() {
        System.out.println("안녕하세요. 제 이름은 " + name + "이고, 나이는 " + age + "살입니다.");
    }
}

// 객체 생성 및 필드/메서드 접근
Person p = new Person();
p.name = "John";
p.age = 30;
p.introduce(); // 출력: 안녕하세요. 제 이름은 John이고, 나이는 30살입니다.
```
- 참조 변수 p를 이용하여 p와 도트연산자를 이용해 Person 클래스의 필드, 메서드에 접근 가능하다.

2. 패키지와 클래스 접근
	```java
// 패키지와 클래스 접근
import java.util.ArrayList;

ArrayList<String> list = new ArrayList<>();
list.add("apple");
list.add("banana");
```
 - import 다음 패키지와 클래스에 접근할때 도트 연산자를 사용한다.

3. 정적 멤버 접근
```java
// 정적 멤버 접근
class Math {
    public static final double PI = 3.14159;

    public static int add(int a, int b) {
        return a + b;
    }
}

double circleArea = Math.PI * 5 * 5;
int sum = Math.add(10, 20);
```
- 도트연산자를 이용하여 static 정적 변수에 접근할 수 있다.
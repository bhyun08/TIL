### extends
extends란 자바에서 클래스 간 상속 관계를 나타내는 문법이다. 하위 클래스는 상위 클래스의 변수와 메서드를 그대로 사용할 수 있다. 상속을 통해 코드의 재사용성이 높아지고 중복을 줄일 수 있다.
##### extends 예제
```java
/ 부모 클래스
class Animal {
    protected String name;
}

// 자식 클래스
class Dog extends Animal {
    public Dog(String name) {
        this.name = name;
    }
}
```
- 부모 클래스 Animal 을 extends 문법을통해 자식클래스 Dog 가 상속받는다.
### implements
implements란 클래스가 인터페이스를 구현할 때 사용된다. 인터페이스에 선언된 메서드는 클래스에서 반드시 오버라이딩해야 한다. 자바는 다중 상속을 지원하지 않지만, 다중 인터페이스는 구현이 가능하다.
##### implements 예제
```java
// 인터페이스
interface Flyable {
    void fly();
}

// 클래스
class Bird implements Flyable {
    @Override
    public void fly() {
        System.out.println("새가 하늘을 납니다.");
    }
}
```
- Flyable 인터페이스를 선언한뒤 추상메서드 fly를 선언하였다.
- 이후 implements 문법을 통해 Bird 클래스가 Flyable 인터페이스를 상속받고, 추상메서드 fly를 오버라이딩해 구연하였다.
### extends VS implements
자바에서는 클래스와 인터페이스간의 관계에 따라서, 상속받을때 사용하는 문법이 다르다.

![](https://i.imgur.com/Y25BbgM.png)

1. 클래스 -> 인터페이스 : 인터페이스가 클래스를 상속받을때
   인터페이스에서 extends 문법을 사용하여 클래스를 상속받는다.
2. 클래스 -> 클래스 : 클래스가 클래스를 상속 받을때
   클래스에서 extends 문법을 사용하여 클래스를 상속받는다.
3. 인터페이스 -> 클래스 : 클래스가 인터페이스를 상속받을때
   클래스에서 implements 문법을 사용하여 인터페이스를 상속받는다.
4. 


[[인터페이스(Interface)]]
[[상속]]
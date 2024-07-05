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

![](https://i.imgur.com/Y25BbgM.png)


[[인터페이스(Interface)]]
[[상속]]
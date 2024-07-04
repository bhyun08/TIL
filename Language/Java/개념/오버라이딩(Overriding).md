오버라이딩(Overriding)은 상속 관계에 있는 클래스에서 부모 클래스의 메소드와 동일한 이름, 리턴 타입, 매개변수 목록을 가지는 메소드를 재정의하는 것을 말한다. 이를 통해 상속받은 메소드의 기능을 변경할 수 있다.    

### 오버라이딩 규칙
1. 메소드 이름, 매개변수 목록, 리턴 타입이 모두 일치해야 한다.
2. 접근 제한자는 부모 클래스의 메소드보다 좁은 범위로 변경할 수 없다.
3. 예외 처리의 경우, 부모 클래스의 메소드보다 더 많은 예외를 던질 수 없다.
### 오버라이딩의 장점
- 상속받은 메소드의 기능을 변경할 수 있어 유연성이 높아집니다.
- 코드의 재사용성이 높아집니다.
- 객체 지향 프로그래밍의 다형성을 구현할 수 있습니다.
### 예제

```java
// 부모 클래스 Animal
public class Animal {
    public void makeSound() {
        System.out.println("동물이 소리를 냅니다.");
    }
}

// 자식 클래스 Dog
public class Dog extends Animal {
    @Override
    public void makeSound() {
        System.out.println("강아지가 멍멍 짖습니다.");
    }
}
```

- Dog 클래스는 Animal 클래스를 상속 받아 `@Override`어노테이션을 통해 `makeSound`메서드를 재정의 하였다.

```java
public class Main {
    public static void main(String[] args) {
        Animal animal = new Animal();
        animal.makeSound(); // 출력: 동물이 소리를 냅니다.

        Dog dog = new Dog();
        dog.makeSound(); // 출력: 강아지가 멍멍 짖습니다.

        Animal animalDog = new Dog();
        animalDog.makeSound(); // 출력: 강아지가 멍멍 짖습니다.
    }
}
```

- `animal.makeSound();`코드에서는 Animal 클래스를 객체로 생성하여 메서드를 호출 하였기 때문에 `makeSound`메서드를 실행한다면 "동물이 소리를 냅니다"가 출력되게 된다.
- `dog.makeSound();`코드에서는 Dog 클래스로 객체를 사용하여 메서드를 호출하기 때문에 `makeSound`메서드를 실행한다면 "강아지가 멍멍 짖습니다"가 출력되게 된다.
- 
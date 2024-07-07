오버로딩(Overloading)이란 하나의 메소드 이름 즉, 하나의 동일한 메서드 이름으로 여러 기능을 구현할 수 있는 기능이다. 메소드 이름이 같고 매개변수의 개수나 타입이 다르면 오버로딩이 가능하다. 오버로딩을 사용하면 같은 기능을 하는 메소드를 하나의 이름으로 사용할 수 있어 상황에 알맞게 사용이 가능하다.
### 오버로딩의 특징
- 오버로딩된 메소드들은 메소드 이름이 같아야 한다.
- 오버로딩된 메소드들은 매개변수의 개수 또는 타입이 달라야 한다.
- 오버로딩된 메소드들의 반환 타입은 영향을 주지 않는다.
- 오버로딩된 메소드 중 어떤 것이 호출될지는 컴파일 시 결정된다.
### 예제

```java
public class DiscountCalculator {
    // 나이를 int로 받는 경우
    public double calculateDiscount(int age) {
        if (age < 20) {
            return 0.1; // 10% 할인
        } else if (age >= 60) {
            return 0.2; // 20% 할인
        } else {
            return 0.0; // 할인 없음
        }
    }

    // 나이를 String으로 받는 경우
    public double calculateDiscount(String age) {
        int ageInt = Integer.parseInt(age);
        if (ageInt < 20) {
            return 0.1; // 10% 할인
        } else if (ageInt >= 60) {
            return 0.2; // 20% 할인
        } else {
            return 0.0; // 할인 없음
        }
    }
```

- 해당 자바 코드는 `calculateDiscount`라는 이름의 메서드를 두가지 선언 하였다.
- 선언된 `calculateDiscount`메서드는 각각 매개변수의 개수는 동일하지만, 매개변수의 타입(자료형)이 다르다.
- 때문에 자바에서는 이를 오버로딩된 코드로 인식하고 메서드를 호출할때 매개변수의 타입(자료형)에 따라서 적절한 메서드를 호출한다.
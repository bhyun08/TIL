메서드는 클래스 내부에 존재하는 영역으로, 특정 기능을 수행하는 코드들의 집합체이다. 메서드는 데이터를 입력받아 처리 과정을 거쳐 결과값을 반환한다. 메서드는 반환 타입, 메서드 이름, 매개변수 타입과 이름, 메서드 바디로 구성된다. 메서드를 실행하려면 호출해야 하며, 호출 시 매개변수를 전달할 수 있다.

### 예시
```java
public class Calculator {
    public int add(int a, int b) { //add 메서드
        return a + b;
    }

    public int subtract(int a, int b) { //subtract 메서드
        return a - b;
    }

    public int multiply(int a, int b) { //multiply 메서드
        return a * b;
    }

    public int divide(int a, int b) { //divide 메서드
        if (b == 0) {
            return 0; // 0으로 나누는 경우 처리
        }
        return a / b;
    }

    public static void main(String[] args) {
        Calculator calc = new Calculator();
        int result1 = calc.add(5, 3); // 메서드 호출
        int result2 = calc.subtract(10, 4);
        int result3 = calc.multiply(2, 6);
        int result4 = calc.divide(15, 3);

        System.out.println("Addition: " + result1);
        System.out.println("Subtraction: " + result2);
        System.out.println("Multiplication: " + result3);
        System.out.println("Division: " + result4);
    }
}
```
이 예제에서는 `Calculator` 클래스에 4개의 메서드(`add`, `subtract`, `multiply`, `divide`)를 정의한다. 각 메서드는 두 개의 정수를 입력받아 해당 연산을 수행하고 결과를 메인 메서드로 반환한다.


- 메서드는 중복 코드를 줄이고 유지보수를 용이하게 하는 등의 목적으로 사용된다. 메서드는 입력값과 출력값이 없을 수도 있으며, 메서드 내부에 선언된 변수는 메서드 작업이 끝나면 소멸되는 지역변수이다.


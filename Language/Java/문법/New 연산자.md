new 연산자는 클래스 타입의 인스턴스(객체)를 생성해주는 역할을 담당한다. new 연산자를 통해 메모리(Heap 영역)에 데이터를 할당하고, 생성자 메서드를 호출하여 객체를 초기화한다. 생성된 객체는 참조 변수를 통해 접근할 수 있다.

![](https://i.imgur.com/SIrBv6a.png)

### Heap 영역에 생성

![](https://i.imgur.com/K0jRezd.png)

Heap 영역 : 사용자가 할당하고, 사용자가 소멸시키는 영역으로, 원하는 순간에 힙 영역에 메모리 공간을 할당 및 소멸할 수 있다. 
### 예제

```java
Person p1 = new Person("Jane", 25);

// 객체의 멤버 접근
System.out.println(p1.getName()); // "Jane"
System.out.println(p1.getAge()); // 25
```

- `Person p1;`은 Person 클래스 타입의 p1 참조 변수를 선언한 것이다. 그 후 new 연산자를 통해서 Person객체를 참조한다.
- 이후 참조 변수를 선언하여 도트(.)연산자를 통해서 멤버에 접근한다.
Hibernate는 **JPA라는 명세의 구현체**이다. 즉,  `EntityManager`와 같은 인터페이스를 직접 구현한 라이브러리이다. **JPA와 Hibernate는 마치 자바의 interface와 해당 interface를 구현한 class와 같은 관계**이다.

![](https://i.imgur.com/Flv4QLt.png)
JPA와 Hibernate의 상속 및 구현 관계를 나타낸 것

JPA의 핵심인 `EntityManagerFactory`, `EntityManager`, `EntityTransaction`을 Hibernate에서는 각각 `SessionFactory`, `Session`, `Transaction`으로 상속받고 각각 `Impl`로 구현하고 있음을 확인할 수 있다.


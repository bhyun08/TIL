Hibernate는 **JPA라는 명세의 구현체**이다. 즉,  `EntityManager`와 같은 인터페이스를 직접 구현한 라이브러리이다. **JPA와 Hibernate는 마치 자바의 interface와 해당 interface를 구현한 class와 같은 관계**이다.

![](https://i.imgur.com/Flv4QLt.png)
JPA와 Hibernate의 상속 및 구현 관계를 나타낸 것

JPA의 핵심인 `EntityManagerFactory`, `EntityManager`, `EntityTransaction`을 Hibernate에서는 각각 `SessionFactory`, `Session`, `Transaction`으로 상속받고 각각 `Impl`로 구현하고 있음을 확인할 수 있다.

“Hibernate는 JPA의 구현체이다”로부터 도출되는 중요한 결론 중 하나는 **JPA를 사용하기 위해서 반드시 Hibernate를 사용할 필요가 없다**는 것이다. Hibernate의 작동 방식이 마음에 들지 않는다면 언제든지 DataNucleus, EclipseLink 등 다른 JPA 구현체를 사용해도 되고, 심지어 본인이 직접 JPA를 구현해서 사용할 수도 있다. 다만 그렇게 하지 않는 이유는 단지 Hibernate가 굉장히 성숙한 라이브러리이기 때문일 뿐이다.

### JPA, Hibernate, Spring Data JPA의 동작 방식

![](https://i.imgur.com/mjTaZjF.png)

빈 스코프(Bean Scope)란 빈이 존재할 수 있는 범위를 의미한다. 스프링은 싱글톤, 프로토타입, 웹 관련 스코프(request, session, application) 등 다양한 스코프를 지원한다.
### 빈 스코프의 종류
1. 싱글톤(singleton)
   - 스프링 컨테이너의 시작과 종료까지 유지되는 가장 넓은 범위의 스코프이다. 기본 스코프 값으로, 의존성 주입을 하면 객체의 기본값은 싱글톤 스코프로 되어있다.
     ![](https://i.imgur.com/6owBY7s.png)
2. 프로토타입(prototype)
   - 매번 새로운 인스턴스를 생성하며, 스프링 컨테이너가 더 이상 관리하지 않는다. 
     ![](https://i.imgur.com/iBdyoW6.png)

3. 웹 관련 스코프
   - Request : HTTP 요청마다 새로운 인스턴스가 생성된다.
   - Session : HTTP 세션마다 새로운 인스턴스가 생성된다.
   - Application : 웹 애플리케이션 수준에서 새로운 인스턴스가 생성된다.

[[빈(Bean)]]
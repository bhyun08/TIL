JDBC(Java Database Connectivity)는 자바 프로그래밍 언어에서 데이터베이스에 접근하기 위한 표준 API이다. JDBC를 사용하면 데이터베이스 독립적인 코드를 작성할 수 있다.
JDBC는 데이터베이스와 연결하고, 쿼리를 실행하며, 데이터 처리, 트랜잭션 관리, 데이터베이스의 메타데이터에 접근 할수 있다.

#### JDBC의 동작 방식

![[JDBC-20240612224454913.webp]]

1. **JDBC 사용**:
    - JPA 구현체(예: Hibernate, Spring Data JPA)는 JDBC API를 사용하여 데이터베이스와 통신한다.
    - JPA는 JDBC 드라이버를 통해 데이터베이스 연결을 생성하고 SQL 쿼리를 실행한다.
	
2. **JDBC 추상화**:
    - JPA는 JDBC 코드의 복잡성을 추상화하여 개발자가 JDBC 코드를 직접 작성할 필요가 없도록 만든다.
    - JPA는 JDBC의 Connection, Statement, ResultSet 등의 객체를 내부적으로 관리한다.
	
3. **JPQL과 SQL 변환**:
    - JPA는 JPQL(Java Persistence Query Language)을 사용하여 쿼리를 작성한다.
    - JPA 구현체는 JPQL을 분석하여 적절한 SQL 쿼리로 변환하고, 이를 JDBC를 통해 실행한다.
    
4. **영속성 관리**:
    - JPA는 영속성 컨텍스트를 통해 엔티티 객체의 상태를 추적하고 관리한다.
    - 이를 통해 JPA는 JDBC의 수동적인 데이터 처리 방식을 자동화하고 최적화할 수 있다.
    
5. **트랜잭션 관리**:
    - JPA는 JDBC의 트랜잭션 관리 기능을 활용하여 데이터 일관성을 보장한다.
    - JPA는 EntityTransaction 인터페이스를 통해 트랜잭션 경계를 설정하고 커밋/롤백을 수행한다.

이와 같이 JPA는 JDBC의 기능을 추상화하고 자동화하여 개발자가 데이터베이스 연동 코드를 직접 작성할 필요 없이 객체 지향적인 방식으로 데이터를 관리할 수 있게 한다.

[[JPA 란]]
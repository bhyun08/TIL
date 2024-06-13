**엔티티 매니저(EntityManager)** 는 JPA 애플리케이션에서 엔티티를 관리하고 데이터베이스와 상호작용하는 주요 인터페이스이다. 엔티티 매니저는 내부에 영속성 컨텍스트(Persistence Context)를 두어서 엔티티들을 관리한다.

![](https://i.imgur.com/rHfRPu4.png)


1. **엔티티 생명 주기 관리**:
    - 엔티티의 상태(새로운 상태, 영속 상태, 분리 상태, 제거 상태 등)를 관리합니다.
    - persist(), merge(), remove(), find() 등의 메서드를 통해 엔티티를 생성, 조회, 수정, 삭제할 수 있습니다.

2. **트랜잭션 관리**:
    - 데이터베이스 트랜잭션을 시작, 커밋, 롤백할 수 있습니다.
    - 트랜잭션 경계 관리를 통해 데이터의 일관성을 보장합니다.

3. **영속성 컨텍스트 관리**:
    - 엔티티 객체를 추적하고 관리하는 영속성 컨텍스트를 관리합니다.
    - 변경 감지, 지연 로딩, 캐싱 등의 기능을 제공합니다.

4. **JPQL 쿼리 실행**:
    - Java Persistence Query Language(JPQL)를 사용하여 엔티티 객체를 대상으로 데이터 조회, 수정, 삭제 작업을 수행할 수 있습니다.

엔티티 매니저는 JPA 구현체(예: Hibernate, EclipseLink)에 의해 제공되며, 애플리케이션 코드에서 주입(Injection)받아 사용한다. 일반적으로 엔티티 매니저는 스프링 프레임워크의 EntityManagerFactory를 통해 생성된다.

#### 엔티티 매니저의 메서드

1. **엔티티 생성 및 삭제**
    - `persist(Object entity)`: 새로운 엔티티 객체를 영속성 컨텍스트에 등록한다.
    - `merge(Object entity)`: 분리된 엔티티 객체를 영속성 컨텍스트에 병합한다.
    - `remove(Object entity)`: 엔티티 객체를 영속성 컨텍스트에서 제거한다.

2. **엔티티 조회**
    - `find(Class<T> entityClass, Object primaryKey)`: 기본 키로 엔티티 객체를 조회한다.
    - `getReference(Class<T> entityClass, Object primaryKey)`: 지연 로딩을 위해 엔티티 참조 객체를 조회한다.

3. **JPQL 쿼리 실행**
    - `createQuery(String jpql)`: JPQL 쿼리를 생성한다.
    - `createNamedQuery(String name)`: 미리 정의된 Named Query를 생성한다.
    - `createNativeQuery(String sql)`: 네이티브 SQL 쿼리를 생성한다.

4. **트랜잭션 관리**
    - `getTransaction()`: 트랜잭션 객체를 반환한다.
    - `begin()`: 트랜잭션을 시작한다.
    - `commit()`: 트랜잭션을 커밋한다.
    - `rollback()`: 트랜잭션을 롤백한다.

5. **기타 메서드**
    - `clear()`: 영속성 컨텍스트를 완전히 비운다.
    - `close()`: 엔티티 매니저를 닫는다.
    - `isOpen()`: 엔티티 매니저가 열려 있는지 확인한다.
    - `flush()`: 영속성 컨텍스트의 변경 내용을 데이터베이스에 동기화한다.

[[BackEnd/Spring/JPA/Entity(엔티티)|Entity(엔티티)]]
JPA에서 엔티티(Entity)는 데이터베이스의 테이블과 매핑되는 객체를 의미한다. 엔티티 클래스는 데이터베이스 테이블의 구조와 일치하도록 정의되며, JPA 구현체는 이 엔티티 클래스를 사용하여 데이터베이스 CRUD(Create, Read, Update, Delete) 작업을 수행한다.

#### 엔티티의 특징

1. **영속성 관리**: 엔티티 객체는 JPA의 영속성 컨텍스트에 의해 관리된다. 이를 통해 변경감지, 지연 로딩 등의 기능이 가능해진다.
    
2. **식별자**: 엔티티 클래스는 반드시 고유한 식별자(Primary Key)를 가져야 한다. 이 식별자는 엔티티의 고유성을 나타낸다.
    
3. **생명 주기**: 엔티티 객체는 새로운 상태, 영속 상태, 분리 상태, 제거 상태 등의 생명 주기를 가진다.
    
4. **매핑 정보**: 엔티티 클래스는 데이터베이스 테이블과의 매핑 정보(테이블 이름, 컬럼 이름 등)를 가지고 있다.
    

#### 예시

```java
@Entity
@Table(name = "MEMBER")
public class Member {

    @Id
    @GeneratedValue
    private Long id;

    @Column(name = "NAME")
    private String name;

    @Column(name = "AGE")
    private int age;

    // Getter, Setter, 생성자 등
}
```

위 코드에서 `@Entity` 어노테이션은 이 클래스가 JPA 엔티티임을 나타내며, `@Table` 어노테이션은 데이터베이스의 MEMBER 테이블과 매핑됨을 의미한다.

- 엔티티는 JPA의 핵심 개념이며, JPA 기반 애플리케이션 개발에 있어 매우 중요한 역할을 한다.
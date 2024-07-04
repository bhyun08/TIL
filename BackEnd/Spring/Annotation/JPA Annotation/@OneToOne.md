`@OneToOne` : 일대일 관계한 엔티티의 인스턴스가 다른 엔티티의 인스턴스 하나와 연결되는 관계를 나타낸다.
### 예시
```java
// 주소 엔티티
@Entity
public class Address {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    private String street;
    private String city;

    @OneToOne(mappedBy = "address")
    private User user;
}

// 사용자 엔티티  
@Entity 
public class User {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    private String name;

    @OneToOne
    @JoinColumn(name = "address_id")
    private Address address;
}
```

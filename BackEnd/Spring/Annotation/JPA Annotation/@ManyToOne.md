`@ManyToOne` : 여러 엔티티의 인스턴스가 다른 엔티티의 인스턴스 하나와 연결되는 관계를 나타낸다.

### 예시
~~~java
// 주문 엔티티
@Entity
public class Order {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    private String orderNumber;

    @ManyToOne
    @JoinColumn(name = "customer_id")
    private Customer customer;
}

// 고객 엔티티
@Entity
public class Customer {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    private String name;

    @OneToMany(mappedBy = "customer")
    private List<Order> orders = new ArrayList<>();
}
~~~


`@OneToMany` : 한 엔티티의 인스턴스가 다른 엔티티의 여러 인스턴스와 연결되는 관계를 나타낸다.

### 예시
```java
// 게시글 엔티티
@Entity
public class Post {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    private String title;
    private String content;

    @ManyToOne
    @JoinColumn(name = "user_id")
    private User user;
}

// 사용자 엔티티
@Entity
public class User {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    private String name;

    @OneToMany(mappedBy = "user")
    private List<Post> posts = new ArrayList<>();
}
```
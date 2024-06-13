JPQL 쿼리의 기본 문법은 다음과 같다:

- SELECT 절
- FROM 절
- WHERE 절
- GROUP BY 절
- HAVING 절
- ORDER BY 절

1. **SELECT 절**
    - 조회할 대상 엔티티와 속성을 명시한다.
    - 예시: `SELECT m FROM Member m`
    
2. **FROM 절**
    - 조회 대상이 되는 엔티티 클래스를 명시한다.
    - 예시: `FROM Member m`
    
3. **WHERE 절**
    - 조회 결과를 필터링하기 위한 조건을 명시한다.
    - 예시: `WHERE m.age > 20`
    
4. **GROUP BY 절**
    - 엔티티 속성을 기준으로 그룹화한다.
    - 예시: `GROUP BY m.department`
    
5. **HAVING 절**
    - GROUP BY 절에 의해 생성된 그룹에 대한 조건을 명시한다.
    - 예시: `HAVING COUNT(m) > 10`
    
6. **ORDER BY 절**
    - 조회 결과를 정렬한다.
    - 예시: `ORDER BY m.name DESC`

#### 사용예시
~~~java
// 엔티티 매니저 주입
@PersistenceContext
private EntityManager em;

// JPQL 쿼리 실행
List<Member> members = em.createQuery("SELECT m FROM Member m WHERE m.age > 20", Member.class)
                         .getResultList();
~~~
위 코드에서는 `em.createQuery()` 메서드를 사용하여 JPQL 쿼리를 실행하고, 그 결과를 `Member` 엔티티 목록으로 받아오는 코드이다.

---
JPQL에는 다양한 함수와 연산자도 지원한다:
- 함수: `SIZE()`, `LENGTH()`, `CONCAT()`, `ABS()` 등
- 연산자: `=`, `>`, `<`, `BETWEEN`, `LIKE`, `IN` 등

또한 JPQL은 엔티티 간 관계를 표현할 수 있는 기능도 제공한다:
- 연관 관계 탐색: `m.team`, `m.orders`
- 컬렉션 함수: `SIZE()`, `ELEMENT()`, `INDEX()` 등

[[JPQL]]
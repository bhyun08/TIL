JPQL 쿼리의 기본 문법은 다음과 같다:

- SELECT 절
- FROM 절
- WHERE 절
- GROUP BY 절
- HAVING 절
- ORDER BY 절

1. **SELECT 절**
    - 조회할 대상 엔티티와 속성을 명시합니다.
    - 예시: `SELECT m FROM Member m`
    
2. **FROM 절**
    - 조회 대상이 되는 엔티티 클래스를 명시합니다.
    - 예시: `FROM Member m`
    
3. **WHERE 절**
    - 조회 결과를 필터링하기 위한 조건을 명시합니다.
    - 예시: `WHERE m.age > 20`
    
4. **GROUP BY 절**
    - 엔티티 속성을 기준으로 그룹화합니다.
    - 예시: `GROUP BY m.department`
5. **HAVING 절**
    - GROUP BY 절에 의해 생성된 그룹에 대한 조건을 명시합니다.
    - 예시: `HAVING COUNT(m) > 10`
6. **ORDER BY 절**
    - 조회 결과를 정렬합니다.
    - 예시: `ORDER BY m.name DESC`
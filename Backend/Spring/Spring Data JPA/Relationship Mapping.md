Relationship Mapping mean way that express database table's relationship object-oriented. Namely, in database, table's relationship mapping to JPA entity class relationship, to use object to do database work easily.
# Unidirectional vs Bidirectional
Unidirectional and Bidirectional is entity reference relationship. 
### Unidirectional
Unidirectional is reference relationship that only one side entity reference other side entity. In this relationship, entity that is referenced to can't know other side entity.
### Bidirectional
Bidirectional is reference relationship that reference entities each other. In this relationship, entities can know each entity.
# Owner of the Relationship
Owner of the Relationship mean entity that manage **FK(Foreign Key)**. 

In unidirectional relationship, owner of the relationship is always entity that reference other entity. But, in bidirectional relationship, because the two entities refer to each other, you must decide which side manages the foreign keys, which are called "owners of the relationship."
## @JoinColumn
`@JoinColumn` is used to owner of the relationship. Specifies how to map the foreign key to which column.
## mappedBy
`mappedBy` is used to the foreign key on the non-managing side, and specify the field name of the entity being the owner. 

**Example**
```java
@Entity
public class Company {
    @OneToMany(mappedBy = "company")  // Owner is Employee
    private List<Employee> employees;
}

@Entity
public class Employee {
    @ManyToOne
    @JoinColumn(name = "company_id") // company_id get as field
    private Company company;
}
```
# Case of Relationship
### One-to-One
One-to-One use when one entity is mapped `1:1` to another.
### One-to-Many
One-to-Many use when one entity mapped with multiple entities.
### Many-to-One
Many-to-One use when multiple entities mapped with one entity.
### Many-to-Many
Many-to-Many use when multiple entities mapped with multiple entities.

---
Reference link 🙂     
https://jeong-pro.tistory.com/231          
https://stackabuse.com/a-guide-to-jpa-with-hibernate-relationship-mapping/          
https://velog.io/@knavoid/Spring-Data-JPA-Relationship-Mapping             
https://www.baeldung.com/jpa-hibernate-associations            
Normalization is a principle that in database design, reduce database's redundancy and guarantee data integrity. Database normalization is worked by split the data into several smaller tables, and define the relationship between these tables.
# Normalization level
![](https://guides.visual-paradigm.com/wp-content/uploads/2023/09/img_6503eac4b1cdf.png)           
Normalization is divided step by step, and as the step increases, the normalization condition of the lower step is satisfied, and the degree of normalization becomes severe.
## 1NF(First Normal Form)
All fields must have atomic values (no more divisible values), which means that a field must not contain multiple values. 
## 2NF(Second Normal Form)
All non-primary properties must be completely functional dependent on the primary key, i.e., remove partial functional dependencies of all properties in the table. This applies only when the default key is a composite key. 

For example, In a table with the default key (`A, B`), if the attribute `C` is dependent on A only and independent of `B`, then `C` has partial dependency. In this case, move `C` to a separate table with respect to `A`.
## 3NF(Third Normal Form)
Non-primary attributes must not be dependent on other non-primary attributes. That is, all attributes must be directly dependent on the default key. (Remove function dependencies that move rows)
## BCNF(Boyce-Codd Normal Form)
Rules for all deciders to be candidate keys. Deciders (attributes that can determine other things) must be candidate keys unconditionally.
## 4NF(Fourth Normal Form)
Store data more efficiently by eliminating multi-value dependencies. Multi-value dependency is an situation that an attribute can have multiple values independently for a particular value. In this way, you can reduce data redundancy.
## 5NF(Fifth Normal Form)
Removing join dependencies to make the relationship between tables neat. Join dependency is a relationships that allow accurate restoration of the original data by splitting the data into multiple tables and then rejoining.

---
Reference link 🙂          
https://superohinsung.tistory.com/111          
https://www.datacamp.com/tutorial/normalization-in-sql
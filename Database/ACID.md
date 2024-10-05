ACID is an acronym that refers to the set of 4 key properties that define a transaction: **Atomicity, Consistency, Isolation,** and **Durability.**  Transaction's works is working normally as follow this properties. 
![](https://www.databricks.com/sites/default/files/inline-images/delta-lake-1-min.png?v=1702063468)             
### ATOMICITY
Atomicity guarantee the transaction work have to "Success all" or "Fail all". Transaction guarantee atomicity through `COMMIT` and `ROLLBACK`.
### CONSISTENCY
When a transaction is successfully completed, the database must always remain consistent.
### ISOLATION
![](https://oopy.lazyrockets.com/api/v2/notion/image?src=https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2Fba383863-486f-4ed8-90d7-88cda9a55121%2FScreen_Shot_2021-02-24_at_3.34.18.png&blockId=77b61993-dd3d-404c-bafd-3f67f5e10c0d)          
One transaction can never interfere with another. That is, the transaction is executed independently. However, this varies slightly from system to system, depending on the level of isolation.
### DURABILITY
After the transaction is complete, the results of the transaction must be permanently stored even if the system fails or a problem occurs.

---
Reference link 🙂           
https://www.databricks.com/glossary/acid-transactions#:~:text=properties%3A%20Atomicity%2C%20Consistency%2C%20Isolation,Consistency%2C%20Isolation%2C%20and%20Durability        
https://blog.yevgnenll.me/posts/what-is-acid-about-transaction       

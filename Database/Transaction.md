In database, transaction mean of one unit of database's work. When change database's status, changing work all must be successfully completed, or cancelled (rollback) altogether. To do this, grouping multiple database operations (e.g., `INSERT`, `UPDATE`, `DELETE`) together and treating them as a single unit is called a transaction.

If you want work as transaction, you have to use `BEGIN TRANSACTION;` or `START TRANSACTION;`.
# How to work transaction?
To process a transaction, transaction has a life cycle.
![](https://images.contentful.com/po4qc9xpmpuh/6jbcyfzdVJlc6XCUbzgMzb/96b1a9f0594f1d769f2254bd1abf25c1/database-transaction-1__1_.png)
1. Transaction becomes active to perform the corresponding command (read or write operation).
2. Partially committed state, changes have been made in this state, but the database has not yet committed changes on disk. Data is stored in memory buffer, and the buffer has not yet been written to disk.
3. If the transaction fails, or if it is suspended in the active or partially committed state, it fails.
4. Commit, in this state, if transaction did not fail, all transaction updates are permanently stored in the database; therefore, transactions cannot be rolled back after this point.
5. When end all of transaction's work, transaction life cycle is end.

---
Reference link 🙂           
https://blog.toktokhan.dev/트랜잭션-이란-무엇인가-986d40d112ac          
https://fauna.com/blog/database-transaction           
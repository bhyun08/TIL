JDBC is an abbreviation of **Java Database Connectivity**. JDBC is a Java API that stores and updates data from Java-based applications in a database, or allows data stored in the database to be used in Java. As a result, jdbc sends a query to db to manipulate it.
# JDBC Driver
![](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*TMMxD1I9wHjzvTWl)
JDBC's architect is divide JDBC API and JDBC Driver.

JDBC Driver is be in charge of dispatching with the database. Provide the correct JDBC driver for databases such as Oracle, MS SQL, MySQL, and more.
# JDBC work flow
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FwTyMC%2FbtrR5yww0DA%2Fjwst72s4xtTKhLTtzfJ0mK%2Fimg.png)
JDBC is worked by this work flow.       
1. Correct JDBC loading, JDBC Driver is loaded by `DriverManager` Class.
2. Connection object create, a `Connection` class is created, which is a session for connecting the database to the JDBC driver.
3. Statement object loading, for SQL query run.
4. Query run, Execute the input SQL query using the `Statement` object.
5. Data inquiry, Query result data for executed SQL query statements from the `ResultSet` object
6. Object close, Objects used through the JDBC API are closed in the reverse order of using the created objects.
# Connection Pool
Creating a Connection object to connect to a database using the JDBC API is one of the costly tasks.
####  Connection Object Creating Process
1. Application check it out the connection through the DB driver.
2. DB driver connects DB and TCP/IP connection. (Network connection operation such as 3-way-handshake occurs)
3. When the TCP/IP connection is connected, the DB driver delivers ID, password, and other additional information to the DB.
4. DB creates a DB inside after internal authentication through ID and password.
5. DB sends a response that the connection creation is complete.
6. DB driver creates a connection object and returns it to the client.
Namely, every time an application accesses a database, a new connection must be created.

So, Connection Pool creates and stores Connection objects in advance, and manages applications to be taken out and used when necessary.
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbJrVSk%2FbtrRZOhiAim%2FieG4YLJvw4TcH6IvAuk8Ok%2Fimg.png)
#### Connection Pool Process
1. At the start of the application, the connection pool creates and stores connections in advance as necessary.
2. The number of connection objects created is different depending on the characteristics and specifications of the service, but in general, 10 are created as default values.
3. Since the connection object in the connection pool is connected to the DB through TCP/IP, SQL may be delivered to the DB immediately.
4. It is used by referring to an already created connection rather than acquiring a new connection through a DB driver.
5. When a connection in the connection pool is requested, the connection pool returns one of its connection objects.

---
Reference link 🙂   
https://medium.com/@Bharat2044/what-is-jdbc-introduction-to-java-database-connectivity-649677818a8b
https://ittrue.tistory.com/250
# Database Fundamentals – Conceptual Understanding

## 1. Why is db.json not suitable as a database for real projects?

A `db.json` file is a simple file-based storage mechanism and is not suitable for real-world applications.

### Limitations of file-based storage:

**Performance:**  
- The entire file often needs to be read and written for small changes.
- Becomes slow as data size increases.

**Scalability:**  
- Cannot efficiently handle large datasets.
- Not suitable for multiple users or high traffic applications.

**Reliability:**  
- High risk of data corruption if the process crashes during a write operation.
- No built-in backup, recovery, or transaction support.

**Concurrency Issues:**  
- Multiple users accessing or modifying the file at the same time can cause conflicts.
- No locking or concurrency control.

Because of these limitations, `db.json` is only suitable for learning, testing, or small mock projects.

---

## 2. What are the ideal characteristics of a database system (apart from just storage)?

An ideal database system provides much more than just storing data.

### Key Characteristics:

**Performance:**  
- Fast data retrieval and efficient query execution.
- Optimized indexing and caching mechanisms.

**Concurrency:**  
- Supports multiple users accessing data simultaneously.
- Ensures consistency even when many operations occur at the same time.

**Reliability:**  
- Ensures data is always available and safe.
- Protects data from crashes, power failures, or system errors.

**Data Integrity:**  
- Maintains accuracy and consistency of data.
- Enforces rules such as primary keys, foreign keys, and constraints.

**Scalability:**  
- Can handle increasing amounts of data and users.
- Supports vertical and horizontal scaling.

**Fault Tolerance:**  
- Can recover automatically from failures.
- Uses replication and backup mechanisms.

---

## 3. How many types of databases are there? What are their use cases or applications?

Databases are mainly categorized into **Relational** and **Non-Relational (NoSQL)** databases.

### 1. Relational Databases (SQL)

**Description:**  
- Store data in tables with rows and columns.
- Use structured schemas and SQL for queries.

**Examples:**  
- MySQL  
- PostgreSQL  
- Oracle  
- SQL Server  

**Use Cases:**  
- Banking and financial systems  
- E-commerce applications  
- Inventory management  
- Applications requiring complex queries and transactions  

---

### 2. Non-Relational Databases (NoSQL)

**Description:**  
- Store data in formats like documents, key-value pairs, graphs, or columns.
- Schema-less or flexible schema design.

**Examples:**  
- MongoDB (Document-based)  
- Redis (Key-value)  
- Cassandra (Column-based)  
- Neo4j (Graph-based)  

**Use Cases:**  
- Social media applications  
- Real-time analytics  
- Big data and distributed systems  
- Applications with rapidly changing data structures  

---

## Conclusion

Relational databases are best suited for structured data and transactional systems, while NoSQL databases are ideal for scalability, flexibility, and high-performance distributed applications.

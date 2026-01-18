Below is a **ready-to-use `answer.md` content** that you can directly copy into a Markdown file, commit, and push to GitHub.
I’ve written it in an **assignment-friendly, detailed, and clear format**, with **e-commerce examples** and **diagram references**.

---

# Database Relationships

## 1. Definition of Database Relationship

A **database relationship** defines how two or more tables in a database are logically connected to each other.
These relationships are created using **primary keys** and **foreign keys** to maintain **data integrity**, **reduce redundancy**, and enable efficient data retrieval.

In real-world applications like **e-commerce systems**, relationships help connect customers, orders, products, payments, and deliveries in a structured way.

---

## 2. Types of Database Relationships

There are **three main types of database relationships**:

1. One-to-One (1:1)
2. One-to-Many (1:N)
3. Many-to-Many (M:N)

Each type is explained below with **clear e-commerce examples**.

---

## 3. One-to-One Relationship (1:1)

### Explanation

In a **one-to-one relationship**, each record in Table A is related to **only one** record in Table B, and vice versa.

This type of relationship is usually used when:

* Data is split for **security**
* Data is split for **better organization**

### E-commerce Example

**User ↔ UserProfile**

* One user has only one profile
* One profile belongs to only one user

**Tables:**

* `Users (user_id, email, password)`
* `UserProfile (profile_id, user_id, address, phone)`

Here, `user_id` is a **foreign key** in `UserProfile`.

![Image](https://support.microsoft.com/images/en-us/9e935295-f8bb-4fce-8ad3-1eddeb37f988)

![Image](https://www.beekeeperstudio.io/assets/img/database-relationships/one-to-one-59751b752058a5d378adc3a9a5ab4f1a7c0b7f2a1bede234aa9a8c2bfb91ee41f7c6c06208d7ae7a00257965313f9a0031578bb8e46bc5d5cbbcded30d5fc454.svg)

---

## 4. One-to-Many Relationship (1:N)

### Explanation

In a **one-to-many relationship**, one record in Table A can be associated with **multiple records** in Table B, but each record in Table B is associated with **only one** record in Table A.

This is the **most common relationship** in databases.

### E-commerce Example

**Customer ↔ Orders**

* One customer can place **many orders**
* Each order belongs to **one customer**

**Tables:**

* `Customers (customer_id, name, email)`
* `Orders (order_id, customer_id, order_date, total_amount)`

Here, `customer_id` is a **foreign key** in `Orders`.

![Image](https://images.ctfassets.net/w6r2i5d8q73s/QDa5oq16N1ifmlWC6Dnu2/a52db5fdedc3e933c865bbd3575e903b/technical_diagramming_01_database_diagram_product_image_EN_standard_4_3_2x.png?fm=webp\&q=75)

![Image](https://www.beekeeperstudio.io/assets/img/database-relationships/one-to-many-b1aa868f0a89fde8f4a4802df798d5dd065d946a0369ab9161c50452311e3c67e6be54379b96d7569c723572525c48b503b6437a237b8e596180e945459b7c61.svg)

---

## 5. Many-to-Many Relationship (M:N)

### Explanation

In a **many-to-many relationship**, multiple records in Table A are related to multiple records in Table B.

This relationship **cannot be implemented directly** and requires a **junction (bridge) table**.

### E-commerce Example

**Orders ↔ Products**

* One order can contain **many products**
* One product can appear in **many orders**

**Tables:**

* `Orders (order_id, customer_id)`
* `Products (product_id, product_name, price)`
* `Order_Items (order_id, product_id, quantity)`

`Order_Items` acts as the **junction table** and contains foreign keys from both tables.

![Image](https://images.ctfassets.net/w6r2i5d8q73s/QDa5oq16N1ifmlWC6Dnu2/a52db5fdedc3e933c865bbd3575e903b/technical_diagramming_01_database_diagram_product_image_EN_standard_4_3_2x.png?fm=webp\&q=75)

![Image](https://global.discourse-cdn.com/sitepoint/optimized/3X/e/a/ea94fbd4e1e8730455bb4fa266a22f423065b43a_2_760x1024.png)

---

## 6. Summary Table

| Relationship Type | Description                         | E-commerce Example |
| ----------------- | ----------------------------------- | ------------------ |
| One-to-One        | One record linked to one record     | User ↔ UserProfile |
| One-to-Many       | One record linked to many records   | Customer ↔ Orders  |
| Many-to-Many      | Many records linked to many records | Orders ↔ Products  |

---

## 7. Conclusion

Database relationships are essential for designing **scalable and efficient e-commerce applications**.
By correctly implementing one-to-one, one-to-many, and many-to-many relationships, developers ensure:

* Accurate data storage
* Better performance
* Easier maintenance
* Real-world data consistency

Understanding these relationships is fundamental for backend development and database design.

---


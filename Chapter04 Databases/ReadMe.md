

# **Chapter 4 — Databases (Quick Revision Sheet)**

---

## **1) What is a Database?**

**Definition:**
A **database** is an organized system for storing, retrieving, and managing data efficiently. Unlike simple files (like CSV), databases support querying, indexing, transactions, and concurrency.

**Role in Preprocessing:**

* Databases are often the **source of data**
* They store large real-world datasets used for analytics and preprocessing
* Preprocessing usually begins with **extracting data** from databases before cleaning and transforming it

⚡ *Key idea:*
Databases are not for deep analytics themselves, but they are where **raw data lives** before preprocessing or analytics.

---

##  **2) Why Databases Matter in Data Preprocessing**

| Benefit               | Explanation                                         |
| --------------------- | --------------------------------------------------- |
| **Efficient storage** | Handles large data more effectively than flat files |
| **Structured access** | SQL lets you query only the data you need           |
| **Scalability**       | Can handle millions or billions of records          |
| **Consistency**       | Data integrity through transactions                 |

In analytics workflows:

1. Connect to database
2. Fetch *relevant subsets*
3. Load into Pandas/DataFrame
4. Then preprocess (clean, transform, reduce, etc.)

---

## **3) Types of Databases**

| Type                             | Description                               | Common Use                 |
| -------------------------------- | ----------------------------------------- | -------------------------- |
| **Relational Databases (RDBMS)** | Data in tables with relationships         | MySQL, PostgreSQL, SQLite  |
| **NoSQL Databases**              | Flexible, unstructured or semi-structured | MongoDB, Cassandra         |
| **Columnar Databases**           | Optimized for analytics                   | Apache Cassandra, BigQuery |
| **Cloud Databases**              | Managed solutions                         | AWS RDS, Azure SQL         |

**Relational DBs** are the most relevant for data preprocessing — they use SQL and support structured queries. 

---

## **4) How to Connect & Pull Data (General Concepts)**

To preprocess data in Python, you usually:

### 🔹 **A) Use Database Connectors**

* For SQL databases:

  * `sqlite3` (Python built-in)
  * `psycopg2` (PostgreSQL)
  * `mysql-connector` (MySQL)

### 🔹 **B) Send SQL Queries**

You can fetch exactly what you need instead of entire tables — helps performance.

```python
import sqlite3
import pandas as pd

conn = sqlite3.connect("mydb.db")
query = "SELECT * FROM customers WHERE age > 30"
df = pd.read_sql_query(query, conn)
```



##  **5) Pulling Data Efficiently**

| Principle                      | Why it matters                     |
| ------------------------------ | ---------------------------------- |
| **Filter at source**           | Reduces amount of data transferred |
| **Select only needed columns** | Saves memory                       |
| **Paginate large results**     | Avoids overload                    |
| **Indexing in DB**             | Speeds up queries                  |

---

##  **6) Databases vs. Flat Files (e.g., CSV)**

| Aspect      | Databases            | CSV/Excel                   |
| ----------- | -------------------- | --------------------------- |
| Data size   | Handles huge volumes | Can be slow for large files |
| Querying    | SQL queries          | Must load entire file       |
| Concurrency | Support              | Not supported               |
| Integrity   | ACID transactions    | No                          |

---

##  **7) When to Extract Data from DB?**

* **Before cleaning:** Pull raw columns you need
* **Before integration:** Join tables via SQL
* **Before sampling:** Let DB handle sampling with SQL
* **Before preprocessing:** Bring data into pandas DataFrame



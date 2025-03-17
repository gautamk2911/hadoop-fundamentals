# Introduction to Hadoop

## 1. Overview of Big Data
Big Data refers to extremely large datasets that are difficult to process using traditional data processing techniques. It is characterized by the **5 Vs**:

- **Volume**: Massive amounts of data generated every second.
- **Velocity**: High-speed data generation and processing.
- **Variety**: Different formats like structured, semi-structured, and unstructured data.
- **Veracity**: Ensuring data quality and reliability.
- **Value**: Extracting meaningful insights from data.

Big Data is used in **healthcare, finance, social media, e-commerce, IoT**, and many other industries.

---

## 2. Introduction to Hadoop
Hadoop is an **open-source framework** designed for processing and storing Big Data efficiently. It allows distributed storage and parallel processing of large datasets across multiple machines.

### **Key Features of Hadoop:**
✔ **Scalability**: Can handle petabytes of data by adding more machines.
✔ **Fault Tolerance**: Replicates data to prevent data loss in case of failures.
✔ **Cost-effective**: Uses commodity hardware instead of expensive servers.
✔ **Flexibility**: Supports structured, semi-structured, and unstructured data.
✔ **Parallel Processing**: Uses a distributed approach to process data faster.

---

## 3. Components of Hadoop
Hadoop consists of four main components:

### **1. Hadoop Distributed File System (HDFS)**
- Distributed storage system that splits large files into blocks.
- Stores data across multiple machines with replication for fault tolerance.
- Commands: `put`, `get`, `ls`, `mkdir`, `rm`, etc.

### **2. MapReduce**
- Programming model for parallel data processing.
- **Mapper**: Processes input data and generates key-value pairs.
- **Reducer**: Aggregates and processes the output from the mapper.
- Example: WordCount program to count word occurrences in a file.

### **3. YARN (Yet Another Resource Negotiator)**
- Manages and allocates resources across Hadoop clusters.
- Separates resource management from data processing.
- Improves efficiency and scalability over Hadoop v1.

### **4. Hadoop Common**
- Set of shared utilities and libraries required by Hadoop components.
- Provides essential Java-based tools for system operation.

---

## 4. Hadoop Ecosystem (Beyond Core Hadoop)
Hadoop integrates with various tools for data analysis and management:

| Tool | Description |
|------|-------------|
| **Apache Hive** | Data warehousing and SQL-like querying |
| **Apache HBase** | NoSQL database for real-time data access |
| **Apache Pig** | Scripting language for data transformation |
| **Apache Spark** | Faster in-memory data processing |
| **Apache Sqoop** | Transfers data between Hadoop and RDBMS |
| **Apache Flume** | Collects and aggregates log data |

---

## 5. Why Use Hadoop?
✔ Handles massive datasets with ease.
✔ Open-source and widely adopted.
✔ Compatible with cloud platforms (AWS, Azure, GCP).
✔ Provides fault tolerance, scalability, and cost-efficiency.

Hadoop is a **cornerstone of Big Data processing**, enabling organizations to **store, process, and analyze** large datasets efficiently.

---

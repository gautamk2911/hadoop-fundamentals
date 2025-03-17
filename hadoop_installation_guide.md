# Hadoop Installation Guide

## **1. System Requirements**
Before installing Hadoop, ensure your system meets the following requirements:

- **Operating System**: Windows 10/11 (with WSL or native installation)
- **RAM**: Minimum 4GB (8GB recommended for smooth operation)
- **Java**: OpenJDK 8 or later
- **SSH**: Required for Hadoop daemons (configured manually on Windows)
- **Storage**: At least 10GB of free disk space

---

## **2. Installing Hadoop on Windows**

### **Step 1: Install Java**
1. Download Java JDK 8 or later from [Oracle Java Downloads](https://www.oracle.com/java/technologies/javase-downloads.html).
2. Install Java and set environment variables:
   - Go to **Control Panel → System → Advanced system settings**.
   - Click **Environment Variables**.
   - Under **System Variables**, click **New**, and set:
     - **Variable Name**: `JAVA_HOME`
     - **Variable Value**: Path to JDK installation (e.g., `C:\Program Files\Java\jdk1.8.0_321`)
   - Edit the **Path** variable and add `%JAVA_HOME%\bin`.
   - Verify installation:
     ```cmd
     java -version
     ```

### **Step 2: Download and Extract Hadoop**
1. Download Hadoop from [https://hadoop.apache.org/releases.html](https://hadoop.apache.org/releases.html).
2. Extract the Hadoop folder to `C:\hadoop`.
3. Set environment variables:
   - Add a new system variable:
     - **Variable Name**: `HADOOP_HOME`
     - **Variable Value**: `C:\hadoop`
   - Add `%HADOOP_HOME%\bin` and `%HADOOP_HOME%\sbin` to the **Path** variable.

### **Step 3: Configure Hadoop**
1. Open `C:\hadoop\etc\hadoop\core-site.xml` and add:
   ```xml
   <configuration>
     <property>
       <name>fs.defaultFS</name>
       <value>hdfs://localhost:9000</value>
     </property>
   </configuration>
   ```
2. Open `C:\hadoop\etc\hadoop\hdfs-site.xml` and add:
   ```xml
   <configuration>
     <property>
       <name>dfs.replication</name>
       <value>1</value>
     </property>
   </configuration>
   ```
3. Edit `C:\hadoop\etc\hadoop\hadoop-env.cmd` and set:
   ```cmd
   set JAVA_HOME=C:\Program Files\Java\jdk1.8.0_321
   ```

### **Step 4: Format HDFS and Start Hadoop**
```cmd
hdfs namenode -format
start-dfs.cmd
start-yarn.cmd
jps  # Check running daemons
```

---

## **3. Verifying Hadoop Installation**
- Open the web UI: [http://localhost:9870/](http://localhost:9870/) (HDFS NameNode UI)
- Check running processes with `jps`

---

## **4. Additional Resources**
- Apache Hadoop Official Docs: [https://hadoop.apache.org/](https://hadoop.apache.org/)
- Video Tutorial: [https://www.youtube.com/watch?v=impAw8c5J8w](https://www.youtube.com/watch?v=impAw8c5J8w)
- Hadoop GitHub Repo: [https://github.com/apache/hadoop](https://github.com/apache/hadoop)

This guide provides a complete setup for **Hadoop installation on Windows**.


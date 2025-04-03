# HDFS Commands Cheat Sheet

## 1. Basic File System Commands
These commands allow interaction with the Hadoop Distributed File System (HDFS).

| Command | Description |
|---------|-------------|
| `hdfs dfs -ls /path` | Lists files and directories in HDFS |
| `hdfs dfs -mkdir /path` | Creates a new directory in HDFS |
| `hdfs dfs -rmdir /path` | Removes an **empty** directory |
| `hdfs dfs -rm -r /path` | Deletes a **non-empty** directory recursively |
| `hdfs dfs -mv /source /dest` | Moves a file or directory |
| `hdfs dfs -cp /source /dest` | Copies a file or directory |

---

## 2. File Operations
| Command | Description |
|---------|-------------|
| `hdfs dfs -touchz /file` | Creates an empty file in HDFS |
| `hdfs dfs -put localfile /path` | Uploads a file from the local system to HDFS |
| `hdfs dfs -copyFromLocal localfile /path` | Similar to `put`, copies a local file to HDFS |
| `hdfs dfs -get /file localfile` | Downloads an HDFS file to the local system |
| `hdfs dfs -copyToLocal /file localfile` | Similar to `get`, copies an HDFS file to local |

---

## 3. Reading & Writing Files
| Command | Description |
|---------|-------------|
| `hdfs dfs -cat /file` | Displays the contents of an HDFS file |
| `hdfs dfs -tail /file` | Shows the last part of an HDFS file |
| `hdfs dfs -text /file` | Converts non-text files (like SequenceFiles) into readable format |
| `hdfs dfs -head /file` | Displays the first few lines of a file |

---

## 4. Appending & Modifying Files
| Command | Description |
|---------|-------------|
| `hdfs dfs -appendToFile localfile /hdfsfile` | Appends local file content to an HDFS file |
| `hdfs dfs -setrep -w 3 /file` | Changes the replication factor of a file |
| `hdfs dfs -chmod 755 /file` | Changes file permissions |
| `hdfs dfs -chown user:group /file` | Changes file ownership |

---

## 5. Checking File System Information
| Command | Description |
|---------|-------------|
| `hdfs dfs -du -s -h /path` | Displays disk usage summary |
| `hdfs dfs -df -h` | Shows available HDFS disk space |
| `hdfs dfs -count -q /path` | Displays the number of directories, files, and disk space usage |


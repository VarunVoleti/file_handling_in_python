# 📂 Python File Handling & OS Operations
## 📌 Project Overview

This repository demonstrates practical implementation of File Handling in Python, including:

Reading files
Writing files
Appending content
Exception handling (try-except-finally)
Context managers
Working with CSV & JSON
Creating folders
Copying and moving files
Using built-in os, shutil, and json modules

This project strengthens foundational Python skills required for automation, scripting, and data engineering workflows.

## 🧠 Core Concepts Covered
### 🔹 1️⃣ Opening, Reading & Closing Files
```
read_file = open('fake_file.txt','r')
print(read_file.read())
read_file.close()
```

### Key Learning:

'r' mode → Read
'w' mode → Write (overwrites)
Always close files to free system resources

### 🔹 2️⃣ Writing to Files
```
write_file = open('fake_file.txt','w')
write_file.write('hello hi')
write_file.close()
```

✔ 'w' mode replaces existing content
✔ Used for updating or generating new files

### 🔹 3️⃣ Exception Handling with File Operations
```
try:
    read_file.write('Hey!!')
except Exception as e:
    print(e)
finally:
    read_file.close()
```

### Why This Matters:

Prevents program crashes
Handles runtime errors safely
Ensures file is always closed

### 🔹 4️⃣ Context Manager (Best Practice)
```
with open('fake_file.txt','w') as file:
    file.write('I am using context manager')
```

### Benefits:

✔ Automatically closes file
✔ Cleaner & safer code
✔ Industry-standard approach

### ✍ Writing & Appending Files
**Writing:**
```
with open('new_file.txt','w') as file:
    file.write('This is 1st sentence')
```
**Appending:**
```
with open('new_file.txt','a') as file:
    file.write('\nThis is an appended sentence')
```

✔ 'a' mode adds content without overwriting
✔ Useful for logs & incremental updates

### 📄 Working with CSV Files
```
with open('csv_file.csv','a') as file:
    file.write('\n data, 2 data, 3 data')
```

✔ Demonstrates structured data writing
✔ Foundation for data analytics workflows

### 🗂 Working with JSON Files
```
import json

data = [['var', 'student', 25], ['par', 'clerk', 23]]

with open('csv_file.json','w') as file:
    json.dump(data, file)
```
### Why JSON?

Common data exchange format
Used in APIs
Used in data engineering pipelines

### 📁 Creating Folders Using os
```
import os
os.mkdir('Example_folder')
```

### Checking before creating:
```
if os.path.exists('Example_folder'):
    os.mkdir('Example_folder2')
```

✔ Prevents duplicate folder errors
✔ Useful for automation scripts

### 📦 Copying & Moving Files (shutil)
```
import shutil

shutil.move(source_path, destination_path)
shutil.copy(source_path, destination_path)
```

### Practical Uses:

Data migration
Backup automation
File organization scripts

### 🛠 Modules Used
Module	Purpose
os	Directory & file system operations
shutil	Copying and moving files
json	Working with JSON data
open()	File handling
with	Context manager

### 🚀 Skills Demonstrated

File Input/Output operations
Resource management
Exception handling
Automation fundamentals
Structured data writing (CSV/JSON)
OS-level file manipulation
Clean and safe coding practices

### 📈 Real-World Applications

This knowledge applies directly to:
Data Engineering pipelines
ETL automation
Log management systems
Report generation
Backup systems
Python scripting jobs
Backend development

### 🎯 Learning Outcome

By completing this project, I strengthened my understanding of:
How Python interacts with the operating system
Managing file lifecycle properly
Writing production-safe file operations
Handling errors gracefully
Organizing and automating file workflows

### 🏁 Conclusion

This project demonstrates practical, real-world Python file handling skills — moving beyond theory into implementation.
It builds a strong foundation for:
Automation
Data analytics
Data engineering
Backend scripting

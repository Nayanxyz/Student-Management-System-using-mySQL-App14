# 🎓 Student Management System 

A robust, Object-Oriented Desktop Graphical User Interface (GUI) application built with Python and PyQt6. This system performs complete CRUD (Create, Read, Update, Delete) operations, bridging a modern desktop frontend with a MySQL relational database backend.

<img width="1052" height="832" alt="Student-Management-System" src="https://github.com/user-attachments/assets/35c5f665-c0bb-4a7a-8484-6d92dad62f3d" />

## 🧠 Engineering Features
* **Full CRUD Functionality:** Seamlessly insert, search, edit, and delete student records directly from the UI.
* **Dynamic Event-Driven UI:** Utilizes PyQt signal-slot architecture. (e.g., Edit and Delete action buttons dynamically render in the `QStatusBar` only when a user selects a specific table row).
* **Safe Database Architecture:** Implements connection parameterization and pure-Python database engine bridging (`use_pure=True` / `pymysql`) to strictly prevent C-level DLL memory access violations (0xC0000005 errors).
* **Error Handling:** Wraps database execution blocks in `try-except` constraints to gracefully catch and report connection failures without silently crashing the main GUI loop.

## 🛠️ Tech Stack
* **Language:** Python 3.12
* **GUI Framework:** PyQt6
* **Database:** MySQL
* **Connector:** `mysql-connector-python` (or `pymysql`)

## ⚙️ Database Setup (Prerequisite)
Before running the application, you must configure the local MySQL environment. 

1. Open your MySQL command line or Workbench.
2. Execute the following SQL schema to create the required database and table:

```sql
CREATE DATABASE school;
USE school;

CREATE TABLE students (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    course VARCHAR(255) NOT NULL,
    mobile VARCHAR(15) NOT NULL
);
```

## 🚀 How to Run Locally

**1. Clone the repository**
```bash
git clone https://github.com/Nayanxyz/Student-Management-System-using-mySQL-App14.git 
cd Student-Management-System-using-mySQL-App14
```
**2. Install Dependencies**
```bash
pip install PyQt6
mysql-connector-python
```

**3. Execute the Application**
```bash
python main.py
```

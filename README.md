
# 🏦 Java Banking System

## 📖 Overview
This is a **console-based banking application** built using **Java**, **JDBC**, and **MySQL**. It allows users to **register, log in, open a bank account**, and perform **banking transactions** like **deposits, withdrawals, and money transfers** securely. 🔒

## 🚀 Features
- ✅ **User Authentication** (Register/Login)
- ✅ **Bank Account Management** (Create, Retrieve)
- ✅ **Deposit Money** 🏦
- ✅ **Withdraw Money** 💵
- ✅ **Transfer Money Between Accounts** 🔄
- ✅ **Check Account Balance** 📊
- ✅ **SQL Database Integration (MySQL)**

## 🛠️ Tech Stack
- **Java** (JDK 8+) ☕
- **JDBC** (Java Database Connectivity) 🔗
- **MySQL Database** 🗄️
- **Git for Version Control** 🛠️

---

## 📂 Project Structure
```plaintext
Banking-System/
│── src/
│   ├── BankingApp.java
│   ├── User.java 
│   ├── Accounts.java
│   ├── AccountManager.java
│── .gitignore
│── README.md
│── banking_system.sql
```

## 🎮 How to Run the Project

### ⚡ 1️⃣ Clone the Repository
```sh
git clone https://github.com/your-username/Banking-System.git
cd Banking-System
```

### ⚡ 2️⃣ Set Up the Database
1. Start your MySQL server.
2. Run the `banking_system.sql` script to create the necessary database and tables.

```sql
CREATE DATABASE banking_system;
USE banking_system;

CREATE TABLE User (
    id INT AUTO_INCREMENT PRIMARY KEY,
    full_name VARCHAR(100),
    email VARCHAR(100) UNIQUE NOT NULL,
    password VARCHAR(255) NOT NULL
);

CREATE TABLE Accounts (
    account_number BIGINT PRIMARY KEY,
    full_name VARCHAR(100),
    email VARCHAR(100) UNIQUE NOT NULL,
    balance DECIMAL(10,2) DEFAULT 0.00,
    security_pin VARCHAR(10) NOT NULL
);
```

### ⚡ 3️⃣ Compile and Run the Program
```sh
javac BankingApp.java
java BankingApp
```

💡 Make sure you have Java and MySQL installed!

---

## 🛡️ Security Considerations
- 🔹 Uses Prepared Statements to prevent SQL Injection.
- 🔹 Security Pin validation for each transaction.
- 🔹 Auto-commit disabled to ensure transactions are fully completed before committing.

## 🔔 Future Enhancements
1. Password Hashing (BCrypt) for secure storage.
2. GUI Interface using JavaFX or Spring Boot.

---

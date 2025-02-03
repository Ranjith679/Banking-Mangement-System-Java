# 🏦 Java Banking System

## 📖 Overview
This is a **console-based banking application** built using **Java, JDBC, and MySQL**. It allows users to **register, log in, open a bank account**, and perform **banking transactions** like **deposit, withdrawal, and money transfer** securely. 🔒

## 🚀 Features
✅ **User Authentication** (Register/Login)  
✅ **Bank Account Management** (Create, Retrieve)  
✅ **Deposit (Credit) Money** 🏦  
✅ **Withdraw (Debit) Money** 💵  
✅ **Transfer Money Between Accounts** 🔄  
✅ **Check Account Balance** 📊  
✅ **SQL Database Integration (MySQL)**  

## 🛠️ Tech Stack
- **Java** (JDK 8+) ☕  
- **JDBC** (Java Database Connectivity) 🔗  
- **MySQL Database** 🗄️  
- **Git for Version Control** 🛠️  

---

## 📂 Project Structure
Banking-System/
│── src/
│   ├── BankingApp.java        # Main application (Handles user interface and flow)
│   ├── User.java              # Manages user authentication (Register/Login)
│   ├── Accounts.java          # Handles bank account creation and retrieval
│   ├── AccountManager.java    # Handles transactions (Deposit, Withdraw, Transfer, Balance Check)
│── .gitignore                 # Ignore unnecessary files (e.g., compiled files, IDE settings)
│── README.md                  # Documentation (Project overview, setup guide, usage)
│── banking_system.sql         # SQL script to create necessary database tables


## 🎮 How to Run the Project

### ⚡ 1️⃣ **Clone the Repository**
```sh
git clone https://github.com/your-username/Banking-System.git
cd Banking-System

🚀 3️⃣ Compile and Run the Program
sh
Copy
Edit
javac BankingApp.java
java BankingApp
💡 Make sure you have Java and MySQL installed!

🗃️ Database Schema (banking_system.sql)
sql
Copy
Edit
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
📜 Usage Guide
🏦 1️⃣ Register a New User
Enter Full Name, Email, Password.
If the email is already registered, it will show:
kotlin
Copy
Edit
User Already Exists for this Email Address!!
🔑 2️⃣ Log In
Enter Email & Password.
If successful, it will check if you have an account:
pgsql
Copy
Edit
User Logged In!
If you don’t have an account, it will prompt you to create one.
💵 3️⃣ Open a Bank Account
Enter Full Name, Initial Deposit, Security Pin.
If successful:
csharp
Copy
Edit
Account Created Successfully!
Your Account Number is: XXXXXXX
🔄 4️⃣ Perform Banking Transactions
Option	Action
1	Debit Money
2	Credit Money
3	Transfer Money
4	Check Balance
5	Log Out
💡 Invalid PINs, Insufficient Balance, or Incorrect Inputs are handled with proper error messages.

🛡️ Security Considerations
🔹 Uses Prepared Statements to prevent SQL Injection.
🔹 Security Pin validation for each transaction.
🔹 Auto-commit disabled to ensure transactions are fully completed before committing.

🔔 Future Enhancements:

Password Hashing (BCrypt) for secure storage.
GUI Interface using JavaFX or Spring Boot.

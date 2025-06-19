
# 💳 ATM Banking System (Java + MySQL)

This project is a **Bank Management System** simulating the functionalities of an ATM. It is built using **Java Swing** for the GUI and **MySQL** as the backend database. The system supports user registration, account setup, login, transactions like deposit/withdrawal, and balance inquiry.

---

## 📌 Features

- Create new bank accounts (multi-step sign-up)
- Auto-generate card number and PIN
- Login using card number and PIN
- Deposit and withdraw money
- View mini statements
- Check account balance
- Change PIN

---

## 🛠️ Tech Stack

| Component         | Technology         |
|------------------|--------------------|
| Frontend (GUI)   | Java Swing         |
| Backend Logic    | Java               |
| Database         | MySQL              |
| Connectivity     | JDBC               |

---

## 📁 Project Structure

```
bank-management-system/
├── ASimulatorSystem/
│   ├── Login.java
│   ├── Signup.java
│   ├── Signup2.java
│   ├── Signup3.java
│   ├── Deposit.java
│   ├── Withdraw.java
│   ├── MiniStatement.java
│   ├── BalanceEnquiry.java
│   ├── PinChange.java
│   └── Conn.java
├── icons/
│   └── logo.jpg
├── README.md
```

---

## 🗃️ MySQL Database Setup

Open your MySQL CLI or any GUI like phpMyAdmin and run the following commands:

### 1. `signup` Table
```sql
CREATE TABLE signup (
  formno VARCHAR(20),
  name VARCHAR(50),
  father_name VARCHAR(50),
  dob VARCHAR(20),
  gender VARCHAR(10),
  email VARCHAR(50),
  marital_status VARCHAR(20),
  address VARCHAR(100),
  city VARCHAR(20),
  pincode VARCHAR(10),
  state VARCHAR(20)
);
```

### 2. `signup2` Table
```sql
CREATE TABLE signup2 (
  formno VARCHAR(20),
  religion VARCHAR(20),
  category VARCHAR(20),
  income VARCHAR(20),
  education VARCHAR(30),
  occupation VARCHAR(30),
  pan VARCHAR(20),
  aadhar VARCHAR(20),
  seniorcitizen VARCHAR(10),
  existingaccount VARCHAR(10)
);
```

### 3. `signup3` Table
```sql
CREATE TABLE signup3 (
  formno VARCHAR(20),
  account_type VARCHAR(30),
  card_number VARCHAR(20),
  pin VARCHAR(10),
  services VARCHAR(100)
);
```

### 4. `login` Table
```sql
CREATE TABLE login (
  formno VARCHAR(20),
  card_number VARCHAR(20),
  pin VARCHAR(10)
);
```

### 5. `bank` Table
```sql
CREATE TABLE bank (
  formno VARCHAR(20),
  card_number VARCHAR(20),
  date VARCHAR(50),
  type VARCHAR(20),
  amount VARCHAR(20)
);
```

---

## ▶️ How to Run the Project

### 🖥️ Prerequisites:
- Java JDK 8 or above
- MySQL Server
- MySQL Connector/J JAR
- IDE (Eclipse / IntelliJ / VS Code) or terminal

### ⚙️ Steps:
1. Clone or download this repository.
2. Create the database:  
   ```sql
   CREATE DATABASE bankmanagementsystem;
   USE bankmanagementsystem;
   ```
3. Create the required tables (see above).
4. Update your `Conn.java` file with your MySQL username & password:
   ```java
   Connection c = DriverManager.getConnection("jdbc:mysql://localhost:3306/bankmanagementsystem", "root", "your_password");
   ```
5. Compile and run:
   ```bash
   javac ASimulatorSystem/*.java
   java ASimulatorSystem.Login
   ```

---

## 🙋‍♀️ Developed By

**Madhuri**  
Java Developer | UI/UX Enthusiast | Backend Integrator

---

## 📄 License

This project is open-source and free to use for learning and development purposes.

---

## 📬 Contact

Feel free to connect for queries or collaboration:

- 📧 Email: *[madhurideekshitha2005@gmail.com]*
- 💼 LinkedIn: *[linkedin.com/in/madhuri2005]*

---

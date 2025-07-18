## 🏦 Bank Management System (ATM Simulator System)

A full-fledged desktop-based **ATM Simulator / Bank Management System** project developed using **Java Swing**, **JDBC**, and **MySQL**. It allows users to sign up, log in, and perform various banking operations like withdrawal, deposit, balance enquiry, PIN change, and more.

---

### 🚀 Tech Stack

* **Frontend / GUI:** Java Swing, AWT, Event Listeners
* **Backend:** Java (Core + JDBC)
* **Database:** MySQL
* **IDE Used:** NetBeans / VS Code
* **Java Version:** JDK 8+

---

### 📚 Java Libraries Used

```java
import javax.swing.*;         // GUI components
import java.awt.*;            // Layouts, color, font
import java.awt.event.*;      // Event listeners
import java.util.*;           // Random number generation, utility functions
import java.sql.*;            // JDBC for DB connection
import com.toedter.calendar.*;// JDateChooser for date selection (optional)
```

---

## 🛠️ Project Structure and Execution Steps

---

### 🔐 1. **Login Page**

* Allows users to enter **Card Number** and **PIN**.
* Verifies credentials using the `login` table in MySQL.
* On success, redirects to **Transactions Menu**.

---

### 📝 2. **Signup Process**

#### 📄 `SignupOne.java`

* Collects basic info: name, father’s name, DOB, gender, email, marital status, address.
* Stores it in the `signup` table.

#### 📄 `SignupTwo.java`

* Collects extra info: religion, income, education, occupation, PAN, Aadhar, senior citizen, and existing account status.
* Stores in the `signup2` table.

#### 📄 `SignupThree.java`

* Generates **Card Number** and **PIN**.
* Asks to choose Account Type (Saving/Current/Fixed/Recurring).
* Data saved in:

  * `signup3` table (account type)
  * `login` table (card number, pin)

---

### 💳 3. **Transaction Menu (`Transactions.java`)**

Post login, user can perform the following actions:

#### 💰 Deposit

* Opens a window to enter the amount.
* Inserts a record in the `bank` table with **type = Deposit**.

#### 💸 Withdraw

* Prompts for withdrawal amount.
* Validates available balance from `bank` table.
* Inserts a record with **type = Withdrawal**.

#### ⚡ Fast Cash

* Allows predefined quick withdrawals (₹100, ₹500, ₹1000, etc.)
* Same logic as Withdraw but faster.

#### 🧾 Mini Statement

* Displays last few transactions from the `bank` table.

#### 🧮 Balance Enquiry

* Fetches and calculates total balance using all transactions of the user in `bank` table.

#### 🔐 PIN Change

* User inputs old PIN and new PIN.
* Updates the PIN in `login` table.

---

### 🗃️ 4. **Database Design**

#### 📁 Tables Used:

1. **`signup`**
   Stores initial personal details.

2. **`signup2`**
   Stores additional details like income, education, occupation.

3. **`signup3`**
   Stores account type info and final confirmation.

4. **`login`**
   Stores card number and PIN for authentication.

5. **`bank`**
   Stores transaction records (Deposit, Withdraw).

---



### 👨‍💻 Author

* **Name:** *Sriram Chiliveri*
* **LinkedIn:** [Your LinkedIn](https://www.linkedin.com/in/sriram-chiliveri-35409727a/)
* **GitHub:** [Your GitHub](https://github.com/sriram1544)

---



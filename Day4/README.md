# Day 4 – EC2, RDS/Aurora & Mini Project 🚀

> Day 4 ka focus real-world practice par tha. Isme maine EC2, RDS/Aurora aur ek small database project ko practically samjha aur implement kiya. Ye notes aise likhe gaye hain ki future me padhte hi pura flow yaad aa jaaye.

---

## 1. EC2 Instances

### Short Definition

EC2 instance ek **virtual server** hota hai jo cloud me run karta hai. Ispar hum applications, database client, ya backend services chala sakte hain.

### Key Points I Learned

* EC2 ko application server ke tarah use kar sakte hain
* Instance ke through hum RDS/Aurora se connect karte hain
* Security Group ka role bahut important hota hai

---

## 2. Aurora and RDS

### Short Definition

**Amazon RDS** ek managed database service hai jo MySQL, MariaDB, PostgreSQL jaise engines support karti hai.

**Amazon Aurora** ek high-performance database hai jo MySQL aur PostgreSQL compatible hota hai aur RDS se zyada fast aur scalable hota hai.

### Difference (Simple Words)

* RDS = Managed database, easy to use
* Aurora = RDS ka advanced version (high availability + performance)

---

## 3. Users (Database Level)

### Short Definition

Database users ka use **secure access** dene ke liye hota hai, taki har koi database ko directly access na kar sake.

Key idea:

* Har application / person ka alag user
* Limited permissions

---

## 4. Mini Project – EC2 + Database Integration

### Project Overview

Is project me maine:

* EC2 instance create kiya
* EC2 me login kiya
* MariaDB install ki
* Database aur table create ki
* RDS / Aurora database ke concept ko samjha

---

### Step 1: Create an EC2 Instance

1. AWS Console → EC2
2. Launch Instance
3. Amazon Linux AMI select ki
4. Instance type (t2.micro)
5. Key pair & security group configure ki
6. Instance launch kiya

---

### Step 2: Login into EC2 Instance

* SSH ke through EC2 me login kiya
* Instance ke andar commands run ki

---

### Step 3: Install MariaDB (Commit Steps)

1. MariaDB install ki:
   sudo yum install mariadb -y

2. MariaDB version check ki:
   mysql --version

---

### Step 4: Database Create & Setup

1. Database create kiya:
   CREATE DATABASE aws;

2. Database use ki:
   USE aws;

3. Databases check ki:
   SHOW DATABASES;

4. Users table create ki:
   CREATE TABLE users (
   id INT AUTO_INCREMENT PRIMARY KEY,
   name VARCHAR(100),
   email VARCHAR(100),
   created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
   );

👉 Is table ka use user data store karne ke liye hota hai.

---

## 5. Create Database using Aurora / RDS

### Steps (High Level)

1. AWS Console → RDS
2. Create Database
3. Engine select (Aurora / MySQL / MariaDB)
4. DB instance settings configure ki
5. Username & password set kiya
6. Database create ki

---

## 6. Connect Database with EC2

### Short Explanation

EC2 ko database se connect karne ke liye:

* EC2 aur RDS same VPC me hone chahiye
* Security group me DB port allow hona chahiye (3306 for MySQL/MariaDB)

👉 Isse EC2 application database se communicate kar paata hai.

---

## 7. Create IAM Roles for Project

### Roles Used

* AmazonRDSFullAccess
* CloudWatchEventsFullAccess

### Short Definition

IAM Role EC2 ko **permissions deta hai** bina access key use kiye.

### Steps to Create and Attach Role

1. IAM → Roles → Create role
2. Trusted entity: EC2
3. Attach policies:

   * AmazonRDSFullAccess
   * CloudWatchEventsFullAccess
4. Role create karo
5. EC2 instance ke saath role attach karo

👉 Ab EC2 securely RDS aur CloudWatch ko access kar sakta hai.

---

## Final Notes ✨

* EC2 = Application server
* RDS / Aurora = Managed database
* Project = EC2 + Database integration
* IAM Role = Secure permission management

📌 Day 4 ne real-world AWS architecture ka clear idea diya.

---

**End of Day 4 Learning ✅**


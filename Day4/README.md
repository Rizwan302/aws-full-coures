# Day 4 – AWS EC2 Learning Notes 🚀

> This README file is written by me for my own learning and revision. The main goal is that whenever I read this file again, everything should become clear without needing to relearn. The language is kept simple and human, just like personal notes – not copied from any report or AI-style content.

---

## 1. Simple EC2 Instance

### Short Definition

An EC2 (Elastic Compute Cloud) instance is basically a **virtual computer (server)** that runs inside the AWS cloud. On this server, we can run applications, websites, or any software just like we do on our own laptop or PC.

### Steps to Create an EC2 Instance

1. Login to the AWS Console
2. Go to the **EC2 service**
3. Click on **Launch Instance**
4. Choose an **AMI (Amazon Machine Image)** (for example: Amazon Linux)
5. Select an **Instance Type** (for example: t2.micro – free tier)
6. Create or select a **Key Pair** (used for login)
7. Configure the **Security Group** (allow SSH, HTTP if needed)
8. Click on **Launch Instance**

👉 Your simple EC2 instance is now running in the cloud.

---

## 2. Instance Type

### Short Definition

An instance type defines how powerful your EC2 instance will be. It decides the amount of **CPU (vCPU), RAM, storage, and network performance**.

In simple words – instance type = power of the server.

### Common Instance Type Examples

* **t2.micro / t3.micro** – practice, small apps, free tier
* **t3.medium** – medium workload
* **m5** – general purpose
* **c5** – CPU intensive tasks

### Steps to Select an Instance Type

1. While launching an EC2 instance, go to the **Instance Type** section
2. Choose the type based on your requirement
3. For practice and free tier, **t2.micro** is usually the best option

👉 Choosing the wrong instance type can cause performance issues or higher cost.

---

## 3. Launch Template

### Short Definition

A Launch Template is a **blueprint** that stores all the configuration details of an EC2 instance such as AMI, instance type, key pair, security group, etc.

It helps in launching multiple instances with the same configuration very easily.

### Steps to Create a Launch Template

1. Go to the **EC2 Dashboard**
2. Open the **Launch Templates** section
3. Click on **Create launch template**
4. Enter the template name and description
5. Choose an AMI
6. Select the instance type
7. Add key pair and security group
8. Click on **Create launch template**

👉 Now you can launch multiple EC2 instances using the same template.

---

## 4. Auto Scaling Groups (ASG)

### Short Definition

Auto Scaling Group automatically **increases or decreases the number of EC2 instances** based on traffic or load.

In simple terms:

* High load → new instances are added automatically
* Low load → extra instances are removed automatically

This helps in saving cost and keeps the application stable.

### Steps to Create an Auto Scaling Group

1. Go to the **EC2 Dashboard**
2. Open **Auto Scaling Groups**
3. Click on **Create Auto Scaling Group**
4. Select an existing **Launch Template**
5. Choose VPC and subnets
6. Set **Desired, Minimum, and Maximum capacity**
7. Add a scaling policy (for example: CPU-based scaling)
8. Click on **Create Auto Scaling Group**

👉 Now AWS will automatically manage instances based on load.

---

## Final Notes ✨

* EC2 = Virtual server
* Instance Type = Server power
* Launch Template = Ready-made configuration
* Auto Scaling Group = Automatic instance management

📌 These notes are perfect for future revision. Whenever I read this file again, everything will become clear.

---

**End of Day 2 Learning ✅**

# Day 3 – AWS S3 & IAM Learning Notes 🚀

> These notes are written by me for clear understanding and future revision. The goal is simple: if I read this again later, everything should be clear without relearning. Language is simple, practical, and human.

---

## 1. Create a Simple S3 Bucket

### Short Definition

An S3 (Simple Storage Service) bucket is used to **store files and data** like images, videos, documents, backups, etc. It is highly durable and scalable.

### Steps to Create a Simple S3 Bucket

1. Login to AWS Console
2. Go to **S3 service**
3. Click on **Create bucket**
4. Enter a **unique bucket name**
5. Select the **AWS region**
6. Keep default settings (or as required)
7. Click on **Create bucket**

👉 Your S3 bucket is now ready to store data.

---

## 2. S3 Bucket with Static Website Hosting

### Short Definition

Static website hosting in S3 allows us to **host a simple website** (HTML, CSS, JS) without using any server.

### Steps to Host a Static Website on S3

1. Create an S3 bucket (bucket name should match website name)
2. Upload website files (HTML, CSS, JS)
3. Go to **Properties** tab of the bucket
4. Enable **Static website hosting**
5. Set index document (e.g. `index.html`)
6. Go to **Permissions** → Bucket Policy
7. Add a public read policy

👉 Now your website is live using the S3 website endpoint.

---

## 3. IAM (Identity and Access Management)

### Short Definition

IAM is used to **manage users, permissions, and access** to AWS services securely.

With IAM, we control:

* Who can access AWS
* What actions they can perform

---

## 4. Create an IAM User

### Short Definition

An IAM user represents a **person or application** that needs access to AWS.

### Steps to Create an IAM User

1. Go to **IAM service**
2. Click on **Users**
3. Click **Add user**
4. Enter username
5. Select access type (Console / Programmatic)
6. Attach permissions (or add to group)
7. Create user and save credentials

👉 User can now access AWS based on given permissions.

---

## 5. Create an IAM Group

### Short Definition

An IAM group is a **collection of users** with the same permissions.

### Steps to Create an IAM Group

1. Go to **IAM → Groups**
2. Click **Create group**
3. Enter group name
4. Attach required policies
5. Add users to the group

👉 Group makes permission management easier.

---

## 6. Create an IAM Role

### Short Definition

An IAM role is used to **give temporary permissions** to AWS services or users without sharing credentials.

### Steps to Create an IAM Role

1. Go to **IAM → Roles**
2. Click **Create role**
3. Select trusted entity (AWS service / user)
4. Attach policies
5. Enter role name
6. Create role

👉 Roles are mostly used with EC2, Lambda, etc.

---

## 7. Create an IAM Policy

### Short Definition

An IAM policy defines **what actions are allowed or denied** on AWS resources.

### Steps to Create an IAM Policy

1. Go to **IAM → Policies**
2. Click **Create policy**
3. Choose JSON or visual editor
4. Define permissions (Allow / Deny)
5. Review and create policy

👉 Policies are attached to users, groups, or roles.

---

## Final Notes ✨

* S3 = Storage service
* Static website = Serverless hosting
* IAM = Security & access control
* User = Individual access
* Group = Multiple users, same permissions
* Role = Temporary access
* Policy = Permission rules

📌 These notes are enough for revision and real-world understanding.

---

**End of Day 3 Learning ✅**

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

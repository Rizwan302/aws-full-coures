# Day 2 – AWS EC2 Learning Notes 🚀

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

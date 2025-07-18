# 🐧 Mini Project: Linux Fundamentals – EC2 Setup & Server Access
---
## 🧱 Objective  
Simulate connecting to a cloud-based Linux server (Ubuntu EC2 instance on AWS) using SSH, install packages using Linux commands, and verify their functionality — laying a foundation for DevOps or cloud administration.
---
## ✅ Step-by-Step Execution Report
---
### 🔹 Step 1: AWS Account Setup
1. Visit [https://aws.amazon.com](https://aws.amazon.com)
2. Create a new AWS account using your email.
3. Complete identity verification and payment method steps.
4. Log into the AWS Management Console.
---
### 🔹 Step 2: Launch an EC2 Instance (Linux Server)
1. In AWS Console, search for **EC2** under “Services”.
2. Click **“Launch instance”** → name it (e.g., `linux-fundamentals`).
3. Select an Ubuntu AMI (e.g., Ubuntu Server 22.04 LTS).
4. Choose instance type: `t2.micro` (Free tier eligible).
5. Create or select an existing key pair (`ubuntu.pem`) — download it and keep safe.
6. Accept default network and storage settings.
7. Click **Launch Instance**.
---
### 🔹 Step 3: Install Terminal Tool (if on Windows)
- Recommended tool: **MobaXterm** (Download [here](https://mobaxterm.mobatek.net/))
- Alternatively: Git Bash, PuTTY, or Windows PowerShell
- macOS: Use built-in **Terminal**
---
### 🔹 Step 4: Connect to the EC2 Server via SSH
1. Move to your `.pem` key location:
   ```bash
   cd ~/Downloads
   ```
2. Change permissions to secure the key file:
   ```bash
   chmod 400 ubuntu.pem
   ```
3. Extract EC2 **public IP address** from AWS Console

4. Connect using SSH:
   ```bash
   ssh -i "ubuntu.pem" ubuntu@<your-ec2-public-ip>
   ```
✅ You should now be inside the remote server environment (e.g., Ubuntu CLI)
### 🔹 Step 5: Update System Packages
```bash
sudo apt update
sudo apt upgrade -y
```
---
### 🔹 Step 6: Install & Use `tree` Command
1. Install tree utility:
   ```bash
   sudo apt install tree
   ```
2. Use it to explore directories:
   ```bash
   tree ~/Downloads
   ```
---
### 🔹 Step 7: Remove Software
```bash
sudo apt remove tree
```
---
### 🔹 Step 8: Bonus Practice (Try More Commands)
- Install and use other packages (e.g., nginx)
  ```bash
  sudo apt install nginx
  sudo systemctl status nginx
  ```
- Navigate directories:
  ```bash
  cd /
  ls -la
  ```
---
### 🔹 Final Outcome
You should be able to:
- Access a Linux server remotely
- Use basic Linux navigation and package management
- Install and remove packages like a DevOps engineer in training
---
## 📁 Suggested Documentation Additions
You can now include:
- Screenshots of your EC2 dashboard and terminal
- Output of `tree` and `ls` commands
- Notes on SSH protocol and key permissions

# Ansible-automation-tasks

# 🔧 Automated Multi-OS Web & FTP Setup Using Ansible (AWS)

This project automates the setup of **Apache/HTTPD**, **Nginx**, and **vsftpd** services across multiple **Ubuntu** and **RedHat (RHEL)** EC2 instances using **Ansible**.

> ✅ This is a fully idempotent and repeatable Ansible playbook designed to work in real-world multi-OS environments hosted on **AWS EC2**.

---

## 📁 Project Structure

multi-os-ansible-setup/
├── inventory.ini # Inventory file with grouped Ubuntu and RedHat EC2 instances
├── playbook.yml # Main Ansible playbook
└── Ansible-key.pem # SSH key to access the EC2 instances

**📦 playbook.yml Tasks Overview**

✅ Detect OS (Ubuntu or RedHat)

📦 Install appropriate packages based on OS

⚠️ Stop Apache before starting Nginx to avoid port conflict

🔁 Enable and start Nginx and vsftpd services

**🚀 How to Run**

**1. Connect to Ansible Controller EC2:**

  > ssh -i your-key.pem ubuntu@<controller-ec2-public-ip>

**2. Clone this Repository**

  > git clone https://github.com/your-username/multi-os-ansible-setup.git
  > cd multi-os-ansible-setup
**3. Update Inventory File**

  > Replace IPs with your actual EC2 instance IPs in inventory.ini.

**4. Run the Playbook**

  > ansible-playbook -i inventory.ini playbook.yml

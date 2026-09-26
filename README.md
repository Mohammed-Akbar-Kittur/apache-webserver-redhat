# 🌐 Apache Web Server - akbarlinops.com

**Project By: Mohammed Akbar Kittur | Linux + DevOps**
**Server IP: 192.168.15.10 | Apache HTTPD on RedHat Linux**

### 🔗 Live Domains
- http://akbarlinops.com
- http://www.akbar-server.com
- http://192.168.15.10

### 📸 Live Proof
https://raw.githubusercontent.com/Mohammed-Akbar-Kittur/apache-webserver-redhat/main/<img width="1366" height="690" alt="image" src="https://github.com/user-attachments/assets/2b373ff7-0b6f-4647-914f-fe546c8077b7" />

*If image not showing, upload screenshot.png first*

### 🛠️ Tech Stack
- OS: RedHat Enterprise Linux 9 (RHEL)
- Web Server: Apache HTTPD
- Frontend: HTML + CSS Neon Glow UI
- Client: Windows 10 + Firefox
- Local DNS: Windows hosts file

### ⚙️ Server Configuration (RHEL)

**1. Install Apache**
```bash
sudo dnf install httpd -y
sudo systemctl enable --now httpd
sudo firewall-cmd --permanent --add-service=http
sudo firewall-cmd --reload

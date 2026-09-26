# 🌐 AkbarLinOps.com - My DevOps Lab
### Live Domain: `akbarlinops.com` | IP: `192.168.15.10` | Year: 2026

> "This server is proudly configured and owned by me." - Mohammed Akbar Kittur

![Status](https://img.shields.io/badge/Status-Live-brightgreen)
![OS](https://img.shields.io/badge/OS-RHEL9-red)
![Server](https://img.shields.io/badge/WebServer-Apache-blue)
![Year](https://img.shields.io/badge/Year-2026-gold)

## 📸 Live Proof - Sept 2026
<img width="1364" height="684" alt="image" src="https://github.com/user-attachments/assets/c9deeab9-ce8e-4a54-8377-4d83734865d6" />
*Successfully running on Firefox at http://akbarlinops.com*

## 🚀 About This Project
I have successfully deployed and hosted my own website `akbarlinops.com` on RedHat Linux using Apache HTTPD. This project covers Linux Admin + Networking + Web Hosting - The foundation of DevOps.

## 🛠️ Tech Stack
- **Operating System:** RedHat Enterprise Linux 9
- **Web Server:** Apache HTTP Server (httpd)
- **Domain:** akbarlinops.com (Custom DNS mapping via /etc/hosts)
- **IP Address:** 192.168.15.10
- **Frontend:** HTML5 + CSS3 (Golden Theme - #FFD700)
- **Version Control:** Git & GitHub

## ⚙️ Implementation Steps (2026)

**1. Install & Start Apache:**
```bash
sudo dnf install httpd -y
sudo systemctl enable --now httpd
sudo firewall-cmd --permanent --add-service=http
sudo firewall-cmd --reload

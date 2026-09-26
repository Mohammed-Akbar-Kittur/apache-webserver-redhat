# akbarlinops.com 🚀

### Apache Web Server on RHEL 9 | Root Setup
**Mohammed Akbar Kittur | Linux + DevOps**

---

### 📊 Project Info

| Field | Details |
|-------|---------|
| **Domain** | akbarlinops.com |
| **Server IP** | 192.168.15.10 |
| **OS** | RedHat Enterprise Linux 9 |
| **Web Server** | Apache HTTPD |
| **Access** | Root User |
| **Package Manager** | yum |

---

### 📸 Live Output

<img width="1366" height="690" alt="image" src="https://github.com/user-attachments/assets/770a2421-a45e-4a87-b2d9-cbf14172a0be" />


**Current Output:**
- ✅ `http://192.168.15.10` - Working (Your photo proof)
- ✅ `http://akbarlinops.com` - Working via local DNS
- Design: Black + Red Neon Card | Golden Heading | Green Name

---

### ⚡ One-Click Setup Script

> **Run as `root` on RHEL 9 - Only ONE script needed**

```bash
#!/bin/bash
# ---------------------------------------------------
# Project: akbarlinops.com
# Author: Mohammed Akbar Kittur
# OS: RHEL 9 | Access: Root | Manager: yum
# ---------------------------------------------------

yum install httpd -y
systemctl enable --now httpd
firewall-cmd --permanent --add-service=http --add-service=https
firewall-cmd --reload
mkdir -p /var/www/akbarlinops.com && chmod -R 755 /var/www/akbarlinops.com

# --- VirtualHost Config ---
cat > /etc/httpd/conf.d/akbarlinops.com.conf <<'CONF'
<VirtualHost *:80>
    ServerName akbarlinops.com
    ServerAlias www.akbarlinops.com
    DocumentRoot /var/www/akbarlinops.com
    <Directory /var/www/akbarlinops.com>
        Require all granted
    </Directory>
</VirtualHost>
CONF

# --- Website Code ---
cat > /var/www/akbarlinops.com/index.html <<'HTML'
<!DOCTYPE html>
<html><head><title>akbarlinops.com</title>
<style>
body{margin:0;background:#000;display:flex;justify-content:center;align-items:center;height:100vh;font-family:Arial}
.card{background:#1a1a1a;border:3px solid red;border-radius:15px;padding:40px 50px;text-align:center;box-shadow:0 0 20px red}
h1{color:#ffeb3b;text-shadow:0 0 10px #ffeb3b}h2{color:#0f0}p{color:#fff}
.domain{color:cyan;font-weight:bold}hr{border:0.5px solid #fff;margin:20px 0}
</style></head>
<body><div class="card">
<h1>Welcome to My Web Server</h1>
<h2>Mohammed Akbar Kittur</h2>
<p>Apache Server Running on RedHat Linux</p>
<p>Domain: <span class="domain">akbarlinops.com</span></p><hr>
<p><i>"This server is proudly configured and owned by me."</i></p>
<p>IP: 192.168.15.10 | Skills: Linux + DevOps</p>
</div></body></html>
HTML

cp /var/www/akbarlinops.com/index.html /var/www/html/index.html
systemctl restart httpd
echo "✅ DONE: akbarlinops.com LIVE at 192.168.15.10"

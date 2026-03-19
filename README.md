# 🔐 Web Application Security Assessment
**Cyber Security Internship – Practical Exam | Treinetic (Pvt) Ltd**

---

## Candidate
**Name:** Arkam Minnas

---

## Target Application
**DVWA (Damn Vulnerable Web Application)**
Running locally via XAMPP on Windows.

---

## Introduction
This repository contains a practical security assessment conducted on DVWA as part of the Cyber Security Internship exam at Treinetic (Pvt) Ltd. The goal was to identify, demonstrate, and analyze common web application vulnerabilities, and suggest fixes for each one found.

---

## Setup Instructions

### 1. Install XAMPP
Download and install from https://www.apachefriends.org

### 2. Setup DVWA
1. Download DVWA from https://github.com/digininja/DVWA/archive/refs/heads/master.zip
2. Extract and rename the folder to `dvwa`
3. Move it to `C:\xampp\htdocs\`

### 3. Configure Database
Go to `C:\xampp\htdocs\dvwa\config\`, copy `config.inc.php.dist` and rename it to `config.inc.php`, then update:
```php
$_DVWA[ 'db_user' ]     = 'root';
$_DVWA[ 'db_password' ] = '';
```

### 4. Start XAMPP
Open XAMPP Control Panel → Start **Apache** and **MySQL**

### 5. Initialize DVWA
Go to `http://localhost/dvwa/setup.php` → Click **"Create / Reset Database"**

### 6. Login
- URL: `http://localhost/dvwa/login.php`
- Username: `admin` | Password: `password`

### 7. Set Security Level
DVWA Security → Set to **Low** → Submit

---

## Tools Used
- **XAMPP** – Local web server
- **Burp Suite Community** – Intercepting HTTP requests

---

## Vulnerabilities Tested
| # | Vulnerability | Severity |
|---|--------------|----------|
| 1 | SQL Injection | 🔴 Critical |
| 2 | XSS – Reflected | 🟠 High |
| 3 | XSS – Stored | 🟠 High |
| 4 | Brute Force / Auth Issues | 🟠 High |
| 5 | IDOR | 🟡 Medium |
| 6 | Security Misconfiguration | 🟡 Medium |



> ⚠️ All testing was done in a local controlled environment for educational purposes only.

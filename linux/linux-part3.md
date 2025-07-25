# 🚀 Linux Fundamentals Part 3 — Cheat Sheet & Learning Reflection

This is a personal cheat sheet and reflection based on the **Linux Fundamentals Part 3** room on [TryHackMe](https://tryhackme.com/). It covers essential Linux skills including file editing, process management, automation, and more.

---

## 📚 Table of Contents

- [Editing Text Files in Terminal](#editing-text-files-in-terminal)
- [Downloading Files](#downloading-files)
- [Secure File Transfer](#secure-file-transfer)
- [Serving Files Over HTTP](#serving-files-over-http)
- [Processes](#processes)
- [Managing Services](#managing-services)
- [Background & Foreground Processes](#background--foreground-processes)
- [Automation with Cron](#automation-with-cron)
- [Packages & Repositories](#packages--repositories)
- [System Logs](#system-logs)
- [Reflection: What I Learned](#reflection-what-i-learned)

---

## 📝 Editing Text Files in Terminal

### Nano (Simple Editor)
```bash
nano filename
```
- 🔍 Search text: `Ctrl + W`  
- 🏃 Jump to line: `Ctrl + _`  
- ❌ Exit: `Ctrl + X`

### VIM (Advanced Editor)
```bash
vim filename
```
- ⚙️ Highly customizable with plugins and keybindings  
- 🎨 Syntax highlighting  
- 🌐 Pre-installed on most systems  
- 📚 Plenty of online tutorials and cheat sheets

---

## 🌐 Downloading Files

### Wget
```bash
wget https://example.com/file.txt
```
- Download files directly from the internet

---

## 🔐 Secure File Transfer

### SCP (Secure Copy)
- Local to Remote:
```bash
scp file user@remote:/path/
```

- Remote to Local:
```bash
scp user@remote:/path/file .
```

- Uses SSH for secure transfer

---

## 📂 Serving Files Over HTTP

### Python HTTP Server
```bash
python3 -m http.server
```
- Serves files from the current directory via HTTP  
- Accessible via `curl`, `wget`, or browser

For a more advanced tool, consider [Updog](https://github.com/sc0tfree/updog) 🐕

---

## ⚙️ Processes

### Viewing Processes
```bash
ps aux
top
```

### Managing Processes
```bash
kill <PID>
```
- Send signals to terminate or control processes

### Process Init System
- Linux uses namespaces and process IDs (PIDs)
- PID 0: Kernel process  
- PID 1: `systemd` (Ubuntu’s init system)

---

## 🔧 Managing Services

### Using `systemctl`
```bash
systemctl start service
systemctl stop service
systemctl enable service
systemctl disable service
```
- Controls background services and daemons

---

## 🎭 Background & Foreground Processes

- Run command in background:
```bash
long_script.sh &
```

- Suspend a process:
```bash
Ctrl + Z
```

- Resume foreground job:
```bash
fg
```

- View background jobs:
```bash
jobs
```

---

## ⏰ Automation with Cron

### Crontab
```bash
crontab -e
```

### Format
```
MIN HOUR DOM MON DOW CMD
```

### Example: Backup every 12 hours
```bash
0 */12 * * * cp -R /home/user/Documents /var/backups/
```

---

## 📦 Packages & Repositories

### Apt (Ubuntu/Debian)

- Add repository:
```bash
add-apt-repository ppa:name/ppa
```

- Update package list:
```bash
apt update
```

- Install package:
```bash
apt install package-name
```

- Remove package:
```bash
apt remove package-name
```

- Add GPG key (for repo authentication)

---

## 📜 System Logs

- Location:  
  ```bash
  /var/log
  ```

### Common Logs:
- Apache: `access.log`, `error.log`  
- fail2ban: intrusion detection  
- UFW: firewall events

- **Log rotation** helps manage file size and history

---

## 🧠 Reflection: What I Learned

- Improved my efficiency using terminal editors like **Nano** and **VIM**
- Learned to **download** and **securely transfer files** using `wget` and `scp`
- Served local files using **Python HTTP server**
- Explored Linux **processes**, including viewing, managing, and signaling
- Controlled system **services** with `systemctl`
- Gained experience multitasking using **background/foreground jobs**
- Automated tasks using **cron** and understood scheduling formats
- Managed software with **apt**, including adding PPAs and verifying with GPG keys
- Analyzed system **logs** to improve monitoring and troubleshooting
- Overall, I gained more confidence navigating, managing, and automating Linux systems

---

## 🔗 Related Links

- [TryHackMe: Linux Fundamentals Part 3](https://tryhackme.com/)
- [My LinkedIn Profile](https://www.linkedin.com/in/areebah890)

---

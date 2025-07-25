# 🚀 Linux Fundamentals Part 3 Cheat Sheet

---

## 📝 Editing Text Files in Terminal

### 🐢 Nano
- Simple text editor: `nano filename`
- Features:
  - 🔍 Search text: `Ctrl + W`
  - 📋 Copy/paste
  - 🏃 Jump to line: `Ctrl + _`
  - 🔢 Show current line number
  - ❌ Exit: `Ctrl + X`

### 🐉 VIM
- Advanced, customizable terminal editor
- Features:
  - ⚙️ Custom keybindings
  - 🎨 Syntax highlighting (great for coding)
  - 🌐 Available on almost all terminals
  - 📚 Extensive tutorials and cheat sheets available

---

## 🌐 Downloading Files

### ⬇️ Wget
- Download files from the web:  
  `wget https://example.com/file.txt`

---

## 🔐 Secure File Transfer

### 🔄 SCP (Secure Copy)
- Copy files between local and remote machines over SSH:
  - 🖥️ Local to remote: `scp file user@remote:/path/`
  - 🌍 Remote to local: `scp user@remote:/path/file .`

---

## 📂 Serving Files Over HTTP

- Use Python3's HTTP server:  
  `python3 -m http.server`
- Serves files from current directory, accessible via `curl` or `wget`
- For advanced lightweight server, consider **Updog** 🐕

---

## ⚙️ Processes

### Basics
- 🧩 Process = running program
- Each has a unique Process ID (PID)
- View processes:  
  `ps aux` or `ps`  
- Real-time monitoring:  
  `top`

### Managing Processes
- ❌ Kill a process:  
  `kill <PID>`
- Signals allow graceful termination ✋

### Process Start & Init System
- 🧱 Linux uses namespaces to isolate resources
- PID 0: Kernel process  
- PID 1: `systemd` (Ubuntu’s init system)
- Child processes managed by `systemd`

---

## 🔧 Managing Services

- Use `systemctl` to control services:
  - ▶️ Start: `systemctl start service`
  - ⏹️ Stop: `systemctl stop service`
  - 🔄 Enable on boot: `systemctl enable service`
  - 🚫 Disable on boot: `systemctl disable service`

---

## 🎭 Background & Foreground Processes

- Run command in background: append `&`  
  e.g. `long_script.sh &`
- ⏸️ Suspend running process: `Ctrl + Z`
- ▶️ Resume in foreground: `fg`
- 🔎 Check running background jobs: `jobs`

---

## ⏰ Automation with Cron

- Schedule tasks with `cron`
- Edit crontab: `crontab -e`
- Crontab format:  
  `MIN HOUR DOM MON DOW CMD`
- Example: backup every 12 hours  
  `0 */12 * * * cp -R /home/user/Documents /var/backups/`

---

## 📦 Packages & Repositories

- Ubuntu uses `apt` for package management
- ➕ Add repository:  
  `add-apt-repository ppa:name/ppa`
- 🔄 Update package list:  
  `apt update`
- 📥 Install package:  
  `apt install package-name`
- 🗑️ Remove package:  
  `apt remove package-name`
- 🔐 Add GPG keys for repository authentication

---

## 📜 System Logs

- Stored in `/var/log`
- Examples:
  - 🌐 Apache: access and error logs
  - 🔒 fail2ban (brute force monitoring)
  - 🛡️ UFW firewall logs
- Logs help monitor system health and security
- 🔄 Log rotation manages log file sizes automatically

---

## 🧠 Reflection: What I Learned & Skills Gained from Linux 3 Room (TryHackMe)

- Gained hands-on experience using **terminal text editors** like Nano and Vim, improving file editing efficiency.
- Learned to **download files** from the internet using `wget` and transfer files securely with `scp`.
- Practiced serving files locally using Python’s HTTP server and understood the basics of simple web servers.
- Developed a solid understanding of **Linux processes**, including viewing, managing, and controlling them with commands like `ps`, `kill`, and `systemctl`.
- Learned how to manage system services, including enabling and disabling them at boot using `systemctl`.
- Experienced running tasks in the **background and foreground**, improving multitasking skills on the command line.
- Gained knowledge of **automation** through scheduling jobs with `cron` and editing crontabs for repetitive tasks.
- Explored package management and repositories with `apt`, including adding third-party repositories and ensuring software integrity with GPG keys.
- Improved ability to monitor system health and security through analysis of **system logs** located in `/var/log`.
- Overall, the room enhanced my confidence navigating Linux systems, managing services, automating tasks, and handling system resources efficiently.

---

# 🪟 Windows Fundamentals Part 1 — Cheat Sheet & Learning Reflection

This cheat sheet summarizes key skills and commands from the **Windows Fundamentals Part 1** room on [TryHackMe](https://tryhackme.com/). It covers Windows OS basics, command prompt, file management, and security essentials.

---

## 📚 Table of Contents

- [Windows Command Prompt Basics](#windows-command-prompt-basics)
- [File and Folder Management](#file-and-folder-management)
- [Windows Services](#windows-services)
- [User and Permissions Management](#user-and-permissions-management)
- [Windows Networking Basics](#windows-networking-basics)
- [Windows Security Features](#windows-security-features)
- [Reflection: What I Learned](#reflection-what-i-learned)

---

## 💻 Windows Command Prompt Basics

### Opening Command Prompt
- Search for `cmd` or press `Win + R`, type `cmd`, press Enter

### Common Commands
```batch
dir             :: List files and folders in current directory
cd <path>       :: Change directory
cls             :: Clear the screen
echo <text>     :: Display text in the console
ipconfig        :: Show network adapter info and IP addresses
tasklist        :: List running processes
taskkill /PID <PID> /F  :: Force kill process by PID
```

---

## 📂 File and Folder Management

### Navigating Directories
```batch
cd ..           :: Move up one directory
cd \            :: Go to root directory
```

### File Operations
```batch
copy source destination   :: Copy files
move source destination   :: Move or rename files
del filename              :: Delete files
mkdir foldername          :: Create new folder
rmdir foldername          :: Remove empty folder
```

---

## 🛠 Windows Services

### Viewing Services
```batch
sc query
```

### Starting/Stopping Services
```batch
net start <service_name>
net stop <service_name>
```

### Task Manager Services Tab
- GUI alternative to view/manage services

---

## 👥 User and Permissions Management

### View User Accounts
```batch
net user
```

### Add New User
```batch
net user username password /add
```

### Change User Password
```batch
net user username newpassword
```

### Check Current User
```batch
whoami
```

### User Groups
- Use `net localgroup` to view groups
- Add user to group:
```batch
net localgroup groupname username /add
```

---

## 🌐 Windows Networking Basics

### Check IP Address
```batch
ipconfig
```

### Display Active Connections
```batch
netstat -an
```

### Ping a Host
```batch
ping example.com
```

### Test Network Path
```batch
tracert example.com
```

---

## 🔒 Windows Security Features

### Windows Defender
- Antivirus and malware protection built-in  
- Check status with:
```powershell
Get-MpComputerStatus
```

### Windows Firewall
- Manage via Control Panel or:
```powershell
netsh advfirewall show allprofiles
```

### User Account Control (UAC)
- Prevents unauthorized system changes by prompting for permission

---

## 🧠 Reflection: What I Learned

- Became comfortable using **Windows Command Prompt** for everyday tasks like navigating directories and managing files  
- Learned to manage **Windows services** both via CLI and Task Manager  
- Gained understanding of **user account management** commands to add, modify, and view users and groups  
- Explored **network commands** like `ipconfig`, `netstat`, `ping`, and `tracert` to troubleshoot connectivity  
- Learned about built-in **Windows security features** including Defender, Firewall, and UAC  
- Overall, I enhanced my foundational knowledge of Windows OS, which is essential for cybersecurity and system administration tasks

---

## 🔗 Related Links

- [TryHackMe: Windows Fundamentals Part 1](https://tryhackme.com/)
- [My LinkedIn Profile](https://www.linkedin.com/in/your-profile) <!-- Replace with your actual link -->

---

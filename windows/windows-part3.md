# 🪟 Windows Fundamentals Part 3 — Cheat Sheet & Learning Reflection

This cheat sheet covers key skills and commands from **Windows Fundamentals Part 3** on [TryHackMe](https://tryhackme.com/), focusing on registry editing, scheduled tasks, Windows Defender, and more.

---

## 📚 Table of Contents

- [Windows Registry Basics](#windows-registry-basics)
- [Scheduled Tasks](#scheduled-tasks)
- [Windows Defender and Security](#windows-defender-and-security)
- [Managing Services and Startup Programs](#managing-services-and-startup-programs)
- [Reflection: What I Learned](#reflection-what-i-learned)

---

## 🗂 Windows Registry Basics

### Open Registry Editor
- Press `Win + R`, type `regedit`, press Enter

### Common Registry Paths
- User settings:  
  `HKEY_CURRENT_USER\Software\`
- System settings:  
  `HKEY_LOCAL_MACHINE\Software\`

### Export Registry Key
```powershell
reg export "HKCU\Software\Example" example.reg
```

### Import Registry Key
```powershell
reg import example.reg
```

---

## ⏰ Scheduled Tasks

### View Scheduled Tasks
```powershell
schtasks /query
```

### Create a Scheduled Task
```powershell
schtasks /create /tn "TaskName" /tr "C:\path\to\script.bat" /sc daily /st 12:00
```

### Delete a Scheduled Task
```powershell
schtasks /delete /tn "TaskName"
```

---

## 🛡 Windows Defender and Security

### Check Defender Status
```powershell
Get-MpComputerStatus
```

### Quick Scan
```powershell
Start-MpScan -ScanType QuickScan
```

### Update Defender Definitions
```powershell
Update-MpSignature
```

---

## ⚙ Managing Services and Startup Programs

### Manage Services
```powershell
Get-Service
Start-Service <ServiceName>
Stop-Service <ServiceName>
```

### View Startup Programs (Task Manager GUI)
- Open Task Manager (`Ctrl + Shift + Esc`)
- Go to **Startup** tab

### Manage Startup Programs via Registry
- Path:  
  `HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run`
- Add or remove startup entries here

---

## 🧠 Reflection: What I Learned

- Gained hands-on experience with **Windows Registry Editor** for viewing and modifying system and user settings  
- Learned to create, view, and delete **scheduled tasks** for automation and task scheduling  
- Explored Windows Defender's command-line management for antivirus status and scanning  
- Improved understanding of managing **services** and controlling startup programs both via PowerShell and Registry  
- Overall, enhanced my Windows administration and security skills, crucial for system hardening and incident response

---

## 🔗 Related Links

- [TryHackMe: Windows Fundamentals Part 3](https://tryhackme.com/)

---

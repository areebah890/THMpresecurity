# 🪟 Windows Fundamentals Part 2 — Cheat Sheet & Learning Reflection

This cheat sheet summarizes key concepts and commands from **Windows Fundamentals Part 2** on [TryHackMe](https://tryhackme.com/), covering file permissions, PowerShell basics, event logs, and more.

---

## 📚 Table of Contents

- [File Permissions and Attributes](#file-permissions-and-attributes)
- [PowerShell Basics](#powershell-basics)
- [Windows Event Logs](#windows-event-logs)
- [Process and Service Management](#process-and-service-management)
- [Basic Windows Networking](#basic-windows-networking)
- [Reflection: What I Learned](#reflection-what-i-learned)

---

## 🔐 File Permissions and Attributes

### View File Permissions
```powershell
icacls filename
```

### Modify Permissions
```powershell
icacls filename /grant UserName:F
```
- `F` = Full control, other flags include `R` (Read), `W` (Write), etc.

### View File Attributes
```powershell
attrib filename
```

### Change Attributes
```powershell
attrib +r filename    # Set Read-only attribute
attrib -r filename    # Remove Read-only attribute
attrib +h filename    # Set Hidden attribute
attrib -h filename    # Remove Hidden attribute
```

---

## 🐚 PowerShell Basics

### Launch PowerShell
- Type `powershell` in Command Prompt or Start menu

### Common Commands
```powershell
Get-Help <cmdlet>            # Get help for a command
Get-Process                  # List running processes
Stop-Process -Id <PID>       # Stop process by PID
Get-Service                  # List services
Start-Service <name>         # Start a service
Stop-Service <name>          # Stop a service
```

### Running Scripts
- Execution Policy may restrict scripts:
```powershell
Set-ExecutionPolicy RemoteSigned
```

---

## 📜 Windows Event Logs

### View Logs with Event Viewer (GUI)
- Access by searching “Event Viewer”

### View Logs via PowerShell
```powershell
Get-EventLog -LogName System -Newest 10
Get-EventLog -LogName Security -Newest 10
```

- Useful logs:  
  - **System**: OS and hardware events  
  - **Application**: Application errors/warnings  
  - **Security**: Login attempts, audit logs

---

## ⚙️ Process and Service Management

### List Processes
```powershell
Get-Process
```

### Kill Process
```powershell
Stop-Process -Name notepad
Stop-Process -Id <PID>
```

### Manage Services
```powershell
Get-Service
Start-Service <serviceName>
Stop-Service <serviceName>
```

---

## 🌐 Basic Windows Networking

### Check IP Configuration
```powershell
Get-NetIPAddress
```

### Test Network Connection
```powershell
Test-Connection example.com
```

### View Active Connections
```powershell
Get-NetTCPConnection
```

---

## 🧠 Reflection: What I Learned

- Learned to inspect and modify **file permissions and attributes** using `icacls` and `attrib`  
- Gained foundational skills in **PowerShell**, including managing processes, services, and running scripts  
- Explored **Windows Event Logs** through Event Viewer and PowerShell to troubleshoot system and security events  
- Improved ability to control and monitor **processes and services** via PowerShell commands  
- Enhanced knowledge of basic Windows networking commands and diagnostics in PowerShell  
- Overall, this deepened my understanding of Windows internals and administrative tools critical for cybersecurity and system administration

---

## 🔗 Related Links

- [TryHackMe: Windows Fundamentals Part 2](https://tryhackme.com/)

---

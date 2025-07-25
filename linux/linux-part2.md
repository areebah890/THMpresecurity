# Linux Part 2 – SSH, File Commands & Permissions

## 🔐 SSH – Secure Shell

SSH (Secure Shell) is how we connect to a remote Linux machine’s terminal securely. In this room, I worked with two machines:
- My Linux target machine
- The TryHackMe AttackBox (used to connect via SSH)

SSH encrypts everything sent between machines, so no one can snoop on the commands or data being transferred.

---

## 🧠 How SSH Works

SSH is just a protocol that takes your readable input and encrypts it using cryptography, sends it across the network, and then decrypts it on the other end.

It lets you run commands on a remote machine as if you were sitting in front of it.

---

## 🔑 Logging into Linux with SSH

To SSH into a machine, all I need is:
1. The machine’s IP address
2. A valid username and password

Basic syntax:
ssh username@IP_address


---

## ⚙️ Flags & Switches

Most Linux commands let you tweak their behavior using **flags** (also called switches). They're added after the command with `-` or `--`.

Example:
- `ls` shows files and folders in the current directory
- `ls -a` includes hidden files too

If I’m not sure what flags are available, I can use:
command --help

This gives me a quick overview of the options. For more details, I can check the **manual page** using:
man command


---

## 📚 Using `man` Pages

Manual pages are full documentation built into Linux. Super helpful when learning what a command does. man <command>

Example:
man ls

Will explain that:
- `-h` or `--human-readable` shows sizes like `1K`, `234M`, `2G`, etc.

---

## 🛠️ Creating & Managing Files

### 📝 Creating Files and Folders
- `touch filename` → makes a blank file  
  Example:
touch note

- `mkdir foldername` → makes a new folder

📸 

<img width="317" height="67" alt="image" src="https://github.com/user-attachments/assets/b9c64b54-46d0-4b9e-bdff-885358c6dd76" />

<img width="314" height="89" alt="image" src="https://github.com/user-attachments/assets/e4adbd6c-32f7-4139-aa07-4877583636b9" />


---

### 🗑️ Removing Files and Folders
- `rm filename` → deletes a file
- `rm -R foldername` → deletes a folder **recursively**

---

### 📁 Copying and Moving

- `cp file1 file2` → copies contents of `file1` into a new file `file2`
- `mv file new_location/` → moves file to another folder
- `mv old_name new_name` → renames a file

📸 

<img width="775" height="175" alt="image" src="https://github.com/user-attachments/assets/d26796d1-fa6a-4fd4-aebf-da4ac4f59288" />


### 📂 Figuring Out File Types

Sometimes files don’t have extensions, so I can’t tell what they are just by looking.  
To find out:
file filename

This command will tell me what type of file it actually is.

📸 

<img width="764" height="170" alt="image" src="https://github.com/user-attachments/assets/2af1f011-6e16-4f06-8c15-9bbabef6d1a1" />


## 🔐 Permissions Basics

Files and folders in Linux have permissions that decide:
- Who can **read**
- Who can **write**
- Who can **execute**

There are 3 types of users:
- The file **owner**
- The **group** the file belongs to
- **Others** (everyone else)

Example output from `ls -l`:
-rwxr-xr--


📸 

<img width="363" height="83" alt="image" src="https://github.com/user-attachments/assets/65d70f8c-bc1e-4940-8e56-f1f968e577b6" />


---

## 👥 Users vs Groups

In Linux, you can have different permissions set for:
- An individual user (owner)
- A group of users

So for example, a web server might have write access to upload logs, but regular users should only be able to view or upload their own files — not mess with each other’s.

---

## 🔄 Switching Users

To switch between users:
su username

You’ll need the user’s password. If you add `-l`, you’ll get that user’s full environment:

su -l username


---

## 📁 Common Linux Directories

Here are some important system directories I learned about:

| Path | What it’s for |
|------|----------------|
| `/etc` | System config files (like `sudoers`) |
| `/var` | Variable data (e.g. logs in `/var/log`) |
| `/root` | Home folder for the root user |
| `/tmp` | Temporary files — wiped on reboot |

📸
<img width="940" height="586" alt="image" src="https://github.com/user-attachments/assets/b158417a-edbc-48ae-8896-59a625ef97fe" />


## ✅ Recap

This part covered a lot of foundational stuff. I learned:
- How to connect to a Linux machine remotely using SSH
- How to use flags and `man` pages to better understand commands
- File system operations (create, copy, move, delete)
- How to check file types and understand permissions
- How to switch users
- What key Linux system folders are and what they’re for

This was a pretty theory-heavy room, so I’ll probably come back and redo parts of it for practice. 🧠






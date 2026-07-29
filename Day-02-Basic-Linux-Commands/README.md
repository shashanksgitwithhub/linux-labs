<p align="center">
  <img src="https://img.shields.io/badge/Linux-Basics-blue" alt="AWS Badge">
</p>


# 🐧 Day-02 - Basic Linux Commands

## Objective

The objective of this lab is to understand and practice basic Linux commands used for navigating the file system, managing files and directories, retrieving system information, and configuring OpenSSH Server for a better command-line experience.

---

# Topics Covered

- pwd
- ls
- cd
- mkdir
- touch
- cp
- mv
- rm
- clear
- whoami
- hostname
- Hidden Files
- OpenSSH Server Installation
- SSH Remote Login

---

# Theory

## What is a Linux Command?

A Linux command is an instruction entered in the terminal to perform a specific task such as creating files, navigating directories, or managing the operating system.

General Syntax:

```bash
command [options] [arguments]
```

Example:

```bash
ls -l
```

Where:

- `ls` → Command
- `-l` → Option

---

## 1. pwd (Print Working Directory)

Displays the current directory.

```bash
pwd
```

---

## 2. ls (List)

Displays files and directories.

```bash
ls
```

Useful options:

```bash
ls -l
ls -a
ls -la
```

---

## 3. cd (Change Directory)

Changes the current working directory.

Examples:

```bash
cd Documents
cd ..
cd
cd /
```

---

## 4. mkdir (Make Directory)

Creates a new directory.

```bash
mkdir LinuxLabs
```

---

## 5. touch

Creates an empty file.

```bash
touch notes.txt
```

---

## 6. cp (Copy)

Copies files or directories.

```bash
cp notes.txt backup.txt
```

---

## 7. mv (Move / Rename)

Rename a file

```bash
mv notes.txt linux_notes.txt
```

Move a file

```bash
mv linux_notes.txt Documents/
```

---

## 8. rm (Remove)

Delete a file

```bash
rm filename
```

Delete a directory

```bash
rm -r directory_name
```

---

## 9. clear

Clears the terminal screen.

```bash
clear
```

Shortcut:

```text
Ctrl + L
```

---

## 10. whoami

Displays the current logged-in user.

```bash
whoami
```

---

## 11. hostname

Displays the hostname of the Linux machine.

```bash
hostname
```

---

## 12. Hidden Files

Linux hides files by placing a dot (`.`) at the beginning of the filename.

Hide a file

```bash
mv notes.txt .notes.txt
```

View hidden files

```bash
ls -a
```

View hidden files with details

```bash
ls -la
```

Unhide a file

```bash
mv .notes.txt notes.txt
```

---

## 13. OpenSSH Server

OpenSSH allows secure remote access to a Linux machine over the network using SSH (Secure Shell). Instead of working directly in the VirtualBox console, SSH provides a much better command-line experience with easy copy/paste, better scrolling, and remote administration capabilities.

### Install OpenSSH Server

```bash
sudo apt update
sudo apt install openssh-server -y
```

### Start SSH Service

```bash
sudo systemctl start ssh
```

### Enable SSH at Boot

```bash
sudo systemctl enable ssh
```

### Verify SSH Status

```bash
sudo systemctl status ssh
```

---

## 14. SSH Remote Login

After installing OpenSSH Server and connecting the VM using a Bridged Network Adapter, the Ubuntu server can be accessed directly from Windows.

Example:

```bash
ssh supermann@192.168.1.45
```

This eliminates the need to work continuously in the VirtualBox console and provides a professional Linux administration experience.

---

# Practical Performed

Performed the following tasks:

- Navigated directories using `pwd` and `cd`
- Listed files using `ls`
- Created directories using `mkdir`
- Created files using `touch`
- Copied files using `cp`
- Renamed files using `mv`
- Deleted files using `rm`
- Cleared the terminal using `clear`
- Verified username using `whoami`
- Displayed hostname using `hostname`
- Practiced creating and viewing hidden files
- Installed OpenSSH Server
- Started and enabled the SSH service
- Verified the SSH service status
- Connected to the Ubuntu Server remotely from Windows using SSH

---

# Commands Used

```bash
pwd
ls
ls -l
ls -a
ls -la
cd
cd ..
cd /
mkdir LinuxLabs
touch notes.txt
cp notes.txt backup.txt
mv notes.txt linux_notes.txt
rm linux_notes.txt
clear
whoami
hostname

mv notes.txt .notes.txt
ls -a
ls -la
mv .notes.txt notes.txt

sudo apt update
sudo apt install openssh-server -y
sudo systemctl start ssh
sudo systemctl enable ssh
sudo systemctl status ssh
hostname -I

ssh supermann@192.168.1.45
```

---

# Practice Lab

### Task 1

Create a directory named:

```text
Linux_Practice
```

### Task 2

Move into it.

### Task 3

Create three files.

```text
file1.txt
file2.txt
file3.txt
```

### Task 4

Rename `file1.txt` to:

```text
notes.txt
```

### Task 5

Copy `notes.txt` to:

```text
backup.txt
```

### Task 6

Delete `file2.txt`.

### Task 7

Create a hidden file and verify it using `ls -a`.

### Task 8

Install OpenSSH Server and verify the SSH service.

### Task 9

Connect to the Ubuntu Server from Windows using SSH.

---

# Interview Questions

### 1. What does the `pwd` command do?

**Answer:** Displays the current working directory.

---

### 2. What is the difference between `cp` and `mv`?

**Answer:** `cp` copies files, whereas `mv` moves or renames files.

---

### 3. How do you view hidden files?

**Answer:** Use `ls -a`.

---

### 4. How do you hide a file in Linux?

**Answer:** Rename it by adding a dot (`.`) at the beginning of the filename.

---

### 5. What is OpenSSH?

**Answer:** OpenSSH is a secure remote access service that allows users to connect to Linux systems using the SSH protocol.

---

### 6. Which command is used to check the SSH service status?

**Answer:**

```bash
sudo systemctl status ssh
```

---

# Screenshots

- Current Working Directory (`pwd`, `hostname`, `whoami`)<img width="1907" height="896" alt="Screenshot 2026-07-29 133523" src="https://github.com/user-attachments/assets/8290e40d-6b52-4f35-bb49-77c1e8442c93" />

- Listing Files (`ls -la`)<img width="1901" height="490" alt="Screenshot 2026-07-29 133621" src="https://github.com/user-attachments/assets/8076c109-d027-4636-a54b-57d4d5c0d3f8" />

- Creating Directories and Files (`mkdir`, `touch`)<img width="1907" height="373" alt="Screenshot 2026-07-29 134043" src="https://github.com/user-attachments/assets/bb5b5a86-c372-44ac-8c69-8192e3ef9ef0" />

- Copying and Renaming Files (`cp`, `mv`)<img width="1907" height="319" alt="Screenshot 2026-07-29 140736" src="https://github.com/user-attachments/assets/52939ddf-4225-46ab-9604-144b58016d83" />
  <img width="1906" height="291" alt="Screenshot 2026-07-29 141350" src="https://github.com/user-attachments/assets/4fafa306-5f53-46e3-bf46-b02aefacbc1e" />

- Hidden Files (`ls -a`)<img width="1905" height="301" alt="Screenshot 2026-07-29 141540" src="https://github.com/user-attachments/assets/430daac1-7e42-4fa0-ac72-3b7150ab7c87" />

- SSH Service Status<img width="1337" height="852" alt="Screenshot 2026-07-29 133215" src="https://github.com/user-attachments/assets/c291eaa1-c207-4760-919a-c35ad4b6a3ae" />

- SSH Login from Windows Terminal<img width="1907" height="942" alt="Screenshot 2026-07-29 133406" src="https://github.com/user-attachments/assets/d795a6d6-f8ea-457b-aaad-9ae6e6a94aa4" />


---

# Conclusion

In this lab, I learned the fundamental Linux commands required for file and directory management, navigation, hidden file handling, and basic system information. I also installed and configured OpenSSH Server, enabling secure remote access to the Ubuntu Server from Windows using SSH. This setup provides a more efficient and professional environment for practicing Linux system administration and forms a strong foundation for future DevOps, Cloud Computing, and AWS administration tasks.

---

# Linux Fundamentals

> Documenting my Linux Fundamentals learning journey — concepts, commands, and hands-on notes organized by topic.

---

## About This Repository

This repository is a personal knowledge base where I document everything I learn about Linux — from core concepts and the file system to working with text files and commands. It is built as both a learning reference and a portfolio piece to demonstrate hands-on Linux knowledge.

---

## Repository Structure

```
Linux-Fundamentals/
├── README.md          <- You are here
├── Basics.md          <- Linux fundamentals, architecture, shell, and core commands
├── FileSystem.md      <- Linux file system hierarchy, navigation, and management
└── TextFiles.md       <- Viewing, editing, and manipulating text files in Linux
```

---

## What's Covered

### [Basics.md](./Basics.md)

Core Linux concepts and essential commands for getting started.

---

### [FileSystem.md](./FileSystem.md)

Linux file system structure, hierarchy, and how to work with it.

---

### [TextFiles.md](./TextFiles.md)

Commands and techniques for viewing, searching, and manipulating text files.

---

## Key Linux Commands Quick Reference

**Navigation**
```bash
pwd           # Print current working directory
ls -la        # List all files with details
cd /path      # Change directory
```

**File Operations**
```bash
touch file    # Create an empty file
cp src dest   # Copy file
mv src dest   # Move or rename file
rm file       # Delete file
mkdir dir     # Create directory
```

**Viewing Files**
```bash
cat file      # Display file contents
less file     # Scroll through file
head -n 10    # Show first 10 lines
tail -n 10    # Show last 10 lines
grep "text"   # Search for pattern
```

**Permissions**
```bash
chmod 755 file       # Set file permissions
chown user:group file # Change ownership
ls -l                # View permissions
```

**Finding Files**
```bash
find / -name "file"  # Find file by name
locate filename      # Fast file search
which command        # Locate a command
```

---

## Linux File System Hierarchy Overview

```
/ (root)
├── /bin       — Essential user binaries (ls, cp, mv)
├── /etc       — Configuration files
├── /home      — User home directories
├── /var       — Variable data (logs, mail)
├── /tmp       — Temporary files
├── /usr       — User programs and utilities
├── /opt       — Optional/third-party software
├── /root      — Root user's home directory
├── /dev       — Device files
├── /proc      — Virtual filesystem for process info
├── /sys       — Virtual filesystem for kernel/hardware info
└── /mnt       — Mount points for external drives
```

---

## Why Linux?

Linux is the foundation of modern computing infrastructure. It powers:
- Web servers and cloud platforms (AWS, GCP, Azure)
- Cybersecurity tools and penetration testing environments (Kali Linux)
- Android mobile operating system
- Embedded systems and IoT devices
- Supercomputers and research systems

For anyone pursuing a career in cybersecurity, DevOps, cloud, or software development, Linux knowledge is essential.

---

## Contributing

This is a personal learning repository. If you spot an error or want to suggest an improvement, feel free to open an **issue** or submit a **pull request**.

---

## License

This project is licensed under the [MIT License](LICENSE).

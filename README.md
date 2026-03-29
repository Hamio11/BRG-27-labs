# BRG-27-labs

Lab work and documentation for Introduction to Server Environments and Architectures

## Session 1 – Setting Up Linux

### GitHub Account and Repository
Created a GitHub account and created a repository for this module to document lab progress and store screenshots.

Repository link: https://github.com/Hamio11/BRG-27-labs

### Installation of Virtual Machine
Downloaded and installed Oracle VirtualBox and used it to set up an Ubuntu virtual machine for the lab exercises.

Configuration used:
- Operating System: Ubuntu Linux
- Memory: 4GB RAM
- Hard Drive: 20GB virtual disk

### Basic Linux Navigation
I practised basic Linux commands using the command-line interface (CLI) to navigate through directories and create files and folders.

Commands used:
```bash
pwd
ls
cd ~
mkdir -p isea-lab1
cd ~/isea-lab1
touch notes.txt
ls
ls -l
help cd
```

Explanation:
- `pwd` shows the current working directory
- `ls` lists files and directories
- `cd ~` moves to the home directory
- `mkdir -p isea-lab1` creates a new folder
- `touch notes.txt` creates a new file
- `ls -l` shows files in long-list format including permissions
- `help cd` displays help for the `cd` command

### Exploring the Linux File Structure
I explored important Linux directories to better understand the file system structure.

Commands used:
```bash
cd /etc
pwd
cd /var
pwd
cd /home
pwd
cd ~/isea-lab1
```

Explanation:
- `/etc` contains system configuration files
- `/var` contains variable data such as logs and cache
- `/home` contains user home directories

### Linux Service Management
I used `systemctl` to view and check Linux services running on the system.

Commands used:
```bash
systemctl list-units --type=service
systemctl status snapd
```

Explanation:
- `systemctl list-units --type=service` lists active service units
- `systemctl status snapd` checks the status of the `snapd` service

### File Permissions
I learnt how to view and change file permissions in Linux.

Commands used:
```bash
touch test.sh
ls -l
chmod 755 test.sh
ls -l
```

Explanation:
- `touch test.sh` creates a test file
- `ls -l` shows the file permissions before and after changes
- `chmod 755 test.sh` changes permissions for the file

Meaning of `755`:
- Owner = read, write, execute
- Group = read, execute
- Others = read, execute

### Searching in the File System
I used `find` and `grep` to search for files and text inside files.

Commands used:
```bash
echo "test line" > notes.txt
find ~/isea-lab1 -name "test.sh"
grep -r "test" ~/isea-lab1
```

Explanation:
- `echo "test line" > notes.txt` writes sample text into the file
- `find ~/isea-lab1 -name "test.sh"` searches for the file by name
- `grep -r "test" ~/isea-lab1` searches recursively for the word `test` inside files

### Screenshots

#### GitHub Repository
![GitHub Repository](<Screenshot 2026-03-29 185829.png>)

#### Ubuntu / VirtualBox
![Ubuntu VirtualBox](<Screenshot 2026-03-29 190322.png>)

#### Linux Commands / Services
![Linux Commands](<Screenshot 2026-03-29 190528.png>)

#### Permissions / Search
![Permissions and Search](<Screenshot 2026-03-29 190903.png>)

### Reflection
In this session, I learnt how to set up Ubuntu in VirtualBox and use the Linux terminal for basic tasks. I practised navigating directories, creating files and folders, checking Linux services, changing file permissions, and searching for files and text. Exploring directories such as `/etc`, `/var`, and `/home` helped me understand the Linux file structure better. Overall, this session helped me become more familiar and confident with using the Linux command line.

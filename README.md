### GitHub account & Repository

Created a GitHub account on https://github.com/ and created a repository for this module.

Repository link: https://github.com/Hamio11/BRG-27-labs

### Installation of Virtual Machine

Downloaded and installed Oracle VirtualBox and created an Ubuntu virtual machine.

Configuration used:
* Linux OS: Ubuntu
* Memory: 4GB
* Hard drive: 20GB

### Basic Linux Navigation

I learnt basic Linux commands using the command-line interface (CLI) to move around the file system and create files and folders.

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
cd /etc
pwd
cd /var
pwd
cd /home
pwd
cd ~/isea-lab1
help cd
```

### Linux Service Management

I used `systemctl` commands to view and check Linux services.

Commands used:
```bash
systemctl list-units --type=service
systemctl status snapd
```

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
* `ls -l` shows the current file permissions
* `chmod 755 test.sh` changes the permissions of the file
* `755` means:
  * Owner = read, write, execute
  * Group = read, execute
  * Others = read, execute

### Searching in the File System

I used commands to search for files and text inside files.

Commands used:
```bash
echo "test line" > notes.txt
find ~/isea-lab1 -name "test.sh"
grep -r "test" ~/isea-lab1
```

Explanation:
* `find` is used to search for a file by name
* `grep -r` is used to search for text recursively in files inside a directory

### Reflection

In this session, I learnt how to set up Ubuntu in VirtualBox and use the Linux terminal for basic tasks. I practised navigating directories, creating files and folders, checking Linux services, changing file permissions, and searching for files and text. This session helped me become more familiar and confident with using the Linux command line.

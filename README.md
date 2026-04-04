# BRG-27-labs

Lab work and documentation for Introduction to Server Environments and Architectures


Student Name : Irham Irsyad Bin Azman

Kaplan Student ID : CT0391096

Murdoch Student ID : 36061621

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
man ls
```

Explanation:
- `/etc` contains system configuration files
- `/var` contains variable data such as logs and cache
- `/home` contains user home directories
- `man ls` displays the manual page for the `ls` command

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
echo "test" > notes.txt
find ~/isea-lab1 -name "test.sh"
grep -r "test" ~/isea-lab1
```

Explanation:
- `echo "test" > notes.txt` writes sample text into the file
- `find ~/isea-lab1 -name "test.sh"` searches for the file by name
- `grep -r "test" ~/isea-lab1` searches recursively for the word `test` inside files

### Screenshots

#### Basic Linux Navigation and File Structure
![Basic Linux Navigation and File Structure](<./Screenshot 2026-03-29 185829.png>)

#### Linux Service Management
![Linux Service Management](<./Screenshot 2026-03-29 190322.png>)

#### File Permissions
![File Permissions](<./Screenshot 2026-03-29 190528.png>)

#### File Search and Command Help
![File Search and Command Help](<./Screenshot 2026-03-29 190903.png>)

### Reflection
In this session, I learnt how to set up Ubuntu in VirtualBox and use the Linux terminal for basic tasks. I practised navigating directories, creating files and folders, checking Linux services, changing file permissions, and searching for files and text. Exploring directories such as `/etc`, `/var`, and `/home` helped me understand the Linux file structure better. Overall, this session helped me become more familiar and confident with using the Linux command line.

## Session 2 – Total Cost of Ownership and Cloud Services

### Session 2a – Total Cost of Ownership (TCO)

For this session, I explored Total Cost of Ownership (TCO) by reviewing a cloud pricing estimate and using it as part of a cost analysis exercise. The purpose of this activity was to understand how cloud infrastructure costs can be estimated and analysed in a practical IT environment.

### TCO Activity
I used a cloud pricing estimate export to review the projected cost of running infrastructure and related services in the cloud. The estimate included several services and showed the monthly and yearly cost of the deployment.

Estimate summary:
- Upfront cost: USD 0
- Monthly cost: USD 10,330.64
- Total 12 months cost: USD 123,967.68

Main services included in the estimate:
- Windows Server and SQL Server on Amazon EC2: USD 3,631.85/month
- Amazon RDS for MySQL: USD 2,477.65/month
- AWS DRS - Replication: USD 4,221.14/month
- AWS DRS - Drill/Recovery: USD 0/month

### TCO Reflection
This activity helped me understand that cloud pricing can be broken down into service-level costs and reviewed over time using monthly and yearly estimates. It also showed how TCO can support IT infrastructure planning and decision-making by highlighting the ongoing operational cost of cloud-based solutions. From this activity, I learned that cloud deployment may reduce upfront hardware investment, but long-term running costs still need to be analysed carefully.


### Session 2b – Cloud Services (Azure Ubuntu VM)

For this session, I created and configured an Ubuntu virtual machine in Microsoft Azure. This lab focused on cloud deployment, remote access using SSH, updating the server, and running a simple Bash script.

### Azure Virtual Machine Configuration
Configuration used:
- Cloud platform: Microsoft Azure
- Virtual machine name: IrhamVM
- Operating system: Ubuntu 24.04 LTS
- Region: Norway East
- VM size: Standard B2ats v2
- Authentication type: SSH public key

### SSH Connection
After creating the Ubuntu VM, I connected to it remotely using SSH through Git Bash on Windows.

Commands used:
```bash
cd /c/Users/Irham/Downloads/Key
ls
chmod 400 KaplanUbuntuKey.pem
ssh -i KaplanUbuntuKey.pem admin123@20.251.161.207
```

Explanation:
- `cd /c/Users/Irham/Downloads/Key` moved to the folder containing the private key
- `ls` displayed the key file
- `chmod 400 KaplanUbuntuKey.pem` secured the private key file
- `ssh -i KaplanUbuntuKey.pem admin123@20.251.161.207` connected to the Azure Ubuntu VM

### Package Update and Upgrade
After connecting to the VM, I updated the package list and upgraded the installed packages.

Commands used:
```bash
sudo apt update
sudo apt upgrade -y
```

Explanation:
- `sudo apt update` refreshed the package list from the repositories
- `sudo apt upgrade -y` installed available package upgrades automatically

### Bash Scripting
I created and ran a simple Bash script on the Azure Ubuntu VM.

Commands used:
```bash
nano script.sh
chmod +x script.sh
./script.sh
```

Script content:
```bash
#!/bin/bash
echo "Hello from Azure VM"
date
pwd
```

Explanation:
- `nano script.sh` created and edited the script file
- `chmod +x script.sh` made the script executable
- `./script.sh` executed the script

### Script Output
The script successfully displayed:
- a custom message
- the current date and time
- the current working directory

### Screenshots

#### Azure VM Creation
![Azure VM Creation](<./Screenshot 2026-03-29 165759.png>)

#### Azure VM Review and Create
![Azure VM Review and Create](<./Screenshot 2026-03-29 170435.png>)

#### Azure Ubuntu VM Overview
![Azure Ubuntu VM Overview](<./Screenshot 2026-03-29 170702.png>)

#### SSH Connection to Azure Ubuntu VM
![SSH Connection](<./Screenshot 2026-04-04 111307.png>)

#### Package Update
![Package Update](<./Screenshot 2026-04-04 111610.png>)

#### Package Upgrade
![Package Upgrade](<./Screenshot 2026-04-04 112054.png>)

#### Bash Script Output
![Bash Script Output](<./Screenshot 2026-04-04 112233.png>)

### Reflection
In this session, I learned how cloud deployment works in a practical environment. The TCO activity helped me understand how cost information can be used to support infrastructure decisions. Creating an Ubuntu virtual machine in Azure, connecting with SSH, updating packages, and running a Bash script helped me understand how Linux servers can be deployed and managed in the cloud. This session improved my confidence in using both cloud services and command-line tools.

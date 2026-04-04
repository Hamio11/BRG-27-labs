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

## Session 3 – DNS, Certificates, and Server Automation

### Session 3a – DNS and Digital Certificates

In this session, I configured DNS for my Azure Ubuntu virtual machine and secured the web server using a Let's Encrypt certificate with Certbot.

#### DNS Configuration
I created a DuckDNS hostname and mapped it to the public IP address of my Azure Ubuntu virtual machine.

Details:
- Domain name: `isea-test.duckdns.org`
- Azure VM public IP: `20.251.161.207`

#### DNS Verification
I verified that the domain name resolved correctly to the public IP address of the Azure VM.

Command used:
```bash
nslookup isea-test.duckdns.org
```

This confirmed that the DNS record was pointing to the correct server.

#### Azure Network Security Rules
To make the server accessible from the internet, I configured Azure inbound rules for:
- SSH (22)
- HTTP (80)
- HTTPS (443)

These rules allowed secure remote access to the VM and enabled web traffic over both HTTP and HTTPS.

#### Web Server Setup
I installed and started Nginx on the Azure Ubuntu VM, then created a simple test page.

Commands used:
```bash
sudo apt update
sudo apt install -y nginx curl
sudo systemctl enable --now nginx
echo "<h1>Session 3 DNS and HTTPS Test</h1>" | sudo tee /var/www/html/index.html
curl http://localhost
```

Explanation:
- `sudo apt install -y nginx curl` installed the Nginx web server and curl
- `sudo systemctl enable --now nginx` started Nginx and enabled it to start automatically at boot
- `echo ... | sudo tee /var/www/html/index.html` created the web page
- `curl http://localhost` tested the page locally on the server

#### HTTP Test
After configuring Nginx and opening port 80 in Azure, I tested the website in the browser using:

`http://isea-test.duckdns.org`

The page loaded successfully, confirming that the DNS record and HTTP service were working correctly.

#### HTTPS Certificate with Certbot
After confirming that the site was available over HTTP, I installed Certbot and requested a Let's Encrypt certificate for the domain.

Commands used:
```bash
sudo snap install --classic certbot
sudo ln -s /snap/bin/certbot /usr/local/bin/certbot
sudo certbot --nginx -d isea-test.duckdns.org
```

Explanation:
- `sudo snap install --classic certbot` installed Certbot
- `sudo ln -s /snap/bin/certbot /usr/local/bin/certbot` made the `certbot` command accessible system-wide
- `sudo certbot --nginx -d isea-test.duckdns.org` requested and deployed the certificate for the Nginx web server

The certificate was issued successfully and deployed to Nginx, which enabled HTTPS for the domain.

#### Certificate Renewal Test
I also tested the certificate renewal process to confirm that automatic renewal had been configured correctly.

Command used:
```bash
sudo certbot renew --dry-run
```

This simulated the renewal process successfully.

### Session 3b – Server Automation

In this session, I created a simple automation script on the Azure Ubuntu VM to run an update task and write the output to a log file. I then scheduled the script using cron so it could run automatically.

#### Automation Script
I created a script called `update_task.sh` to automate package update checks and record the output in a log file.

Commands used:
```bash
nano update_task.sh
chmod +x update_task.sh
sudo ./update_task.sh
sudo cat /var/log/task.log
```

Script content:
```bash
#!/bin/bash
echo "Task started: $(date)" >> /var/log/task.log
apt update >> /var/log/task.log 2>&1
echo "Task completed: $(date)" >> /var/log/task.log
echo "------------------------------" >> /var/log/task.log
```

Explanation:
- `nano update_task.sh` created and edited the script
- `chmod +x update_task.sh` made the script executable
- `sudo ./update_task.sh` ran the script manually
- `sudo cat /var/log/task.log` displayed the log file contents

#### Cron Scheduling
After testing the script manually, I scheduled it using cron so it would run automatically every day at 9:00 AM.

Commands used:
```bash
sudo crontab -e
sudo crontab -l
```

Cron entry:
```bash
0 9 * * * /home/admin123/update_task.sh
```

Explanation:
- `sudo crontab -e` opened the cron editor
- `0 9 * * * /home/admin123/update_task.sh` schedules the task to run every day at 9:00 AM
- `sudo crontab -l` displayed the saved cron jobs

### Screenshots

#### DNS Verification
![DNS Verification](<./Screenshot 2026-04-04 170638.png>)

#### SSH Connection and Package Update
![SSH Connection and Package Update](<./Screenshot 2026-04-04 170613.png>)

#### Azure Network Security Rules
![Azure Network Security Rules](<./Screenshot 2026-04-04 164930.png>)

#### Local Web Server Test
![Local Web Server Test](<./Screenshot 2026-04-04 171041.png>)

#### HTTP Website Test
![HTTP Website Test](<./Screenshot 2026-04-04 171229.png>)

#### Certbot Certificate Deployment
![Certbot Certificate Deployment](<./Screenshot 2026-04-04 171926.png>)

#### Certificate Renewal Test
![Certificate Renewal Test](<./Screenshot 2026-04-04 172228.png>)

#### Script Execution and Log Output
![Script Execution and Log Output](<./Screenshot 2026-04-04 175751.png>)

#### Cron Job Configuration
![Cron Job Configuration](<./Screenshot 2026-04-04 175848.png>)

### Reflection
In this session, I learnt how to connect a domain name to a cloud server using DNS and how to make a website available through Nginx. I also learnt how Azure network security rules affect web access and how Let's Encrypt certificates can be installed using Certbot to secure a website with HTTPS. For the automation part, I created a shell script to record update activity in a log file and scheduled it with cron to run automatically. This session improved my understanding of DNS, web server configuration, certificate management, and Linux server automation in a cloud environment.

## Session 4 – Additional Server Service and Final Documentation

### Session 4a – Additional Server Service (MySQL)

For this session, I installed and tested an additional server service on my Azure Ubuntu virtual machine. I chose MySQL because it is a widely used database server and is commonly used in Linux server environments.

### MySQL Installation
I installed MySQL Server on the Azure Ubuntu virtual machine after updating the package list.

Commands used:
```bash
sudo apt update
sudo apt install mysql-server -y

Explanation:

sudo apt update refreshed the package list from the repositories
sudo apt install mysql-server -y installed MySQL Server and required packages automatically

MySQL Service Status

After installation, I checked the MySQL service to confirm that it was running correctly on the server.

Command used:

sudo systemctl status mysql

Explanation:

sudo systemctl status mysql displayed the status of the MySQL service
The output showed that the service was active and running

Logging in to MySQL

I logged in to the MySQL server using the root account through the terminal.

Command used:

sudo mysql

Explanation:

sudo mysql opened the MySQL command-line interface using administrative access
Creating a Test Database

To test that MySQL was working properly, I created a sample database and displayed the list of databases.

Commands used:

CREATE DATABASE labdb;
SHOW DATABASES;
EXIT;

Explanation:

CREATE DATABASE labdb; created a new test database called labdb
SHOW DATABASES; displayed all available databases, including the new database
EXIT; closed the MySQL interface

Creating a Table and Inserting Data

To further test the MySQL server, I created a simple table inside the test database, inserted a sample record, and displayed the stored data.

Commands used:

USE labdb;
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50) NOT NULL
);
INSERT INTO users (name) VALUES ('Test User');
SELECT * FROM users;
EXIT;

Explanation:

USE labdb; selected the test database
CREATE TABLE users (...) created a table named users
INSERT INTO users (name) VALUES ('Test User'); inserted a sample row into the table
SELECT * FROM users; displayed the stored data to confirm the table and insert operation worked correctly
EXIT; closed the MySQL interface

Basic Functionality Test

The MySQL server was successfully installed, started, and tested. I was able to:

![MySQL Installation](<./Screenshot 2026-04-04 184857.png>)
![MySQL Service Status](<./Screenshot 2026-04-04 185002.png>)
![Creating the Test Database](<./Screenshot 2026-04-04 185116.png>)
![Creating Table and Inserting Data](<./Screenshot 2026-04-04 185338.png>)


This confirmed that the additional server service was installed and functioning correctly.

Reflection

In this session, I learned how to install and test an additional server service on a Linux cloud server. By installing MySQL, checking the service status, creating a database, creating a table, and inserting sample data, I gained a better understanding of how database services are managed on Ubuntu. This session helped me improve my practical knowledge of server administration and basic database setup in a cloud environment.

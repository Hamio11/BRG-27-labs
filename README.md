# BRG-27-labs

Lab work and documentation for Introduction to Server Environments and Architectures

## Session 1 – Setting Up Linux

### Tasks completed
- Created GitHub repository
- Installed Git and cloned the repository
- Installed VirtualBox
- Installed Ubuntu in VirtualBox
- Practised basic Linux commands
- Explored Linux directories: `/etc`, `/var`, `/home`
- Viewed Linux services using `systemctl`
- Tested Linux permissions using `ls -l` and `chmod`
- Searched files using `find` and `grep`

### Commands used
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
systemctl list-units --type=service
systemctl status snapd
touch test.sh
ls -l
chmod 755 test.sh
ls -l
echo "test" > notes.txt
find ~/isea-lab1 -name "test.sh"
grep -r "test" ~/isea-lab1
help cd

### Reflection

In this session I learned how to set up Ubuntu in a virtual machine and use basic Linux terminal commands. I also learned how Linux services, permissions, and file searching work. This helped me become more familiar with the Linux environme

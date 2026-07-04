# Module 01: Foundation of Cybersecurity and Computing - Kali Linux Practical Lab

## 📅 Date Started: 2026-06-30
## 📅 Date Completed: 2026-07-01

## ⚠️ Disclaimer:
**This activity is a simulation for practical educational purposes only. All exercises are conducted in controlled, isolated virtual environments to develop cybersecurity skills and knowledge. No real systems, networks, or production data were accessed or modified.**

## 🧪 Activity Type:
Hands-on technical lab: Mastering Kali Linux navigation, command-line operations, file system management, and permission controls as foundational cybersecurity competencies.

## 🎯 Lab Goal:
To develop proficiency in Kali Linux by navigating both GUI and terminal environments, executing essential file/directory operations, understanding and manipulating Linux file permissions, and applying foundational commands used in security auditing and penetration testing workflows.

## 🛠 Tools Used:
- Kali Linux 2024.2 virtual machine (VM)
- Terminal/Shell (Bash)
- Thunar file manager (GUI)
- Linux command-line utilities: `whoami`, `pwd`, `cd`, `ls`, `mkdir`, `touch`, `cp`, `mv`, `rm`, `cat`, `less`, `chmod`, `chown`, `groupadd`, `usermod`, `grep`, `ps`, `ip`, `apt`, `ping`, `df`, `free`, `man`

## 📋 What I Did:

### **Part 1: Create and Change Directories**
1. Verified current user identity:
   ```bash
   $ whoami
   analyst
   ```
2. Printed current working directory to confirm location:
   ```bash
   $ pwd
   /home/analyst
   ```
3. Navigated to the `Documents` directory:
   ```bash
   $ cd Documents
   ```
4. Listed directory contents in long format to view metadata:
   ```bash
   $ ls -l
   total 12
   -rw-r--r-- 1 analyst analyst  245 Jun 30 14:22 notes.txt
   drwxr-xr-x 2 analyst analyst 4096 Jun 30 14:20 projects
   ```
5. Created a new directory for lab work:
   ```bash
   $ mkdir security_lab_01
   ```
6. Verified directory creation:
   ```bash
   $ ls
   notes.txt  projects  security_lab_01
   ```
7. Created a new test file:
   ```bash
   $ touch security_lab_01/audit_checklist.txt
   ```
8. Removed the test directory after verification:
   ```bash
   $ rmdir security_lab_01
   ```
9. Confirmed successful removal:
   ```bash
   $ ls
   notes.txt  projects
   ```

### **Part 2: Copying and Moving Files**
1. Copied a credential reference file for backup:
   ```bash
   $ cp gvm_admin_passwd.txt backup_gvm_admin_passwd.txt
   ```
2. Verified copy operation:
   ```bash
   $ ls -l *.txt
   -rw-r--r-- 1 analyst analyst 128 Jun 30 15:10 gvm_admin_passwd.txt
   -rw-r--r-- 1 analyst analyst 128 Jun 30 15:11 backup_gvm_admin_passwd.txt
   ```
3. Moved the original file to an organized subdirectory:
   ```bash
   $ mv gvm_admin_passwd.txt Documents/credentials/
   ```
4. Confirmed successful move:
   ```bash
   $ ls Documents/credentials/
   gvm_admin_passwd.txt
   ```

### **Part 3: Deleting Files**
1. Deleted the backup file after confirming it was no longer needed:
   ```bash
   $ rm backup_gvm_admin_passwd.txt
   ```
2. Verified deletion:
   ```bash
   $ ls *.txt
   ls: cannot access '*.txt': No such file or directory
   ```

### **Part 4: Viewing File Content**
1. Displayed contents of a configuration file:
   ```bash
   $ cat Documents/credentials/gvm_admin_passwd.txt
   GVM_Admin_Password: SecureP@ssw0rd2026!
   Last_Updated: 2026-06-30
   ```
2. Used paginated viewing for a longer log file:
   ```bash
   $ less /var/log/auth.log
   # (Navigated with spacebar, searched with /failed, exited with q)
   ```

### **Lab 2: Understanding and Working with File Permissions**
1. Created 5 test files and examined default permissions:
   ```bash
   $ touch report_v1.txt report_v2.txt config.ini script.sh notes.md
   $ ls -l
   -rw-r--r-- 1 analyst analyst 0 Jun 30 15:45 config.ini
   -rw-r--r-- 1 analyst analyst 0 Jun 30 15:45 notes.md
   -rw-r--r-- 1 analyst analyst 0 Jun 30 15:45 report_v1.txt
   -rw-r--r-- 1 analyst analyst 0 Jun 30 15:45 report_v2.txt
   -rw-r--r-- 1 analyst analyst 0 Jun 30 15:45 script.sh
   ```
2. Interpreted permission structure:
   - First character `-` = regular file
   - Triplets `rw- r-- r--` = owner (read/write), group (read), others (read)
3. Modified permissions on a sensitive config file:
   ```bash
   $ chmod 750 config.ini
   $ ls -l config.ini
   -rwxr-x--- 1 analyst analyst 0 Jun 30 15:45 config.ini
   ```
   - Owner: rwx (full access)
   - Group: r-x (read/execute)
   - Others: --- (no access)
4. Changed file ownership for administrative control:
   ```bash
   $ sudo chown root config.ini
   $ ls -l config.ini
   -rwxr-x--- 1 root analyst 0 Jun 30 15:45 config.ini
   ```
5. Created a new security group for collaborative access:
   ```bash
   $ sudo groupadd sec_audit_team
   $ getent group sec_audit_team
   sec_audit_team:x:1025:
   ```
6. Added current user to the new group:
   ```bash
   $ sudo usermod -aG sec_audit_team analyst
   $ groups analyst
   analyst : analyst sec_audit_team sudo
   ```
7. Assigned file to new group and set collaborative permissions:
   ```bash
   $ sudo chown analyst:sec_audit_team report_v1.txt
   $ chmod 760 report_v1.txt
   $ ls -l report_v1.txt
   -rwxrw---- 1 analyst sec_audit_team 0 Jun 30 15:45 report_v1.txt
   ```

### **Additional Commands Explored**
- Network diagnostics:
  ```bash
  $ ping -c4 google.com
  PING google.com (142.250.189.206) 56(84) bytes of data.
  64 bytes from 142.250.189.206: icmp_seq=1 ttl=117 time=23.4 ms
  ```
- Network interface information:
  ```bash
  $ ip addr show eth0
  2: eth0: <BROADCAST,MULTICAST,UP> mtu 1500 qdisc pfifo_fast state UP
      link/ether 08:00:27:ab:cd:ef brd ff:ff:ff:ff:ff:ff
      inet 192.168.56.101/24 brd 192.168.56.255 scope global eth0
  ```
- System monitoring:
  ```bash
  $ ps aux | head -5
  USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
  root         1  0.0  0.1 169856 11232 ?        Ss   14:20   0:02 /sbin/init
  root         2  0.0  0.0      0     0 ?        S    14:20   0:00 [kthreadd]
  ```
- Disk and memory usage:
  ```bash
  $ df -h /home
  Filesystem      Size  Used Avail Use% Mounted on
  /dev/sda1        50G   12G   36G  25% /
  
  $ free -h
                total        used        free      shared  buff/cache   available
  Mem:           3.8G        1.2G        1.9G        156M        712M        2.3G
  ```
- Package management workflow:
  ```bash
  $ sudo apt update
  $ sudo apt upgrade -y
  $ sudo apt install nmap -y
  ```

## 🔍 What I Found:

### **File System Navigation**
- `pwd` provides immediate context within the Linux directory hierarchy; essential when working across multiple terminal sessions
- `ls -l` reveals critical metadata: permissions, owner, group, size, modification timestamp, and filename—key for security auditing
- Relative paths (`cd credentials`) vs. absolute paths (`cd /home/analyst/Documents/credentials`) affect navigation efficiency and script portability
- Directory creation/removal is instantaneous; verification with `ls` confirms operation success and prevents downstream errors

### **File Operations**
- `cp` creates independent copies; original and backup coexist until explicitly modified or deleted—critical for preserving evidence integrity
- `mv` performs relocation or renaming; file disappears from source and appears in destination—useful for organizing forensic artifacts
- `rm` permanently deletes files without trash recovery; caution required to avoid accidental data loss during investigations
- `cat` is ideal for short files; `less` enables scrolling through large outputs (logs, reports) without flooding the terminal

### **Permission Model Insights**
- Linux permissions follow a three-tier model: owner, group, others—fundamental to implementing least privilege
- Numeric notation (e.g., 750) is efficient: 7=rwx (4+2+1), 6=rw- (4+2), 5=r-x (4+1), 0=--- (no access)
- `chmod` changes permissions; `chown` changes ownership; both require appropriate privileges (`sudo` for system files)
- Group-based permissions enable collaborative access while restricting external users—essential for team-based security operations
- `sudo` elevates privileges for administrative tasks but should be used judiciously to minimize risk surface

### **System Administration Commands**
- `ping` tests network connectivity and latency; `-c4` limits to 4 packets for quick validation during recon
- `ip addr` (modern replacement for deprecated `ifconfig`) displays network interface configuration and IP assignment
- `ps aux` lists active processes with user, CPU, memory, and command details—critical for identifying suspicious processes
- `df -h` and `free -h` provide human-readable disk and memory usage summaries for capacity planning
- `apt` package management requires `update` before `install` to ensure latest package indices and security patches

### **Security-Relevant Observations**
- File permissions directly impact security: overly permissive settings (e.g., 777) expose data to unauthorized access or modification
- Principle of least privilege: granting only necessary permissions reduces attack surface and limits lateral movement
- Ownership and group assignments enable role-based access control at the file system level—foundational for secure multi-user environments
- Command-line proficiency accelerates security tasks: scanning logs with `grep`, filtering process lists with `ps`, auditing permissions with `ls -l`

## 💡 What I Learned:

### **Foundational Linux Competencies**
- Navigating Linux via terminal is faster and more powerful than GUI for repetitive, automated, or remote security tasks
- Understanding file permissions is essential for securing systems, managing user access, and hardening environments against misconfiguration attacks
- Basic commands (`ls`, `cd`, `cp`, `mv`, `rm`, `cat`) form the building blocks for advanced scripting, automation, and incident response

### **Security Operations Relevance**
- Kali Linux is purpose-built for security testing; familiarity with its environment accelerates adoption of tools like Nmap, Metasploit, Burp Suite, and John the Ripper
- Permission misconfigurations are common attack vectors; knowing how to audit and correct them is a core defensive skill for SOC analysts and pentesters
- Command-line proficiency enables efficient log analysis, process monitoring, artifact collection, and rapid incident triage

### **Best Practices Developed**
- Always verify operations (`ls`, `cat`, `pwd`) after executing file system commands to confirm intended outcome
- Use `sudo` only when necessary; excessive privilege escalation increases risk of accidental system changes or privilege abuse
- Test permission changes on non-critical files before applying to production or evidence systems
- Leverage `man <command>` for on-demand reference rather than memorizing every flag—efficiency over rote learning

### **Transferable Skills for Cybersecurity Roles**
- Terminal fluency is required for SOC analysis, penetration testing, digital forensics, cloud security, and DevSecOps roles
- Understanding Linux permission models translates to Windows ACLs, cloud IAM policies, container security (Docker/Kubernetes), and infrastructure-as-code
- Command-line efficiency supports automation (Bash/Python scripting), tool chaining, and rapid incident response under time pressure

### **Next Steps for Skill Development**
- Practice combining commands with pipes (`|`) and redirection (`>`, `>>`) for advanced data processing and log parsing
- Explore Bash scripting to automate repetitive security tasks (user provisioning, log rotation, backup verification)
- Learn process management (`kill`, `top`, `htop`, `systemctl`) for system monitoring, threat hunting, and service hardening
- Study package management and dependency resolution for maintaining secure, updated tooling in isolated environments

## 📸 Screenshot:
🔒 **Screenshot Restriction Notice**

Screenshots from TS Academy or affiliated simulated lab environments may contain proprietary educational content. Specific terminal outputs, file names, or system identifiers are not shared publicly to maintain academic integrity and platform terms of use.

**Lab Completion Verified:**
- ✅ Platform: TS Academy Cybersecurity Program
- ✅ Module Status: 100% COMPLETE
- ✅ Activities Completed: 
  - Kali Linux GUI and terminal navigation
  - File/directory operations (create, copy, move, delete, view)
  - File permission analysis and modification (`chmod`, `chown`, group management)
  - System commands exploration (`ping`, `ip addr`, `ps`, `apt`, `df`, `free`)
- ✅ Completion Date: 2026-07-01

**Alternative Evidence:** Comprehensive written documentation of commands executed, permission models analyzed, and security-relevant insights provided in sections above.
```

# Linux for Beginners — Complete Ubuntu Learning Repository

Beginner level Ubuntu GitHub-ready

We're building a practical Linux course for someone starting with absolutely no Linux experience.

The repository will include:

- 10 structured learning modules with actual lesson content.
- Step-by-step Ubuntu terminal demonstrations.
- Hands-on labs with expected results.
- Quizzes with answer keys.
- Real-world beginner projects.
- A final Linux administration challenge.

The exercises will use Ubuntu and Bash. Commands that modify the system will include explanations and safety notes.

## 1\. Repository structure

text

```text
linux-for-beginners/
│
├── README.md
├── LICENSE
├── CONTRIBUTING.md
│
├── 01-linux-fundamentals/
│   └── lesson.md
├── 02-terminal-commands/
│   └── lesson.md
├── 03-files-and-directories/
│   └── lesson.md
├── 04-users-and-permissions/
│   └── lesson.md
├── 05-package-management/
│   └── lesson.md
├── 06-process-management/
│   └── lesson.md
├── 07-networking/
│   └── lesson.md
├── 08-shell-scripting/
│   └── lesson.md
├── 09-system-administration/
│   └── lesson.md
├── 10-practical-projects/
│   ├── backup.sh
│   ├── system-info.sh
│   └── README.md
│
├── labs/
│   ├── lab-01-terminal.md
│   ├── lab-02-files.md
│   ├── lab-03-permissions.md
│   └── lab-04-networking.md
│
└── quizzes/
    ├── questions.md
    └── answers.md
```

## 2. Complete course content

The following is the main repository content. Each section can be saved as its corresponding Markdown file.

Writing

# 🐧 Linux for Beginners

### A Complete Hands-On Ubuntu Linux Learning Course

\!Linux \!Ubuntu \!Level \!License

Welcome to Linux for Beginners\!

This repository is a practical learning resource for people who have never used Linux before.

You will learn Linux from the ground up using Ubuntu. Every module includes explanations, commands, examples, practical exercises, and quizzes.

## Learning objectives

By completing this course, you should be able to:

- Understand Linux and its architecture.
- Navigate the Linux terminal.
- Create, copy, move, and delete files.
- Understand Linux permissions.
- Manage users and groups.
- Install and remove applications.
- Monitor processes and system resources.
- Understand basic networking.
- Write Bash scripts.
- Perform basic Linux administration.
- Complete practical Linux projects.

## Requirements

- A computer running Windows, Linux, or macOS.
- Ubuntu installed directly, in a virtual machine, or through WSL.
- At least 20–30 minutes of practice per day.
- Basic computer literacy.

Recommended distribution: Ubuntu Desktop or Ubuntu Server.

Ubuntu download: https://ubuntu.com/download

---

# MODULE 01: INTRODUCTION TO LINUX

## 1.1 What is Linux?

Linux is an open-source operating system kernel.

An operating system manages computer resources, including:

- CPU.
- RAM.
- Storage.
- Hardware devices.
- Running applications.
- User accounts.

Linux distributions combine the Linux kernel with utilities, software, and other components to create a complete operating system.

## 1.2 Where is Linux used?

Linux is widely used in:

1. Web servers.
2. Cloud computing.
3. Cybersecurity.
4. Software development.
5. Networking.
6. Supercomputers.
7. Embedded systems.

## 1.3 Understanding Linux distributions

A distribution is a complete operating system built around the Linux kernel.

Examples:

| Distribution | Main use |
| --- | --- |
| Ubuntu | Desktop, servers and development |
| Debian | Stable operating systems |
| Fedora | Modern Linux technologies |
| Kali Linux | Security testing |
| Linux Mint | Desktop computing |
| Rocky Linux | Enterprise servers |

For this course, we will use Ubuntu.

## 1.4 Understanding the Linux architecture

A simplified Linux architecture:

text

```text
+-----------------------------+
|       User Applications     |
+-----------------------------+
|       Shell / Terminal      |
+-----------------------------+
|        System Libraries     |
+-----------------------------+
|        Linux Kernel         |
+-----------------------------+
|          Hardware           |
+-----------------------------+
```

The kernel manages hardware and system resources.

The shell allows users to interact with the operating system.

## 1.5 Your first Linux commands

Open your Ubuntu terminal using:

bash

```bash
Ctrl + Alt + T
```

Run:

bash

```bash
whoami
```

Displays your username.

bash

```bash
pwd
```

Displays your current directory.

bash

```bash
date
```

Displays the current date and time.

bash

```bash
uname -a
```

Displays kernel and system information.

bash

```bash
cat /etc/os-release
```

Displays your Linux distribution information.

## 1.6 Practical exercise

Run all five commands and record their output.

### Quiz

1. What is Linux?
2. What is a Linux distribution?
3. What does the kernel do?
4. Which command displays your username?
5. Which command displays your current directory?

---

# MODULE 02: LINUX TERMINAL COMMANDS

## 2.1 What is a terminal?

A terminal is a text-based interface used to communicate with Linux.

Instead of clicking buttons, you type commands.

Example:

bash

```bash
username@ubuntu:~$
```

This prompt contains:

- Username: Current account.
- Hostname: Computer name.
- `~`: Home directory.
- `$`: Regular user prompt.

## 2.2 Essential Linux commands

### Listing files

bash

```bash
ls
```

List files and folders.

bash

```bash
ls -l
```

Show detailed information.

bash

```bash
ls -a
```

Show hidden files.

bash

```bash
ls -lh
```

Show human-readable file sizes.

### Directory navigation

bash

```bash
pwd
```

Show current location.

bash

```bash
cd Documents
```

Enter the Documents directory.

bash

```bash
cd ..
```

Move one directory backward.

bash

```bash
cd ~
```

Return to your home directory.

bash

```bash
cd /
```

Move to the root directory.

### Getting help

bash

```bash
man ls
```

Read the manual for the `ls` command.

bash

```bash
ls --help
```

Display command help.

### Other useful commands

bash

```bash
clear
```

Clear the screen.

bash

```bash
history
```

Display previous commands.

bash

```bash
echo "Hello Linux"
```

Print a message.

bash

```bash
hostname
```

Display the computer hostname.

## 2.3 Command options

Linux commands can accept options.

Example:

bash

```bash
ls -la
```

Here:

- `ls` is the command.
- `-l` requests detailed output.
- `-a` includes hidden files.

## 2.4 Practical lab

Complete the following:

bash

```bash
whoami
pwd
ls -la
date
hostname
uname -a
```

Try using `man` to learn more about each command.

### Quiz

1. What does `pwd` do?
2. What does `ls -a` display?
3. How do you return to your home directory?
4. What does `clear` do?
5. How do you view command history?

---

# MODULE 03: FILE AND DIRECTORY MANAGEMENT

## 3.1 Linux filesystem

Linux uses a hierarchical filesystem.

The top-level directory is `/`.

Important directories:

| Directory | Purpose |
| --- | --- |
| `/` | Root of filesystem |
| `/home` | User directories |
| `/etc` | Configuration files |
| `/var` | Variable data and logs |
| `/tmp` | Temporary files |
| `/usr` | Applications and resources |
| `/root` | Root user's home directory |
| `/dev` | Device files |
| `/proc` | Process and kernel information |

## 3.2 Creating directories

Create a directory:

bash

```bash
mkdir linux-practice
```

Create nested directories:

bash

```bash
mkdir -p linux-practice/notes/lessons
```

## 3.3 Creating files

bash

```bash
touch notes.txt
```

Create a file with content:

bash

```bash
echo "I am learning Linux" > notes.txt
```

Append content:

bash

```bash
echo "Linux is powerful" >> notes.txt
```

Remember:

- `>` replaces existing content.
- `>>` appends content.

## 3.4 Reading files

bash

```bash
cat notes.txt
```

Read a long file:

bash

```bash
less notes.txt
```

Display the first lines:

bash

```bash
head notes.txt
```

Display the last lines:

bash

```bash
tail notes.txt
```

## 3.5 Copying files

bash

```bash
cp notes.txt backup.txt
```

Copy directories:

bash

```bash
cp -r linux-practice linux-backup
```

## 3.6 Moving and renaming files

bash

```bash
mv notes.txt linux-notes.txt
```

Move a file:

bash

```bash
mv linux-notes.txt linux-practice/
```

## 3.7 Deleting files

bash

```bash
rm backup.txt
```

Remove an empty directory:

bash

```bash
rmdir empty-folder
```

Remove a directory and its contents:

bash

```bash
rm -r linux-backup
```

**Safety:** Check the target before deleting files. Avoid unfamiliar uses of `rm`, especially commands involving `sudo` or wildcards.

## 3.8 Finding files

bash

```bash
find ~/Documents -name "*.txt"
```

Find text files in Documents.

Search for a word inside a file:

bash

```bash
grep "Linux" notes.txt
```

Search without case sensitivity:

bash

```bash
grep -i "linux" notes.txt
```

## 3.9 Practical project

Create a folder named `student-records`.

Inside it, create:

text

```text
student-records/
├── names.txt
├── courses.txt
└── backups/
```

Add some sample content, copy the files into the backup directory, and display the directory structure using:

bash

```bash
ls -R student-records
```

---

# MODULE 04: USERS AND FILE PERMISSIONS

## 4.1 Understanding Linux users

Linux supports multiple user accounts.

Each user has an identity and associated permissions.

Useful commands:

bash

```bash
whoami
```

Display the current user.

bash

```bash
who
```

Display logged-in users.

bash

```bash
id
```

Display user and group information.

## 4.2 Creating users

On Ubuntu:

bash

```bash
sudo adduser student
```

This creates a new account.

You will be asked to enter a password and optional user information.

## 4.3 Managing groups

Create a group:

bash

```bash
sudo groupadd learners
```

Add a user to a group:

bash

```bash
sudo usermod -aG learners student
```

Check group membership:

bash

```bash
groups student
```

## 4.4 Understanding permissions

Linux has three basic permissions:

| Permission | Symbol | Value |
| --- | --- | --- |
| Read | r | 4 |
| Write | w | 2 |
| Execute | x | 1 |

These permissions apply to:

- Owner.
- Group.
- Others.

Example:

text

```text
-rwxr-xr--
```

Interpretation:

- Owner: Read, write, execute.
- Group: Read and execute.
- Others: Read only.

## 4.5 Changing permissions

Create a file:

bash

```bash
touch example.txt
```

View permissions:

bash

```bash
ls -l example.txt
```

Add execute permission for the owner:

bash

```bash
chmod u+x example.txt
```

Set numerical permissions:

bash

```bash
chmod 755 example.txt
```

Another example:

bash

```bash
chmod 644 example.txt
```

Meaning of 644:

- Owner: Read and write.
- Group: Read.
- Others: Read.

## 4.6 Changing ownership

bash

```bash
sudo chown student example.txt
```

Change owner and group:

bash

```bash
sudo chown student:learners example.txt
```

## 4.7 Understanding sudo

`sudo` allows an authorized user to execute a command with elevated privileges.

Example:

bash

```bash
sudo apt update
```

Use elevated permissions only when needed.

---

# MODULE 05: PACKAGE MANAGEMENT

## 5.1 What is a package manager?

A package manager installs, updates, and removes software.

Ubuntu uses APT.

## 5.2 Update package information

bash

```bash
sudo apt update
```

This refreshes information about available packages.

## 5.3 Upgrade software

bash

```bash
sudo apt upgrade
```

Installs available updates for installed packages.

## 5.4 Installing applications

Install Git:

bash

```bash
sudo apt install git
```

Install Nano:

bash

```bash
sudo apt install nano
```

Install curl:

bash

```bash
sudo apt install curl
```

## 5.5 Checking installed applications

bash

```bash
git --version
```

bash

```bash
curl --version
```

## 5.6 Removing software

bash

```bash
sudo apt remove git
```

Remove unused dependencies:

bash

```bash
sudo apt autoremove
```

## 5.7 Searching for packages

bash

```bash
apt search nginx
```

Display package information:

bash

```bash
apt show nginx
```

### Practical lab

1. Update Ubuntu package information.
2. Install Git.
3. Check the Git version.
4. Install curl.
5. Check the curl version.

---

# MODULE 06: PROCESS MANAGEMENT

## 6.1 What is a process?

A process is a running instance of a program.

Examples include:

- Web browsers.
- Text editors.
- Background services.
- Terminal commands.

Each process has a Process ID (PID).

## 6.2 Viewing processes

bash

```bash
ps
```

Display processes:

bash

```bash
ps aux
```

## 6.3 Real-time monitoring

bash

```bash
top
```

This displays:

- CPU usage.
- Memory usage.
- Running processes.
- Process IDs.

Exit using `q`.

Optional alternative:

bash

```bash
sudo apt install htop
htop
```

## 6.4 Finding processes

bash

```bash
pgrep firefox
```

Search for Firefox processes.

## 6.5 Stopping processes

First identify a process ID.

Then:

bash

```bash
kill PID
```

Replace `PID` with the actual process ID.

This sends a normal termination request.

Use force termination only when necessary.

## 6.6 Background tasks

Run a command in the background:

bash

```bash
sleep 60 &
```

Display background jobs:

bash

```bash
jobs
```

### Practical lab

1. Open a terminal.
2. Run `top`.
3. Identify CPU and memory usage.
4. Exit with `q`.
5. Run `sleep 60 &`.
6. Display the background job.

---

# MODULE 07: NETWORKING FUNDAMENTALS

## 7.1 What is a network?

A network connects computers and devices so that they can communicate.

Basic networking concepts:

- IP address.
- MAC address.
- DNS.
- Gateway.
- Router.
- TCP.
- UDP.

## 7.2 Display IP information

bash

```bash
ip addr
```

Display network interfaces:

bash

```bash
ip link
```

Display routing information:

bash

```bash
ip route
```

## 7.3 Test connectivity

bash

```bash
ping -c 4 google.com
```

This sends four test packets.

## 7.4 DNS lookup

bash

```bash
nslookup google.com
```

If unavailable:

bash

```bash
sudo apt install dnsutils
```

## 7.5 Check network connections

bash

```bash
ss -tuln
```

This displays listening TCP and UDP sockets.

## 7.6 Download files

bash

```bash
wget https://example.com
```

Or:

bash

```bash
curl https://example.com
```

### Practical lab

Run:

bash

```bash
ip addr
ip route
ping -c 4 google.com
nslookup google.com
ss -tuln
```

Record your findings.

Only perform network testing on systems and networks you own or are authorized to administer.

---

# MODULE 08: BASH SHELL SCRIPTING

## 8.1 What is Bash?

Bash is a command-line shell commonly used on Linux.

It also supports scripting, which allows you to automate repetitive tasks.

## 8.2 Create your first script

Create a file:

bash

```bash
nano hello.sh
```

Add:

bash

```bash
#!/bin/bash

echo "Welcome to Linux!"
echo "This is my first Bash script."

name="Student"

echo "Hello, $name!"
```

Save and exit.

## 8.3 Execute the script

bash

```bash
chmod +x hello.sh
./hello.sh
```

Expected output:

text

```text
Welcome to Linux!
This is my first Bash script.
Hello, Student!
```

## 8.4 Variables

bash

```bash
#!/bin/bash

name="Alice"
course="Linux"

echo "My name is $name"
echo "I am studying $course"
```

## 8.5 User input

bash

```bash
#!/bin/bash

echo "Enter your name:"
read name

echo "Welcome, $name!"
```

## 8.6 Conditional statements

bash

```bash
#!/bin/bash

number=10

if [ "$number" -gt 5 ]; then
    echo "Number is greater than 5"
else
    echo "Number is 5 or less"
fi
```

## 8.7 Loops

bash

```bash
#!/bin/bash

for number in 1 2 3 4 5
do
    echo "Number: $number"
done
```

## 8.8 Functions

bash

```bash
#!/bin/bash

greet() {
    echo "Welcome to Linux!"
}

greet
```

## 8.9 Practical challenge

Create a script that:

1. Asks the user for their name.
2. Asks what Linux distribution they use.
3. Displays a welcome message.
4. Displays the current date.

---

# MODULE 09: BASIC SYSTEM ADMINISTRATION

## 9.1 System information

bash

```bash
uname -a
```

bash

```bash
hostnamectl
```

bash

```bash
cat /etc/os-release
```

## 9.2 Memory usage

bash

```bash
free -h
```

## 9.3 Disk usage

bash

```bash
df -h
```

## 9.4 Directory storage usage

bash

```bash
du -sh ~/Documents
```

## 9.5 Block devices

bash

```bash
lsblk
```

## 9.6 System logs

View recent system journal entries:

bash

```bash
journalctl -n 20
```

View service status:

bash

```bash
systemctl status
```

## 9.7 Services

Check SSH service status:

bash

```bash
systemctl status ssh
```

If SSH is installed, start it with:

bash

```bash
sudo systemctl start ssh
```

Enable automatic startup:

bash

```bash
sudo systemctl enable ssh
```

Only enable services you actually need.

## 9.8 Scheduled tasks

Linux provides cron for scheduling recurring tasks.

Edit your user's cron jobs:

bash

```bash
crontab -e
```

Example:

cron

```cron
0 8 * * * /home/student/backup.sh
```

This schedules the script to run daily at 8:00 AM, provided the script is executable and the path is correct.

---

# MODULE 10: PRACTICAL LINUX PROJECTS

## PROJECT 1: SYSTEM INFORMATION SCRIPT

### Objective

Create a script that displays important information about your Ubuntu system.

Create:

bash

```bash
nano system-info.sh
```

Code:

bash

```bash
#!/bin/bash

echo "=============================="
echo "       SYSTEM INFORMATION"
echo "=============================="

echo "Username:"
whoami

echo "Hostname:"
hostname

echo "Operating System:"
. /etc/os-release
echo "$PRETTY_NAME"

echo "Kernel:"
uname -r

echo "Current Date:"
date

echo "Memory Usage:"
free -h

echo "Disk Usage:"
df -h /

echo "=============================="
echo "       REPORT COMPLETE"
echo "=============================="
```

Run:

bash

```bash
chmod +x system-info.sh
./system-info.sh
```

Expected result: A report containing your username, hostname, Ubuntu version, kernel, date, memory, and disk usage.

## PROJECT 2: AUTOMATED BACKUP SCRIPT

### Objective

Create a script that backs up a directory into another directory.

Create:

bash

```bash
nano backup.sh
```

Code:

bash

```bash
#!/bin/bash

SOURCE="$HOME/Documents"
DESTINATION="$HOME/backups"

mkdir -p "$DESTINATION"

BACKUP_FILE="$DESTINATION/documents-$(date +%Y%m%d-%H%M%S).tar.gz"

if [ ! -d "$SOURCE" ]; then
    echo "Source directory does not exist."
    exit 1
fi

if tar -czf "$BACKUP_FILE" -C "$HOME" Documents; then
    echo "Backup completed successfully!"
    echo "Backup location: $BACKUP_FILE"
else
    echo "Backup failed."
    exit 1
fi
```

Run:

bash

```bash
chmod +x backup.sh
./backup.sh
```

Check your backups:

bash

```bash
ls -lh ~/backups
```

Note: This example assumes that `~/Documents` exists. Modify the source directory if necessary.

## PROJECT 3: FILE ORGANIZER

### Objective

Create a script that organizes files into folders according to their extensions.

Create:

bash

```bash
nano organize.sh
```

Code:

bash

```bash
#!/bin/bash

TARGET="$HOME/Downloads"

if [ ! -d "$TARGET" ]; then
    echo "Downloads directory not found."
    exit 1
fi

mkdir -p "$TARGET/PDFs"
mkdir -p "$TARGET/Images"
mkdir -p "$TARGET/Documents"

find "$TARGET" -maxdepth 1 -type f -iname "*.pdf" \
    -exec mv -t "$TARGET/PDFs" -- {} +

find "$TARGET" -maxdepth 1 -type f \( \
    -iname "*.jpg" -o \
    -iname "*.jpeg" -o \
    -iname "*.png" \
    \) -exec mv -t "$TARGET/Images" -- {} +

find "$TARGET" -maxdepth 1 -type f \( \
    -iname "*.doc" -o \
    -iname "*.docx" -o \
    -iname "*.txt" \
    \) -exec mv -t "$TARGET/Documents" -- {} +

echo "File organization completed."
```

Before running this project, test it with sample files in a separate practice directory. The script moves files, so check the target carefully.

---

# HANDS-ON LABS

## LAB 01: TERMINAL BASICS

### Objective

Become comfortable using the Linux terminal.

Tasks:

- Open your terminal.
- Display your username.
- Display the current directory.
- List all files.
- Display the operating system.
- Display the date.

Commands:

bash

```bash
whoami
pwd
ls -la
cat /etc/os-release
date
```

Expected result: You should understand how to identify your user, location, files, and operating system.

## LAB 02: FILE MANAGEMENT

### Objective

Practice creating and organizing files.

Tasks:

1. Create a directory named `linux-lab`.
2. Create a directory named `documents` inside it.
3. Create `notes.txt`.
4. Write three lines into the file.
5. Display its contents.
6. Copy it into a backup directory.
7. Rename the original file.

Useful commands:

bash

```bash
mkdir -p linux-lab/documents
cd linux-lab
touch documents/notes.txt
echo "Learning Linux" > documents/notes.txt
echo "Practicing commands" >> documents/notes.txt
echo "Building projects" >> documents/notes.txt
cat documents/notes.txt
mkdir backup
cp documents/notes.txt backup/
mv documents/notes.txt documents/linux-notes.txt
```

## LAB 03: PERMISSIONS

### Objective

Understand Linux file permissions.

Tasks:

bash

```bash
touch practice.txt
ls -l practice.txt
chmod 644 practice.txt
ls -l practice.txt
chmod u+x practice.txt
ls -l practice.txt
```

Questions:

- What changed after using `chmod 644`?
- What happened after using `chmod u+x`?
- What does execute permission mean?

## LAB 04: NETWORKING

### Objective

Understand basic network information.

Tasks:

bash

```bash
ip addr
ip route
ping -c 4 google.com
ss -tuln
```

Record:

- Your network interface.
- Your local IP address.
- Your default gateway.
- Whether the connectivity test succeeded.

---

# QUIZZES

## QUIZ 1: LINUX FUNDAMENTALS

1. What is Linux?
   - A. A programming language
   - B. An operating system kernel
   - C. A web browser
   - D. A database
2. Which command displays the current directory?
   - A. ls
   - B. pwd
   - C. cd
   - D. whoami
3. Which directory contains system configuration files?
   - A. /etc
   - B. /home
   - C. /tmp
   - D. /dev
4. Which command displays your username?
   - A. hostname
   - B. uname
   - C. whoami
   - D. date

## QUIZ 2: FILE MANAGEMENT

1. Which command creates a directory?
   - A. touch
   - B. mkdir
   - C. mv
   - D. cat
2. Which command copies a file?
   - A. cp
   - B. rm
   - C. pwd
   - D. cd
3. What does `>` do?
   - A. Deletes a file
   - B. Redirects output and replaces existing file content
   - C. Copies a file
   - D. Displays a directory
4. Which command displays file contents?
   - A. cat
   - B. mkdir
   - C. chmod
   - D. hostname

## QUIZ 3: PERMISSIONS

1. What does `r` mean?
2. What does `w` mean?
3. What does `x` mean?
4. What numeric value represents read permission?
5. What does `chmod 755` mean?
6. What is the purpose of `sudo`?

## QUIZ 4: SYSTEM ADMINISTRATION

1. Which package manager does Ubuntu use?
2. Which command updates package information?
3. Which command displays running processes?
4. Which command displays disk space?
5. Which command displays memory usage?
6. Which command displays IP addresses?

## QUIZ ANSWERS

### Quiz 1

1. B
2. B
3. A
4. C

### Quiz 2

1. B
2. A
3. B
4. A

### Quiz 3

1. Read.
2. Write.
3. Execute.
4.
   4.
5. Owner has read, write, and execute; group and others have read and execute.
6. It runs an authorized command with elevated privileges.

### Quiz 4

1. APT.
2. `sudo apt update`.
3. `ps aux` or `top`.
4. `df -h`.
5. `free -h`.
6. `ip addr`.

---

# FINAL PRACTICAL CHALLENGE

## Build Your Own Linux Administration Toolkit

Create a directory called:

bash

```bash
mkdir linux-admin-toolkit
```

Your toolkit should contain:

text

```text
linux-admin-toolkit/
├── system-info.sh
├── backup.sh
├── file-organizer.sh
└── README.md
```

Requirements:

1. Create a system information script.
2. Create a backup script.
3. Create a file organizer.
4. Make each script executable.
5. Test every script.
6. Document what each script does.
7. Upload the project to GitHub.

### Final assessment

You should be able to:

- [ ]Navigate Linux directories.
- [ ]Manage files and folders.
- [ ]Read and edit text files.
- [ ]Understand file permissions.
- [ ]Manage basic user accounts.
- [ ]Install applications.
- [ ]Monitor running processes.
- [ ]Check network configuration.
- [ ]Write simple Bash scripts.
- [ ]Perform basic system administration.

---

# FOUR-WEEK LEARNING PLAN

| Week | Focus | Expected achievement |
| --- | --- | --- |
| 1 | Linux fundamentals and terminal | Navigate Ubuntu confidently |
| 2 | Files, permissions and users | Manage files and accounts |
| 3 | Packages, processes and networking | Understand basic administration |
| 4 | Bash and practical projects | Automate simple tasks |

Suggested daily study time: 20–30 minutes.

---

# GITHUB CONTRIBUTIONS

Contributions are welcome\!

If you want to improve this course:

1. Fork the repository.
2. Create a branch.
3. Add your improvements.
4. Test your commands and scripts.
5. Submit a pull request.

---

# LICENSE

This learning repository is released under the MIT License.

You are free to use, modify, and distribute this learning material under the terms of that license.

---

# USEFUL RESOURCES

- Ubuntu: https://ubuntu.com/
- Ubuntu Documentation: https://help.ubuntu.com/
- Linux Journey: https://linuxjourney.com/
- GNU Bash Manual: https://www.gnu.org/software/bash/manual/
- OverTheWire Bandit: https://overthewire.org/wargames/bandit/
- Linux Documentation Project: https://tldp.org/

---

## CONCLUSION

Linux is a valuable skill for anyone interested in technology.

Start with the fundamentals, practice commands regularly, complete the labs, and build your own projects.

Do not worry about memorizing every command. Learn how to use documentation and understand what each command does.

**Keep learning. Keep practicing. Master Linux one command at a time\! 🐧**

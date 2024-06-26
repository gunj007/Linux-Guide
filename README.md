# Linux-Guide
Explore essential Linux commands, installation guides for Miniconda/Anaconda and NGS tools, alongside tips for tmux, server upgrades, and basic automation techniques. Ideal for beginners and Linux enthusiasts looking to streamline their workflow and improve system administration skills.


1. Linux Basic Commands

Directory Navigation

cd: Change directory
pwd: Print working directory
ls: List directory contents
mkdir: Make directories
rmdir: Remove empty directories
rm -r: Remove directories and their contents recursively

File Navigation

cp: Copy files and directories
mv: Move (rename) files and directories
rm: Remove files
touch: Create empty files
cat: Concatenate and display file contents
less: View file contents interactively
head and tail: View the beginning or end of files

Finding Files

find: Search for files and directories
Syntax examples: finding files by name, type, size, etc.
locate: Quickly find files by name

Viewing and Processing File Contents

grep: Search for patterns in files
wc: Count lines, words, or characters in a file
sed: Stream editor for filtering and transforming text
awk: Pattern scanning and processing language
cut: Extract sections from each line of files

Directory and File Management

chmod: Change file mode (permissions)
chown: Change file owner and group
ln: Create hard and symbolic links
du: Estimate file space usage
df: Report file system disk space usage
tar: Archive files and directories
zip and unzip: Compress and extract ZIP archives
gzip, gunzip, bzip2, xz: Compress and decompress files

File and Text Manipulation

sort: Sort lines of text files
uniq: Report or omit repeated lines
tee: Read from standard input and write to standard output and files
diff: Compare files line by line
patch: Apply a diff file to an original

Cache Memory Management
Clearing PageCache

sync: Ensure all cached data is written to disk
echo 1 > /proc/sys/vm/drop_caches: Drop page cache from memory
Note: Requires appropriate permissions (sudo)
Clearing dentries and inodes
echo 2 > /proc/sys/vm/drop_caches: Drop dentries and inodes from memory
Clearing PageCache, dentries, and inodes
echo 3 > /proc/sys/vm/drop_caches: Drop page cache, dentries, and inodes from memory

Checking Which Command Was Killed in journalctl
Using journalctl

journalctl -b -1: Show logs from the previous boot (replace -1 with the appropriate boot number)
journalctl -u UNIT_NAME: Show logs for a specific systemd unit
journalctl -p ERR: Show only messages with a priority level of ERR or higher
journalctl _PID=PID_NUMBER: Show logs related to a specific process ID (PID)

2. Install Miniconda or Anaconda

Basic NGS Tools Installation
conda install: Installing packages with Conda
Examples: prefetch, kraken, bracken
Using Docker for tool management
Installing NetFlow for network flow analysis

Advanced Package Management

pip: Python package installer (for packages not available via Conda)
apt-get or yum: Package managers for system-wide software installation (e.g., system utilities)

3. Other Helpful Tools

System Monitoring and Management

top and htop: Interactive process viewer (shows system tasks)
free: Display amount of free and used memory in the system
iostat: Report CPU and I/O statistics
netstat and ss: Network statistics
tmux

Networking

ping: Check network connectivity to another host
ifconfig and ip: Configure network interfaces

Terminal multiplexer for managing multiple sessions
Basic commands: creating, detaching, attaching sessions

Server Upgrade

Updating and upgrading system packages
Managing system services and dependencies

4. Automation Basics

Shell Scripting

Loops (for, while)
Conditionals (if, else, elif)
Functions and variables in shell scripts
Using cron for scheduled tasks

Additional Tips

User Management: Commands like useradd, usermod, passwd for managing users and passwords.
Process Management: Commands like ps, kill, pgrep for managing processes.
System Information: Commands like uname, hostname, uptime for retrieving system information.
File System Navigation: Understanding /, ~, . and .., and the significance of absolute vs relative paths.

CLI automation techniques

Handling multiple files with scripts
SNP (Single Nucleotide Polymorphism) processing and analysis

# 🐧 Linux Command Cheat Sheet

Quick reference for common Linux terminal commands.

---

## 🔧 System Info

```bash
uname -a                   # Kernel version
hostname                   # Show hostname
uptime                     # Show system uptime
whoami                     # Current user
top                        # Live process viewer
htop                       # Enhanced process viewer (if installed)



⸻

📂 File & Directory

ls                         # List files
ls -lAh                    # Long list with hidden files, human-readable
cd /path/to/dir            # Change directory
pwd                        # Show current directory
mkdir newdir               # Create directory
rm file.txt                # Remove file
rm -r dir/                 # Remove directory and contents
cp source dest             # Copy files or directories
mv old new                 # Move/rename files or directories



⸻

📄 Viewing Files

cat file.txt               # Show file content
less file.txt              # View file with paging
head -n 10 file.txt        # First 10 lines
tail -n 10 file.txt        # Last 10 lines
tail -f file.txt           # Real-time output (e.g., logs)



⸻

🔎 Searching

find . -name "*.txt"       # Find files
grep "text" file.txt       # Search inside files
grep -r "text" .           # Recursive grep



⸻

⚙️ Permissions

chmod +x script.sh         # Make executable
chmod 755 file             # Set permissions
chown user:group file      # Change ownership



⸻

📦 Package Management

Debian/Ubuntu (apt):

sudo apt update            # Refresh package list
sudo apt upgrade           # Upgrade packages
sudo apt install <pkg>     # Install package
sudo apt remove <pkg>      # Remove package

RHEL/CentOS (yum/dnf):

sudo dnf install <pkg>
sudo yum remove <pkg>



⸻

🧰 Process Management

ps aux                     # List processes
kill <PID>                 # Kill by PID
killall <name>             # Kill by name
bg                         # Resume in background
fg                         # Resume in foreground
jobs                       # Show background jobs



⸻

🌐 Networking

ip a                       # Show IP addresses
ping <host>                # Check connectivity
curl <url>                 # Fetch URL
wget <url>                 # Download file
netstat -tulpn             # Listening ports (if available)
ss -tulpn                  # Modern netstat replacement



⸻

📦 Disk & Filesystem

df -h                      # Disk space (human-readable)
du -sh *                   # Folder sizes in current dir
mount | grep <device>      # Mounted drives
lsblk                      # Block devices



⸻

🕒 Date & Time

date                       # Show date and time
cal                        # Calendar
timedatectl                # Show time settings



⸻

🧪 Scripting & Shortcuts

nano script.sh             # Edit file
bash script.sh             # Run shell script
echo $VAR                  # Print env variable
export VAR=value           # Set env variable
alias ll='ls -lAh'         # Create alias



⸻

🔄 Compression

tar -czvf archive.tar.gz dir/   # Compress directory
tar -xzvf archive.tar.gz        # Extract archive
zip archive.zip file            # Zip file
unzip archive.zip               # Unzip file



⸻

🧼 Cleanup & Disk Tools

history                   # Show command history
clear                     # Clear terminal
sudo apt autoremove       # Remove unused packages
sudo journalctl --vacuum-time=7d   # Clean logs older than 7 days



⸻

✅ Pro Tips
	•	Use TAB for autocompletion
	•	Use CTRL + R to reverse search history
	•	Use !! to repeat the last command
	•	Use > file or >> file to redirect output

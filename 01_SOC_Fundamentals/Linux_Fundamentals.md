# Linux Command Fundamentals

## File & Directory Operations

pwd                         # Print current working directory
ls                          # List files and directories
ls -la                      # List all files including hidden, with detailed info
cd /path/to/dir             # Change directory
cd ~                        # Go to home directory
mkdir new_folder            # Create a new directory
touch new_file.txt          # Create a new empty file
rm file.txt                 # Delete a file
rm -r folder/               # Delete a folder and its contents recursively
cp file1.txt file2.txt      # Copy file1 to file2
mv file.txt /new/location/  # Move file to another location
find / -name "file.txt"            # Search for a file by name starting from root
grep "string" file.txt             # Search for string inside a file
grep -r "pattern" /path/to/dir     # Recursively search for pattern in directory
whoami                             # Display current user
id                                 # Show user ID and group info
sudo su                            # Become root user
chmod 755 script.sh                # Set file permissions
chown user:group file.txt          # Change file owner and group
sudo apt update                    # Refresh package lists
sudo apt upgrade                   # Upgrade all packages
sudo apt install package_name      # Install a new package
sudo apt remove package_name       # Remove a package
dpkg -l                            # List all installed packages
top                                # View running processes in real-time
htop                               # Enhanced top (requires install)
ps aux                             # List all active processes
kill PID                           # Kill a process by PID
killall process_name               # Kill all instances of a process
ip a                               # Show network interfaces and IPs
ping IP_or_domain                  # Test connectivity
netstat -tuln                      # Show open TCP/UDP ports
ss -tuln                           # Modern replacement for netstat
nmap 192.168.1.1                   # Scan ports (requires install)
curl http://example.com            # Fetch content from a website
wget http://example.com/file.txt   # Download a file from the internet
sudo ufw enable                    # Enable UFW firewall
sudo ufw status                    # Show current firewall rules
sudo ufw allow 22                  # Allow SSH (port 22)
sha256sum file.iso                 # Generate SHA256 hash of a file
md5sum file.txt                    # Generate MD5 hash (for verification)
journalctl                         # Show system logs
journalctl -u ssh                  # Logs for SSH service
tail -f /var/log/syslog            # Live stream logs
systemctl status service_name      # Show service status
systemctl start service_name       # Start a service
systemctl stop service_name        # Stop a service
systemctl enable service_name      # Enable service to start on boot

# Setting Up an Nginx Web Server on an Arch Linux Droplet

This guide will walk you through setting up an Nginx web server on an Arch Linux droplet. It's designed to be easy to follow, step by step.

### 1. Update Your System
Before we get started, make sure your system is up-to-date by running:
```bash
sudo pacman -Syu
```

### 2. Clone the Repository
Next, clone the repository that contains the setup script into your home directory:
```bash
git clone https://github.com/inspiritilda/2420_linux_assignment_3-1.git
```

### 3. Run the Setup Script
Now, change into the cloned directory and run the setup script with:
```bash
cd ~/nginx_setup
sudo ./setup_script
```
The script will automatically install and configure Nginx for you. It will also set up the necessary files and permissions.
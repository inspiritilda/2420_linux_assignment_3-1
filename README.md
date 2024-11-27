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
cd ~/nginx-setup
sudo ./setup-script
```
The script will automatically install and configure Nginx for you. It will also set up the necessary files and permissions.

### 4. Verify the Setup
Once the script is done, open your web browser and enter your droplet’s IP address. You should see the default Nginx welcome page.
If it’s not working, check the status of Nginx by running:
```bash
systemctl status nginx
```
If Nginx isn’t running, you can start it with:
```bash
sudo systemctl start nginx
```

### 5. Enabling Nginx to Start on Boot
To make sure Nginx starts automatically when your droplet reboots, run:
```bash
sudo systemctl enable nginx
```

### 6. Firewall Settings (UFW)
If you're using UFW (Uncomplicated Firewall), you’ll need to allow HTTP traffic to your server.
To allow HTTP traffic:
```bash
sudo ufw allow http
```
To enable firewall with:
```bash
sudo ufw --force enable
```
You can check the status of your firewall with:
```bash
sudo ufw status verbose
```

### 7. Restarting Nginx After Configuration Changes
If you make any changes to Nginx’s configuration, you’ll need to restart the server to apply the changes. Use this command:
```bash
sudo systemctl restart nginx
```

### 8. Checking Server Status
To check that Nginx is still running after restarting, use:
```bash
sudo systemctl status nginx
```

### 9. Testing the Web Server
After everything is set up, you can test the server again by typing your droplet's IP address into a web browser. If you see the default Nginx page, everything is working as expected!
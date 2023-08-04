# Network Scanner Project

This project is a network scanner that uses Nmap to scan a local network and presents the results in a structured format using PHP and Apache2.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Cron Job Configuration](#cron-job-configuration)

## Installation

Make sure you have the following dependencies installed:

- **Check if you're working on the latest version:**
  ```bash
  sudo apt-get update
  
- **Apache2:**
  ```bash
  sudo apt-get install apache2
  
- **nmap:**
  ```bash
  sudo apt-get install nmap
  
- **php:**
  ```bash
  sudo apt-get install php

Next, configure the ownership and permissions for the Apache web server:

```bash
sudo chown <your_username> /var/www/html
sudo chmod 777 /var/www/html
```

## Usage

```bash
git clone <>
```
**1. Move the project files to the Apache web server's root directory:**
```bash
sudo mv network_scanner /var/www/html/
```

**2. Access the web interface by navigating to http://localhost/Network.php/ in your web browser**

## Cron Job Configuration

To perform periodic network scans, we can set up a cron job to run Nmap at specified intervals. Open the cron table editor:

```bash
sudo crontab -e
```
Add the following line to the file to run the Nmap scan every 10 minutes:

```bash
*/10 * * * * nmap 192.168.1.0/24 -oN /var/www/html/nmap.html
```
Save and close the file.







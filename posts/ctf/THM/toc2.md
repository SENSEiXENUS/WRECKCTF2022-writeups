---------------------

### CTF: TRYHACKME
### LAB: TOC2

---------------------

![image](https://github.com/user-attachments/assets/e03e69fa-1a99-4bdf-8653-4418f7ba5aa8)

---------------------

### RECONNAISSANCE

- Rustscan's network scan output


      ❯ rustscan -a 10.10.59.48 -- -sC -sV
      .----. .-. .-. .----..---.  .----. .---.   .--.  .-. .-.
      | {}  }| { } |{ {__ {_   _}{ {__  /  ___} / {} \ |  `| |
      | .-. \| {_} |.-._} } | |  .-._} }\     }/  /\  \| |\  |
      `-' `-'`-----'`----'  `-'  `----'  `---' `-'  `-'`-' `-'
      The Modern Day Port Scanner.
      ________________________________________
      : https://discord.gg/GFrQsGy           :
      : https://github.com/RustScan/RustScan :
       --------------------------------------
      Please contribute more quotes to our GitHub https://github.com/rustscan/rustscan
      
      [~] The config file is expected to be at "/home/sensei/.rustscan.toml"
      [!] File limit is lower than default batch size. Consider upping with --ulimit. May cause harm to sensitive servers
      [!] Your file limit is very small, which negatively impacts RustScan's speed. Use the Docker image, or up the Ulimit with '--ulimit 5000'. 
      Open 10.10.59.48:22
      Open 10.10.59.48:80
      [~] Starting Script(s)
      [>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")
      
      [~] Starting Nmap 7.94SVN ( https://nmap.org ) at 2024-08-28 08:58 EDT
      NSE: Loaded 156 scripts for scanning.
      NSE: Script Pre-scanning.
      NSE: Starting runlevel 1 (of 3) scan.
      Initiating NSE at 08:58
      Completed NSE at 08:58, 0.00s elapsed
      NSE: Starting runlevel 2 (of 3) scan.
      Initiating NSE at 08:58
      Completed NSE at 08:58, 0.00s elapsed
      NSE: Starting runlevel 3 (of 3) scan.
      Initiating NSE at 08:58
      Completed NSE at 08:58, 0.00s elapsed
      Initiating Ping Scan at 08:58
      Scanning 10.10.59.48 [2 ports]
      Completed Ping Scan at 08:58, 0.21s elapsed (1 total hosts)
      Initiating Parallel DNS resolution of 1 host. at 08:58
      Completed Parallel DNS resolution of 1 host. at 08:58, 0.02s elapsed
      DNS resolution of 1 IPs took 0.03s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
      Initiating Connect Scan at 08:58
      Scanning 10.10.59.48 [2 ports]
      Discovered open port 22/tcp on 10.10.59.48
      Discovered open port 80/tcp on 10.10.59.48
      Completed Connect Scan at 08:58, 0.29s elapsed (2 total ports)
      Initiating Service scan at 08:58
      Scanning 2 services on 10.10.59.48
      Completed Service scan at 08:58, 6.45s elapsed (2 services on 1 host)
      NSE: Script scanning 10.10.59.48.
      NSE: Starting runlevel 1 (of 3) scan.
      Initiating NSE at 08:58
      Completed NSE at 08:58, 16.03s elapsed
      NSE: Starting runlevel 2 (of 3) scan.
      Initiating NSE at 08:58
      Completed NSE at 08:58, 0.87s elapsed
      NSE: Starting runlevel 3 (of 3) scan.
      Initiating NSE at 08:58
      Completed NSE at 08:58, 0.00s elapsed
      Nmap scan report for 10.10.59.48
      Host is up, received syn-ack (0.23s latency).
      Scanned at 2024-08-28 08:58:10 EDT for 24s
      
      PORT   STATE SERVICE REASON  VERSION
      22/tcp open  ssh     syn-ack OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
      | ssh-hostkey: 
      |   2048 84:4e:b1:49:31:22:94:84:83:97:91:72:cb:23:33:36 (RSA)
      | ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCuaqFOGQLuuh5gZPHAMXN7mbBvvKFQNjf7BE4nQcou0kK9vn/2NoMDyr3ZNKRvfG/Q2S+Nk1cew2KYvBN8OmJP0a4iTiQNd2MNftiOvH6zA7DbHD8WcuqoFNVUILB0fR3zHLOTJdZmvUX14TJnlGpd+Zt6wNOH9+EXNZDhjG7f7D/StcxurCuGAwkqQb7/oP5euE5sQaJ31ZnTL4RK4sk7LzXQprPBJa0IjEthBtKhSbKS0XmvzCFcSYNn/RUhFAOBR4WXKRGk9+WKlhj5KUli0BmUB6v9OnTcRZHjVQ7cj/8QoFYh5Ns38DM2oFYibhTGmODK6OeyOQgFe9iNc/KT
      |   256 cc:32:19:3f:f5:b9:a4:d5:ac:32:0f:6e:f0:83:35:71 (ECDSA)
      | ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBAXDnQKHAfzUPrhhICFpTSbE3+bjHgyIEapWhaEZkimi2WdGqPh3+vX7602C3+B4Q+TitOB+YR7xQNmUxk89vac=
      |   256 bd:d8:00:be:49:b5:15:af:bf:d5:85:f7:3a:ab:d6:48 (ED25519)
      |_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIJ3eshAl/8myavr2XQdEDrVBN5hBGf1Jwxn8CajXqhZ1
      80/tcp open  http    syn-ack Apache httpd 2.4.29 ((Ubuntu))
      |_http-title: Site Maintenance
      | http-robots.txt: 1 disallowed entry 
      |_/cmsms/cmsms-2.1.6-install.php
      | http-methods: 
      |_  Supported Methods: HEAD GET POST OPTIONS
      |_http-server-header: Apache/2.4.29 (Ubuntu)
      Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

-  FFUF's output

![image](https://github.com/user-attachments/assets/e3ca51a6-3cfc-4127-954c-4dc5449dc1a6)

- I discovered exposed credentials in the index page

![image](https://github.com/user-attachments/assets/a6c8b758-1bf1-48cc-abb4-4eea872f3ced)

- `Robots.txt` reveals an installation page and a note pointing to a database file named `cmsmsdb` which was recently created by the admin.

![image](https://github.com/user-attachments/assets/9b9d47b8-a6bf-4c27-a722-754affe9598e)

### CMSMS 2.1.6 exploit

- The `cmsms version 2.1.6` is vulnerable to `Remote Code Execution` as explained in [exploitdb](https://www.exploit-db.com/exploits/44192). The vulnerability entails injection of php code into a parameter `timestamp` while installing the cms on a server.

![image](https://github.com/user-attachments/assets/1ba899ea-a2d2-4071-90ed-ab09236ac6b7)

- I intercepted the request of stage 4's installation and tweaked the request as displayed below.












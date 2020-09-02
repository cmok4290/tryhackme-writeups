# Vulnversity

## [Task 1] Deploy the machine

## [Task 2] Reconnaissance
1. Scan this box: `nmap -sV <machines ip>`
2. Scan the box, how many ports are open?
    - 6
3. What version of the squid proxy is running on the machine?
    - 3.5.12
4. How many ports will nmap scan if the flag `-p-400` was used?
    - 400
5. Using the nmap flag `-n` what will it not resolve?
    - dns
6. What is the most likely operating system this machine is running?
    - ubuntu
7. What port is the web server running on?
    - 3333
8. It's important to ensure you are always doing your reconnaisance thoroughly before progressing. Knowing all open services (which can all be points of exploitation) is very important, don't forget that ports on a higher range might be open so always scan ports after 1000 (even if you leave scanning in the background).

## [Task 3] Locating directories using GoBuster
1. Let's first start off by scanning the website to find any hidden directories. To do this, we're going to use GoBuster.
    - `gobuster dir -u http://<ip>:3333 -w <word list location>`
2. What is the directory that has an upload form page?
    - /internal/

## [Task 4] Compromise the webserver
1. Try to upload a few file types to the server, what common extensions seem to be blocked?
    - .php
2. To identify which extensions are not blocked, we're going to fuzz the upload form. To do this, we're doing to use BurpSuite. If you are unsure to what BurpSuite is, or how to set it up please complete our BurpSuite room first.
3. We're going to use Intruder (used for automating customised attacks).
- phpext.txt
    ```
    .php
    .php3
    .php4
    .php5
    .phtml
    ```
- Run this attack, what extension is allowed?
    - .phtml
4. Now we know what extension we can use for our payload, we can progress.
5. What is the name of the user who manages the webserver?
    - bill
6. What is the user flag?
    - 8bd7992fbe8a6ad22a63361004cfcedb

## [Task 5] Privilege Escalation
Now you have compromised the machine, we are going to escalate our privileges and become the superuser (root).
1. On the system, search for all SUID files. What file stands out?
    - find / -user root -perm -4000 -print 2>/dev/null
    - /bin/systemctl
2. It's challenge time! We have guided you through this far, are you able to exploit this system further to escalate your privileges and get the final answer? Become root and get the last flag (/root/root.txt).
    - https://gtfobins.github.io/gtfobins/systemctl/
    - a58ff8579f0a9270368d33a9966c7fd5


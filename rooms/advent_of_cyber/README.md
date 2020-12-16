# Advent of Cyber

## Task 1: Introduction

## Task 2: Our Socials
1. Join our [Discord](https://discord.gg/tryhackme) and say hi!
2. Follow us on [Twitter](https://twitter.com/RealTryHackMe)!
3. Check out the [subreddit](https://www.reddit.com/r/tryhackme/)!

## Task 3: Short Tutorials & Rules

## Task 4: Subscribing

## Task 5: The Story

## [Day 1] Web Exploitation: A Christmas Crisis
1. Deploy your AttackBox (the blue "Start AttackBox" button) and the tasks machine (green button on this task) if you haven't already. Once both have deployed, open FireFox on the AttackBox and copy/paste the machines IP into the browser search bar.
2. Register for an account, and then login. What is the name of the cookie used for authentication?
    - auth
3. In what format is the value of this cookie encoded?
    - hexadecimal 
4. Having decoded the cookie, what format is the data stored in?
    - json
5. Figure out how to bypass the authentication. What is the value of Santa's cookie?
    - 7b22636f6d70616e79223a22546865204265737420466573746976616c20436f6d70616e79222c2022757365726e616d65223a2273616e7461227d
6. What is the flag you're given when the line is fully active?
    - THM{MjY0Yzg5NTJmY2Q1NzM1NjBmZWFhYmQy}

## [Day 2] Web Exploitation: The Elf Strikes Back!
- [php-reverse-shell.php](https://raw.githubusercontent.com/pentestmonkey/php-reverse-shell/master/php-reverse-shell.php)
1. What string of text needs adding to the URL to get access to the upload page?
    - ?id=ODIzODI5MTNiYmYw
2. What type of file is accepted by the site?
    - image
3. Bypass the filter and upload a reverse shell. In which directory are the uploaded files stored?
    - /uploads/
4. Activate your reverse shell and catch it in a netcat listener!
    - `sudo nc -lvnp 443`
5. What is the flag in /var/www/flag.txt?
    - THM{MGU3Y2UyMGUwNjExYTY4NTAxOWJhMzhh}

## [Day 3] Web Exploitation: Christmas Chaos
1. Deploy your AttackBox (the blue "Start AttackBox" button) and the tasks machine (green button on this task) if you haven't already. Once both have deployed, open Firefox on the AttackBox and copy/paste the machines IP (MACHINE_IP) into the browser search bar.
2. Use BurpSuite to brute force the login form. Use the following lists for the default credentials:
Username | Password
---
root | root
admin | password
user | 12345

Use the correct credentials to log in to the Santa Sleigh Tracker app. Don't forget to turn off Foxyproxy once BurpSuite has finished the attack!
    - THM{885ffab980e049847516f9d8fe99ad1a}

## [Day 4] Web Exploitation: Santa's Watching
1. Deploy your AttackBox (the blue "Start AttackBox" button) and the tasks machine (green button on this task) if you haven't already. Once both have deployed, open FireFox on the AttackBox and copy/paste the machines IP (MACHINE_IP) into the browser search bar.
2. Given the URL "http://shibes.xyz/api.php", what would the entire wfuzz command look like to query the "breed" parameter using the wordlist "big.txt" (assume that "big.txt" is in your current directory)

Note: For legal reasons, do not actually run this command as the site in question has not consented to being fuzzed!
    - `wfuzz -c -z file,big.txt http://shibes.xyz/api.php?breed=FUZZ`
3. Use GoBuster (against the target you deployed -- not the shibes.xyz domain) to find the API directory. What file is there?
    - site-log.php
4. Fuzz the date parameter on the file you found in the API directory. What is the flag displayed in the correct post?
    - THM{D4t3_AP1} 

## [Day 5] Web Exploitation: Someone stole Santa's gift list!
1. Without using directory brute forcing, what's Santa's secret login panel?
    - /santapanel
2. Visit Santa's secret login panel and bypass the login using SQLi.
3. How many entries are there in the gift database?
    - 22
4. What did Paul ask for?
    - github ownership
5. What is the flag?
    - thmfox{All_I_Want_for_Christmas_Is_You}
6. What is admin's password?
    - EhCNSWzzFP6sc7gB

## [Day 6] Web Exploitation: Be careful with what you wish on Christmas night
- [OWASP/CheatSheetSeries](https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/Input_Validation_Cheat_Sheet.md)
- [swisskyrepo/PayloadsAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/XSS%20Injection)
- [payloadbox/xss-payload-list](https://github.com/payloadbox/xss-payload-list)
- [Learn OWASP Zap](https://tryhackme.com/room/learnowaspzap)
1. Deploy your AttackBox (the blue "Start AttackBox" button) and the tasks machine (green button on this task) if you haven't already. Once both have deployed, open Firefox on the AttackBox and copy/paste the machines IP (http://MACHINE_IP:5000) into the browser search bar (the webserver is running on port 5000, so make sure this is included in your web requests).
2. What vulnerability type was used to exploit the application?
    - stored cross-site scripting
3. What query string can be abused to craft a reflected XSS?
    - q
4. Launch the OWASP ZAP Application
5. Run a ZAP (zaproxy) automated scan on the target. How many XSS alerts are in the scan?
    - 2
6. Explore the XSS alerts that ZAP has identified, are you able to make an alert appear on the "Make a wish" website?

## [Day 7] Networking: The Grinch Really Did Steal Christmas
1. Open "pcap1.pcap" in Wireshark. What is the IP address that initiates an ICMP/ping?
    - 10.11.3.2
2. If we only wanted to see HTTP GET requests in our "pcap1.pcap" file, what filter would we use?
    - http.request.method == GET
3. Now apply this filter to "pcap1.pcap" in Wireshark, what is the name of the article that the IP address "10.10.67.199" visited?
    - reindeer-of-the-week
4. Let's begin analysing "pcap2.pcap". Look at the captured FTP traffic; what password was leaked during the login process? There's a lot of irrelevant data here - Using a filter here would be useful!
    - plaintext_password_fiasco
5. Continuing with our analysis of "pcap2.pcap", what is the name of the protocol that is encrypted?
    - ssh
6. Analyse "pcap3.pcap" and recover Christmas! What is on Elf McSkidy's wishlist that will be used to replace Elf McEager?
    - Rubber ducky

## [Day 8] Networking: What's Under the Christmas Tree?
1. When was Snort created?
    - 1998
2. Using Nmap on MACHINE_IP, what are the port numbers of the three services running?  (Please provide your answer in ascending order/lowest -> highest, separated by a comma) 
    - 80,2222,3389
3. Run a scan and provide the `-Pn` flag to ignore ICMP being used to determine if the host is up
4. Experiment with different scan settings such as `-A` and `-sV` whilst comparing the outputs given.
5. Use Nmap to determine the name of the Linux distribution that is running, what is reported as the most likely distribution to be running?
    - Ubuntu
6. Use Nmap's Network Scripting Engine (NSE) to retrieve the "HTTP-TITLE" of the webserver. Based on the value returned, what do we think this website might be used for?
    - blog
7. Now use different scripts against the remaining services to discover any further information about them.

## [Day 9] Networking: Anyone can be Santa!
1. Name the directory on the FTP server that has data accessible by the "anonymous" user
    - public
2. What script gets executed within this directory?
    - backup.sh
3. What movie did Santa have on his Christmas shopping list?
    - The Polar Express
4. Re-upload this script to contain malicious data (just like we did in section 9.6. Output the contents of /root/flag.txt! Note that the script that we have uploaded may take a minute to return a connection. If it doesn't after a couple of minutes, double-check that you have set up a Netcat listener on the device that you are working from, and have provided the TryHackMe IP of the device that you are connecting from.
    - THM{even_you_can_be_santa}

## [Day 10] Networking: Don't be sElfish!
1. Using enum4linux, how many users are there on the Samba server (MACHINE_IP)?
    - 3
2. Now how many "shares" are there on the Samba server?
    - 4
3. Use smbclient to try to login to the shares on the Samba server (MACHINE_IP). What share doesn't require a password?
    - tbfc-santa
4. Log in to this share, what directory did ElfMcSkidy leave for Santa?
    - jingle-tunes

## [Day 11] Networking: The Rogue Gnome
1. What type of privilege escalation involves using a user account to execute commands as an administrator?
    - vertical
2. What is the name of the file that contains a list of users who are a part of the sudo group?
    - sudoers
3. Use ssh to log in to the vulnerable machine like so: `ssh cmnatic@MACHINE_IP`. Input the following password when prompted: aoc2020
4. Enumerate the machine for executables that have had the SUID permission set. Look at the output and use a mixture of [GTFObins](https://gtfobins.github.io/) and your researching skills to learn how to exploit this binary. You may find uploading some of the enumeration scripts that were used during today's task to be usefule. 
5. Use this executable to launch a system shell as root. What are the contents of the file located at /root/flag.txt?
    - thm{2fb10afe933296592}


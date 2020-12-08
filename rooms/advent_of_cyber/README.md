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

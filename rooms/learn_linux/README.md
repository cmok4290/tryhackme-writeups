# Learn Linux

## [Task 1] Intro
- Deploy

## [Task 2] Methodology

## [Task 3] [Section 1: SSH] - Intro

## [Task 4] [Section 1: SSH] - Putty and ssh
- `ssh shiba1@BOX_IP`

## [Task 5] [Section 2: Running Commands] - Basic Command Execution
- `echo hello`

## [Task 6] [Section 2: Running Commands] - Manual Pages and Flags
- `man echo`
- `echo -n Shiba`
- `echo -n hello`

## [Task 7] [Section 3: Basic File Operations] - ls
- `ls`
- `ls -a`
1. What flag outputs all entries?
    - `-a`
2. What flag outputs things in a "long list" format?
    - `-l`

## [Task 8] [Section 3: Basic File Operations] - cat
- `cat --help`
1. What flag numbers all output lines?
    - `-n`

## [Task 9] [Section 3: Basic File Operations] - touch
- `touch b.txt`

## [Task 10] [Section 3: Basic File Operations] - Running A Binary
- `ls .`
1. How would you run a binary called hello using the directory shorcut __.__?
    - `./hello`
2. How would you run a binary called hello in your home directory using the shortcut __~__?
    - `~/hello`
3. How would you run a binary called hello in the previous directory using the shortcut __..__?
    - `../hello`

## [Task 11] Binary - Shiba1
- `touch noot.txt`
- `./shiba1`
1. What's the password for shiba2?
    - pinguftw

## [Task 12] su
- `su shiba2`
1. How do you specify which shell is used when you login?
    - `-s`

## [Task 13] [Section 4: Linux Operators] - Intro

## [Task 14] [Section 4: Linux Operators] - ">"
1. How would you output twenty to a file called test?
    - `echo twenty > test`

## [Task 15] [Section 4: Linux Operators] - ">>"
- `echo hello >> file`

## [Task 16] [Section 4: Linux Operators] - "&&"
- `ls && echo hello`
- `echo hello >> file2 && cat file2`

## [Task 17] [Section 4: Linux Operators] - "&"
- `sleep 5`
- `sleep 5 &`

## [Task 18] [Section 4: Linux Operators] - "$"
- `echo $USER`
- `touch $USER`
- `echo hi >> $USER`
- `cat shiba2`
- `export nootnoot=test`
- `echo $nootnoot`
1. How would you set nootnoot equal to 1111?
    - `export nootnoot=1111`
2. What is the value of the home environment variable?
    - /home/shiba2

## [Task 19] [Section 4: Linux Operators] - "|"
- `cat test | grep noot`
- `cat test | grep 123`
- `cat -`

## [Task 20] [Section 4: Linux Operators] - ";"
- `dkhsgffgsafgfasdgfasfghkgdsgfs; ls`

## [Task 21] Binary - shiba2
- `echo test1234=$USER`
1. What is shiba3's password?
    - happynootnoises

## [Task 22] [Section 5: Advanced File Operations] - Intro

## [Task 23] [Section 5: Advanced File Operations] - A bit of background

## [Task 24] [Section 5: Advanced File Operations] - chmod
1. What permissions mean the user can read the file, the group can read and write to the file, and no one else can read, write or execute the file?
    - 460
2. What permissions mean the user can read, write, and execute the file, the group can read, write, and execute the file, and everyone else can read, write, and execute the file?
    - 777


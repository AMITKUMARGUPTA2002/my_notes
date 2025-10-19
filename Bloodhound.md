```sh
sudo neo4j start
```

```sh
sudo /home/kali/oscp/oscpa/BloodHound-linux-x64/BloodHound --no-sandbox
```

```sh
powershell -exec bypass -Command "Import-Module .\SharpHound.ps1; Invoke-BloodHound -CollectionMethod All"

```

```password
4^nENFx&Jua~:PC
```

```
powershell -exec bypass -Command "Import-Module .\PowerView.ps1"
```

```
. ./PowerView.ps1
```

```
Get-DomainUser | Select samaccountname,description
```

```
Get-DomainGroupMember -Identity "Domain Admins"
```

```
Get-DomainObjectAcl -Identity "Domain Admins" -ResolveGUIDs -Verbose
```

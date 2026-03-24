# MySQL

## What is MySQL?

MySQL is a database service used to store and manage data.

---

## Basic Scan

```bash id="y6k2p1"
nmap -p3306 target
```

Check if MySQL service is running.

---

## Service Detection

```bash id="r8n4t3"
nmap -sV -p3306 target
```

Detect MySQL version.

---

## MySQL Login

```bash id="k3w7z9"
mysql -h target -u root -p
```

Try to login to the database.

---

## Enumeration with Metasploit

```bash id="p1x9m4"
use auxiliary/scanner/mysql/mysql_version
set RHOSTS target
run
```

Get MySQL version.

---

```bash id="q5d2v8"
use auxiliary/scanner/mysql/mysql_login
set RHOSTS target
run
```

Try to find valid credentials.

---

## Notes

* Port 3306 → MySQL
* Default user is often root
* Weak passwords can be exploited

> Tested during labs

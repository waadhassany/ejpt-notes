# FTP

## What is FTP?

FTP (File Transfer Protocol) is used to transfer files between a client and a server.

---

## Basic Scan

```bash id="8g7y2l"
nmap -p21 target
```

Used to check if FTP service is running.

---

## Anonymous Login

```bash id="7p3v0s"
ftp target
```

Try logging in with:

* username: anonymous
* password: anonymous

---

## FTP Enumeration with Nmap

```bash id="0x3k8n"
nmap -p21 --script ftp-anon target
nmap -p21 --script ftp-brute target
```

* ftp-anon → check anonymous access
* ftp-brute → brute force login

---

## Brute Force with Hydra

```bash id="3r7t2m"
hydra -l user -P passwords.txt ftp://target
```

---

## Notes

* Port 21 → FTP
* Anonymous login = misconfiguration
* Weak credentials can be exploited

> Tested during labs

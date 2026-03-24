# SMB

## What is SMB?

SMB (Server Message Block) is a protocol used for file sharing and communication between systems.

---

## Basic Scan

```bash
nmap -p445 target
```

Used to check if SMB service is running.

---

## SMB Enumeration with Nmap

```bash
nmap -p445 --script smb-protocols target
nmap -p445 --script smb-enum-users target
nmap -p445 --script smb-enum-shares target
```

* smb-protocols → shows supported SMB versions
* smb-enum-users → lists users
* smb-enum-shares → lists shared folders

---

## Access Shares

```bash
smbclient -L //target -U user
```

List available shares.

---

## Connect to Share

```bash
smbclient //target/share -U user
```

Access a specific share.

---

## Notes

* Port 445 → SMB
* Anonymous login may be allowed (null session)
* Misconfigurations can expose sensitive data

> Tested during labs

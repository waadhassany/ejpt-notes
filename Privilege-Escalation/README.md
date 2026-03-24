# Privilege Escalation

## What is Privilege Escalation?

Privilege escalation is the process of gaining higher access or permissions on a system.

---

## Basic Enumeration

```bash id="x3p8k1"
whoami
id
```

Check current user and privileges.

---

## Check SUID Files

```bash id="f6n2v4"
find / -perm -4000 2>/dev/null
```

Find files with SUID permission.

---

## Check Cron Jobs

```bash id="k7w5t2"
crontab -l
ls -la /etc/cron*
```

Look for scheduled tasks that can be exploited.

---

## Check Writable Files

```bash id="q9m3z8"
find / -writable 2>/dev/null
```

Find files with write permissions.

---

## Linux Privilege Escalation Tools

```bash id="b2c7x6"
linpeas.sh
```

Automated script for finding vulnerabilities.

---

## Windows Privilege Escalation Tools

```bash id="z4n1l9"
PowerUp.ps1
```

Used to find privilege escalation opportunities.

---

## Notes

* Always enumerate first
* Look for misconfigurations
* Weak permissions can lead to escalation

> Tested during labs

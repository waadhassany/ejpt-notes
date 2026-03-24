# Privilege Escalation

## What is Privilege Escalation?

Privilege escalation is the process of gaining higher access or permissions on a system.

---

## Basic Enumeration

```bash
whoami
id
```

Check current user and privileges.

---

## Check SUID Files

```bash
find / -perm -4000 2>/dev/null
```

Find files with SUID permission.

---

## Check Cron Jobs

```bash
crontab -l
ls -la /etc/cron*
```

Look for scheduled tasks that can be exploited.

---

## Check Writable Files

```bash
find / -writable 2>/dev/null
```

Find files with write permissions.

---

## Linux Privilege Escalation Tools

```bash
linpeas.sh
```

Automated script for finding vulnerabilities.

---

## Windows Privilege Escalation Tools

```bash
PowerUp.ps1
```

Used to find privilege escalation opportunities.

---

## Notes

* Always enumerate first
* Look for misconfigurations
* Weak permissions can lead to escalation

> Tested during labs

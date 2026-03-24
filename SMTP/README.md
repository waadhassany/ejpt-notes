# SMTP

## What is SMTP?

SMTP (Simple Mail Transfer Protocol) is used to send emails between servers.

---

## Basic Scan

```bash id="x8p2k4"
nmap -p25 target
```

Check if SMTP service is running.

---

## Service Detection

```bash id="f3n7v1"
nmap -sV -p25 target
```

Detect SMTP version and banner.

---

## Banner Grabbing

```bash id="k2w6t9"
nc target 25
```

Connect to SMTP service and view banner.

---

## SMTP Commands

```bash id="q7m1z5"
VRFY user
EHLO attacker.com
```

* VRFY → check if user exists
* EHLO → list supported commands

---

## Enumeration with Tool

```bash id="b4c9x2"
smtp-user-enum -U users.txt -t target
```

Find valid users.

---

## Notes

* Port 25 → SMTP
* VRFY may reveal valid users
* Misconfigurations can leak information

> Tested during labs

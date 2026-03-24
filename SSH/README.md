# SSH

## What is SSH?

SSH (Secure Shell) is used to remotely access and control systems securely.

---

## Basic Scan

```bash id="s8x2p4"
nmap -p22 target
```

Check if SSH service is running.

---

## Service Detection

```bash id="f7n3v1"
nmap -sV -p22 target
```

Detect SSH version.

---

## SSH Login

```bash id="k9w1t6"
ssh user@target
```

Connect to the target using SSH.

---

## Brute Force with Hydra

```bash id="q2m7z5"
hydra -L users.txt -P passwords.txt ssh://target
```

Try to find valid credentials.

---

## Notes

* Port 22 → SSH
* Requires valid credentials
* Weak passwords can be exploited

> Tested during labs

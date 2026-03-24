# HTTP

## What is HTTP?

HTTP (Hypertext Transfer Protocol) is used for communication between web clients and servers.

---

## Basic Scan

```bash id="k1x2p9"
nmap -p80 target
```

Used to check if HTTP service is running.

---

## Service Detection

```bash id="z7v3m1"
nmap -sV -p80 target
```

Detect web server version.

---

## Directory Enumeration

```bash id="h8t4n2"
dirb http://target
```

Find hidden directories.

---

## Nmap HTTP Scripts

```bash id="p3q9r7"
nmap -p80 --script http-enum target
nmap -p80 --script http-headers target
```

* http-enum → find directories
* http-headers → show server headers

---

## Using Curl

```bash id="c6w1x8"
curl http://target
```

View HTTP response.

---

## Notes

* Port 80 → HTTP
* Look for hidden directories and files
* Check server headers for information

> Tested during labs

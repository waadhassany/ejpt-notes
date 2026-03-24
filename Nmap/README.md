# Nmap

## 🔍 What is Nmap?

Nmap (Network Mapper) is a tool used to discover hosts, open ports, and services on a network.

---

## 🚀 Basic Scan

```bash
nmap target
```
<img width="807" height="245" alt="image" src="https://github.com/user-attachments/assets/36b3199a-fe54-4e0e-a8dc-c322b14d8c45" />

---

## 🧠 Host Discovery

```bash
nmap -Pn target

```
<img width="594" height="291" alt="image" src="https://github.com/user-attachments/assets/a0f2965b-886b-49de-ba7c-0f04dd21626d" />

* Skip ping
* Useful when ICMP is blocked

---

## 🚪 Port Scanning

```bash
nmap -p 80 target
nmap -p- target
```
<img width="671" height="321" alt="image" src="https://github.com/user-attachments/assets/1ca90563-e004-4347-8e41-659f6148ffed" />
<img width="719" height="173" alt="image" src="https://github.com/user-attachments/assets/2fd748fe-5503-4643-89eb-7cb8cdc1078d" />


* Scan specific port
* Scan all ports

---

## 🧬 Service Detection

```bash
nmap -sV target
```
<img width="640" height="313" alt="image" src="https://github.com/user-attachments/assets/9e61698d-bf25-435d-9867-d9610a743484" />


* Detect service versions

---

## ⚡ Aggressive Scan

```bash
nmap -A target
```
<img width="1869" height="606" alt="image" src="https://github.com/user-attachments/assets/f55290a5-d9fd-4893-98a2-97fb779ec56a" />

* OS detection
* Version detection
* Script scanning

---

## 🧱 SMB Enumeration

```bash
nmap -p445 --script smb-protocols target
nmap -p445 --script smb-enum-users target
nmap -p445 --script smb-enum-shares target
```
<img width="583" height="398" alt="image" src="https://github.com/user-attachments/assets/e39ce800-4d7e-4961-a388-e7665061366a" />
<img width="649" height="335" alt="image" src="https://github.com/user-attachments/assets/cd208db1-a237-4561-8859-d60806253170" />
<img width="751" height="636" alt="image" src="https://github.com/user-attachments/assets/c7e1e858-12fe-4078-a2ef-741378313714" />


---

## 📁 Save Results

```bash
nmap -oX scan.xml target
```
<img width="644" height="275" alt="image" src="https://github.com/user-attachments/assets/52c11863-f0b1-4638-a3fa-77f6d3367d36" />

---

## ⚠️ Notes

* Filtered = firewall blocking the request
* Open = service is running
* Closed = port is accessible but no service

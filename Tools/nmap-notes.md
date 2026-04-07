# 🌐 Nmap Notes for Security Testing

## 📌 Objective

Understand how Nmap is used for network discovery, service detection, and basic security assessment.

---

## 🧠 What is Nmap?

Nmap (Network Mapper) is a tool used to discover hosts, identify open ports, detect running services, and gather information about systems on a network.

---

## 🔍 Common Use Cases

* Host discovery
* Port scanning
* Service version detection
* OS detection
* Network enumeration

---

## 🧪 Common Commands

### 1️⃣ Basic Scan

```bash
nmap 192.168.1.10
```

Scans the most common ports on the target.

---

### 2️⃣ Scan Specific Ports

```bash
nmap -p 22,80,443 192.168.1.10
```

Checks whether selected ports are open.

---

### 3️⃣ Service Version Detection

```bash
nmap -sV 192.168.1.10
```

Identifies services and versions running on open ports.

---

### 4️⃣ OS Detection

```bash
nmap -O 192.168.1.10
```

Attempts to detect the operating system.

---

### 5️⃣ SYN Scan

```bash
nmap -sS 192.168.1.10
```

Performs a stealthy TCP SYN scan.

---

### 6️⃣ Full Port Scan

```bash
nmap -p- 192.168.1.10
```

Scans all 65535 TCP ports.

---

### 7️⃣ Aggressive Scan

```bash
nmap -A 192.168.1.10
```

Performs OS detection, version detection, script scanning, and traceroute.

---

## 📌 Important Ports to Remember

* 21 → FTP
* 22 → SSH
* 23 → Telnet
* 25 → SMTP
* 53 → DNS
* 80 → HTTP
* 110 → POP3
* 139 → NetBIOS
* 143 → IMAP
* 443 → HTTPS
* 445 → SMB
* 3389 → RDP

---

## ⚠️ Security Relevance

Nmap helps identify:

* Unnecessary open ports
* Exposed services
* Legacy protocols
* Potential attack surface

---

## 🛡️ Best Practice

Always use Nmap only on authorized systems and approved lab environments.

---

## 🎯 Conclusion

Nmap is one of the most important tools for network reconnaissance and security testing.


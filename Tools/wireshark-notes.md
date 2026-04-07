# 📡 Wireshark Notes for SOC Analysis

## 📌 Objective

Understand how Wireshark is used to capture and analyze network traffic for security investigations.

---

## 🧠 What is Wireshark?

Wireshark is a network packet analyzer used to capture and inspect data traveling across a network in real time.

---

## 🔍 Common Use Cases

* Network troubleshooting
* Detecting suspicious traffic
* Malware traffic analysis
* Investigating data exfiltration
* Protocol analysis

---

## 🧪 Important Filters

### 1️⃣ HTTP Traffic

```wireshark
http
```

---

### 2️⃣ DNS Traffic

```wireshark
dns
```

---

### 3️⃣ TCP Traffic

```wireshark
tcp
```

---

### 4️⃣ Specific IP

```wireshark
ip.addr == 192.168.1.10
```

---

### 5️⃣ Failed Connections

```wireshark
tcp.flags.reset == 1
```

---

### 6️⃣ Suspicious Traffic (Non-standard Ports)

```wireshark
!(tcp.port == 80 || tcp.port == 443)
```

---

## 🔎 Investigation Workflow

1. Capture traffic
2. Apply filters
3. Identify unusual patterns
4. Follow TCP stream
5. Extract suspicious data

---

## 🚨 Indicators of Suspicious Activity

* Unusual DNS queries
* Large outbound data transfers
* Communication with unknown IPs
* Repeated connection attempts
* Data sent over non-standard ports

---

## 🛠️ Features Used

* Display Filters
* Follow TCP Stream
* Packet Details Pane
* Export Objects

---

## ⚠️ Security Relevance

Wireshark helps SOC Analysts detect:

* Data exfiltration
* Command & Control (C2) communication
* Malware traffic
* Network anomalies

---

## 🛡️ Best Practice

Use Wireshark in lab environments or authorized networks only.

---

## 🎯 Conclusion

Wireshark is an essential tool for network-level analysis and incident investigation in SOC environments.


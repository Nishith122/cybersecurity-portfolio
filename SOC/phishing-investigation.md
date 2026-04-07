# 📧 Phishing Email Investigation – SOC Analyst Approach

## 📌 Objective

Investigate a phishing email incident and determine if it is malicious.

---

## 🧠 What is Phishing?

Phishing is a social engineering attack where attackers trick users into clicking malicious links or providing sensitive information.

---

## 🚨 Scenario

A user reports that they clicked on a suspicious email link.

---

## 🔍 Investigation Steps

### 1️⃣ Analyze Email Headers

* Check sender email address (spoofing)
* Verify SPF, DKIM, DMARC results
* Look for mismatched domains

---

### 2️⃣ Analyze the URL

* Open link in a safe environment (sandbox)
* Check domain reputation using VirusTotal
* Look for typosquatting (e.g., gooogle.com)

---

### 3️⃣ Check Endpoint Activity

* Review browser history
* Look for file downloads
* Check process execution (e.g., PowerShell, scripts)

---

### 4️⃣ Check Network Logs

* Identify outbound connections to suspicious IPs
* Look for unusual traffic patterns

---

### 5️⃣ Check SIEM Alerts

* Search for related alerts in Splunk/Wazuh
* Correlate with user activity and timestamps

---

## 🛠️ Tools Used

* Splunk / Wazuh (SIEM)
* VirusTotal
* Browser Developer Tools
* Endpoint Detection Tools (EDR)

---

## 🚨 Impact

* Credential theft
* Malware infection
* Unauthorized access

---

## 🛡️ Response Actions

* Isolate affected system
* Reset user credentials
* Block malicious domain/IP
* Inform security team
* Educate user

---

## 🎯 Conclusion

Phishing attacks can be effectively investigated by combining email analysis, URL inspection, endpoint monitoring, and SIEM correlation.


# 🔍 Brute Force Attack Detection – Splunk

## 📌 Objective

Detect and analyze brute-force login attempts using Windows Event Logs in Splunk.

---

## 🧠 What is a Brute Force Attack?

A brute-force attack is when an attacker tries multiple passwords repeatedly to gain unauthorized access.

---

## 📊 Detection Query (Splunk)

```
index=windows EventCode=4625
| stats count by src_ip, user 
| where count > 10

---

## 📌 Explanation

* EventCode 4625 → Failed login attempts
* stats count → Counts attempts per IP/user
* where count > 10 → Filters suspicious activity

---

## 🔎 Investigation Steps

1. Identify source IP generating multiple failures
2. Check if same user is targeted
3. Look for successful login (Event ID 4624) after failures
4. Correlate with endpoint logs
5. Check geolocation of IP

---

## 🚨 Impact

* Account compromise
* Unauthorized access
* Privilege escalation

---

## 🛡️ Mitigation

* Enable account lockout policy
* Use multi-factor authentication (MFA)
* Block suspicious IPs
* Monitor failed login thresholds

---

## 🎯 Conclusion

Brute-force attacks can be effectively detected using log correlation in SIEM tools like Splunk.


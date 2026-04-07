# 📊 Splunk Queries for SOC Analyst (L1)

## 📌 Objective

Provide commonly used Splunk queries for detecting security incidents.

---

## 🔐 1. Failed Login Attempts (Brute Force Detection)

```id="d6k9p2"
index=windows EventCode=4625
| stats count by src_ip, user
| where count > 10
```

### 📌 Use Case:

Detect brute-force attacks by identifying multiple failed logins.

---

## 🔓 2. Successful Logins After Failures

```id="d7h3l1"
index=windows (EventCode=4624 OR EventCode=4625)
| stats count by user, EventCode
```

### 📌 Use Case:

Check if attacker succeeded after multiple failures.

---

## 🖥️ 3. PowerShell Execution Detection

```id="d8m2q4"
index=windows EventCode=4688
| search process_name="powershell.exe"
```

### 📌 Use Case:

Detect suspicious PowerShell activity (common in attacks).

---

## 🌐 4. Suspicious Outbound Traffic

```id="d9x7z5"
index=network
| stats count by dest_ip
| sort - count
```

### 📌 Use Case:

Identify unusual outbound connections.

---

## 📧 5. Possible Phishing Indicators

```id="b2n5r6"
index=email
| search subject="urgent" OR subject="password reset"
```

### 📌 Use Case:

Detect suspicious email patterns.

---

## 🧠 Key Concepts

* Index → Data source
* EventCode → Type of event
* stats → Aggregation
* search → Filtering

---

## 🎯 Conclusion

Splunk queries help SOC Analysts quickly detect and investigate security incidents using log data.


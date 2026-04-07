# 🛠️ Burp Suite Guide for Web Application Testing

## 📌 Objective

Understand how Burp Suite is used to capture, inspect, and test web application traffic.

---

## 🧠 What is Burp Suite?

Burp Suite is a web security testing tool used to intercept HTTP/HTTPS requests, modify traffic, and identify web vulnerabilities.

---

## 🔍 Main Uses

* Capture requests and responses
* Modify parameters
* Test authentication and authorization
* Replay requests
* Find vulnerabilities in web applications and APIs

---

## 🧰 Important Burp Suite Features

### 1️⃣ Proxy

Used to intercept browser traffic between the client and server.

### 2️⃣ Repeater

Used to resend and modify captured requests manually.

### 3️⃣ Intruder

Used to automate payload testing such as brute-force or fuzzing.

### 4️⃣ Decoder

Used to encode and decode data such as URL, Base64, and HTML.

### 5️⃣ Comparer

Used to compare two requests or responses.

---

## 📌 Basic Workflow

### Step 1

Open Burp Suite and enable intercept.

### Step 2

Configure browser to send traffic through Burp Proxy.

### Step 3

Browse the target application.

### Step 4

Capture request in Proxy.

### Step 5

Send request to Repeater.

### Step 6

Modify parameters and analyze response.

---

## 🧪 Example Testing Scenarios

### XSS Testing

Inject:

```html
<script>alert(1)</script>
```

### IDOR Testing

Change:

```http
GET /api/user/profile?id=123
```

to:

```http
GET /api/user/profile?id=124
```

### Authentication Testing

* Remove token
* Use invalid token
* Replay request after logout

---

## ⚠️ Security Relevance

Burp Suite helps identify:

* XSS
* SQL Injection
* IDOR
* Broken Access Control
* Missing Authentication
* Sensitive Data Exposure

---

## 🛡️ Best Practice

Use Burp Suite only on authorized targets, labs, and legal bug bounty programs.

---

## 🎯 Conclusion

Burp Suite is one of the most essential tools for VAPT, bug bounty, and API security testing.


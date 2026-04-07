# 💥 Cross-Site Scripting (XSS) Vulnerability Report

## 📌 Objective

Identify and demonstrate a Cross-Site Scripting (XSS) vulnerability in a web application.

---

## 🧠 What is XSS?

XSS (Cross-Site Scripting) is a vulnerability where an attacker injects malicious JavaScript into a web application, which executes in another user's browser.

---

## 🚨 Vulnerability Type

Reflected XSS

---

## 🔍 Testing Approach

1. Identify input fields (search, login, forms)
2. Inject test payloads
3. Observe response in browser

---

## 🧪 Payload Used

```html
<script>alert(1)</script>
```

---

## 📌 Steps to Reproduce

1. Navigate to vulnerable input field
2. Enter payload: `<script>alert(1)</script>`
3. Submit request
4. JavaScript executes in browser

---

## 🎯 Impact

* Session hijacking
* Cookie theft
* Account takeover
* Defacement

---

## 🛡️ Mitigation

* Input validation
* Output encoding
* Use Content Security Policy (CSP)
* Avoid directly rendering user input

---

## 🧰 Tools Used

* Burp Suite
* Browser Developer Tools

---

## 🎯 Conclusion

XSS vulnerabilities can lead to severe client-side attacks and must be properly mitigated using secure coding practices.


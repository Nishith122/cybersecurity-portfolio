# 🔓 IDOR (Insecure Direct Object Reference) Vulnerability Analysis

## 📌 Objective

Identify and demonstrate an IDOR vulnerability in an application by accessing unauthorized data.

---

## 🧠 What is IDOR?

IDOR (Insecure Direct Object Reference) is a type of Broken Access Control where an attacker can access or modify resources by changing an identifier (ID) without proper authorization.

---

## 🚨 Vulnerability Type

Broken Access Control (OWASP Top 10)

---

## 🔍 Testing Approach

1. Create two user accounts (User A and User B)
2. Capture request using Burp Suite
3. Identify user-specific parameter (e.g., user_id)
4. Modify parameter and send request

---

## 🧪 Example Request

### Original Request (User A)

```http id="h7k2lm"
GET /api/user/profile?id=123 HTTP/1.1
Authorization: Bearer TOKEN_A
```

---

### Modified Request (Accessing User B Data)

```http id="r9x4zt"
GET /api/user/profile?id=124 HTTP/1.1
Authorization: Bearer TOKEN_A
```

---

## 📌 Result

* Server returns data of User B
* No authorization check implemented

---

## 🎯 Impact

* Unauthorized data access
* Data leakage
* Account takeover (in some cases)

---

## 🛡️ Mitigation

* Implement proper authorization checks
* Use indirect references (UUIDs)
* Validate user access on server-side
* Avoid exposing predictable IDs

---

## 🧰 Tools Used

* Burp Suite (Repeater)
* Browser Developer Tools

---

## 🎯 Conclusion

IDOR vulnerabilities occur due to missing authorization checks and can lead to serious data breaches if not properly handled.


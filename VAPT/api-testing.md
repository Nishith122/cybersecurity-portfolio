# 🔐 API Security Testing – VAPT Approach

## 📌 Objective

Identify security vulnerabilities in APIs such as Broken Access Control, improper authentication, and data exposure.

---

## 🧠 What is API Security Testing?

API security testing focuses on analyzing endpoints to ensure proper authentication, authorization, and data protection.

---

## 🔍 Testing Approach

### 1️⃣ Identify Endpoints

* Capture API requests using Burp Suite
* Explore endpoints via application usage
* Check Swagger / OpenAPI documentation

---

### 2️⃣ Authentication Testing

* Check if endpoints require authentication
* Remove token and test response
* Use invalid or expired tokens

---

### 3️⃣ Authorization Testing (IDOR)

* Use two accounts
* Change user ID / object ID
* Check if unauthorized data is accessible

---

### 4️⃣ Input Validation Testing

* Send unexpected inputs (e.g., scripts, SQL payloads)
* Check for XSS / SQL Injection

---

### 5️⃣ Rate Limiting Testing

* Send multiple requests rapidly
* Check if API blocks or allows brute-force

---

## 🧪 Example Request

```http id="m4n8qp"
GET /api/v1/users HTTP/1.1
Authorization: Bearer <token>
```

---

## 📌 Common Vulnerabilities

* Broken Access Control (IDOR)
* Missing Authentication
* Sensitive Data Exposure
* Rate Limiting Issues

---

## 🎯 Impact

* Data leakage
* Account takeover
* Service abuse

---

## 🛡️ Mitigation

* Enforce authentication and authorization
* Implement rate limiting
* Validate input data
* Use secure tokens

---

## 🧰 Tools Used

* Burp Suite
* Postman
* Browser Developer Tools

---

## 🎯 Conclusion

API security testing is critical as APIs are widely used and often expose sensitive data if not properly secured.


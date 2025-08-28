# 📑 Case Studies – Android Bug Bounty Hunting

## 🐞 Case Study 1: Insecure Data Storage
- **Target:** Banking application
- **Issue:** Credentials stored in plaintext SharedPreferences
- **Impact:** Attacker with device access could extract login data
- **Mitigation:** Use Keystore API and encryption

---

## 🐞 Case Study 2: Improper SSL Pinning
- **Target:** E-commerce app
- **Issue:** Weak SSL pinning bypassed with Frida
- **Impact:** Man-in-the-middle (MITM) attacks possible
- **Mitigation:** Enforce robust SSL pinning and certificate validation

---

## 🐞 Case Study 3: Exported Component Abuse
- **Target:** Messaging application
- **Issue:** Exported activity allowed access without authentication
- **Impact:** Attacker could send messages as another user
- **Mitigation:** Restrict exported components, enforce permission checks

---

## 🐞 Case Study 4: WebView Vulnerability
- **Target:** News app
- **Issue:** WebView with JavaScript enabled loaded untrusted input
- **Impact:** XSS injection and data theft
- **Mitigation:** Sanitize inputs, disable unnecessary WebView features

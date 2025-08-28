## 🌐 MITM Traffic Capture Demo

Steps

- Configure emulator/device to use Burp Suite/mitmproxy.

- Install Burp CA certificate on device.

- Intercept app traffic.

Example Captured Request

```pgsql
POST /login HTTP/1.1
Host: vulnerable-app.com
Content-Type: application/json

{"username":"admin","password":"123456"}
```

Lesson

- Apps must enforce HTTPS with SSL pinning.

- Without it, attackers can intercept and tamper with sensitive data.

## ✅ Summary

- These demos show three common areas of Android bug bounty testing:

APK analysis → reveal misconfigurations and secrets

SQL Injection → insecure database queries

MITM traffic capture → weak/no encryption & pinning

Use them responsibly and always in legal environments.

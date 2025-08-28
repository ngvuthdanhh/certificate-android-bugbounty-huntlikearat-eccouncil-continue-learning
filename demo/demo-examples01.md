# 🧪 Android Bug Bounty Demo Examples

This file contains multiple **demo scenarios** for Android bug bounty hunting, covering APK analysis, SQL injection in mobile apps, and MITM traffic capture.

---

## 🔍 APK Analysis Demo

### Steps
1. **Unpack APK**

```bash
apktool d target-app.apk -o target-app-src
```

2. **Review AndroidManifest.xml**

- Look for exported activities/services

- Check requested permissions

3.  **Look for Hardcoded Secrets**

```bash
grep -r "api_key" target-app-src/
```
4. **Dynamic Testing with Frida**

- Hook methods to bypass root detection or SSL pinning.

## Outcome

APK static + dynamic analysis helps reveal hidden vulnerabilities in app logic.

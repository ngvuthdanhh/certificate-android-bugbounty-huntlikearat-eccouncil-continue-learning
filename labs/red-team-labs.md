# ⚔️ Red Team Labs – Android Bug Bounty Hunting

Hands-on exploitation scenarios for practicing **Android application vulnerabilities**.

---

## 🔍 Lab 1: APK Recon & Manifest Analysis
- Extract APK from device or Play Store mirror
- Decompile using `apktool` or `jadx`
- Analyze `AndroidManifest.xml`:
  - Permissions
  - Exported components
  - Debuggable flag

---

## 🧩 Lab 2: Insecure Data Storage
- Install vulnerable APK
- Inspect shared preferences (`/data/data/<package>/shared_prefs/`)
- Look for stored credentials
- Exploit: Extract sensitive data

---

## 🌐 Lab 3: Insecure Communication
- Intercept app traffic with Burp Suite / mitmproxy
- Identify unencrypted HTTP traffic
- Modify API requests → privilege escalation
- Exploit: Replay / tamper requests

---

## 🕹️ Lab 4: WebView Exploitation
- Identify apps using WebView
- Inject JavaScript payloads
- Access local files through misconfigured WebView
- Exploit: Steal session data

---

## 🛠️ Lab 5: Exported Components Abuse
- Use `adb shell` or Drozer
- Enumerate exported activities/services
- Send crafted intents to trigger hidden functionality
- Exploit: Access restricted features

---

## ⏱️ Lab 6: SSL Pinning Bypass
- Test app with SSL pinning
- Use Frida / Objection to bypass
- Intercept & modify HTTPS traffic
- Exploit: Steal sensitive data via MITM

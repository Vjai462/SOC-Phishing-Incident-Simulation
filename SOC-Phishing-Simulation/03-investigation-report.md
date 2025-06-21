# 🛡️ SOC Analyst Investigation Report
## 📅 Date: 21-07-2025
## 🧑‍💻 Analyst: Vislavath Vijay

---

## 1️⃣ Alert Summary
- **Alert Source:** Microsoft Defender for Office 365
- **Detected by:** Microsoft Sentinel
- **Alert Title:** Suspicious Email Detected - Possible Phishing
- **Severity:** High
- **User Impacted:** jane.doe@acme-corp.com
- **Email Subject:** Urgent: Copyright Violation Report on Your Instagram Account

---

## 2️⃣ Email Analysis

### ✉️ Header Details (from `phishing-email.eml`)
- **From Address:** security@mail-instagram-support.com
- **To Address:** jane.doe@acme-corp.com
- **Message-ID:** <18273645.mail-instagram-support.com>
- **Date Sent:** 21-Jul-2025, 08:45 IST

---

### 🌐 Suspicious Link
- **Extracted URL:**  
  `https://ig-meta-security.support-verify.com`
- **URL is suspicious because:**
  - Uses domain spoofing (`instagram` lookalike)
  - Not an official Meta/Instagram domain
  - Hosted on suspicious `.support-verify.com` domain

---

### 🧠 Threat Type: Phishing Attempt
- The email is attempting to scare the user into clicking a malicious link.
- User might be tricked into entering their credentials on a fake site.

---

## 3️⃣ Analyst Verdict

✅ **Confirmed True Positive (TP)**  
> This is a real phishing email designed to steal Instagram credentials.

---

## 4️⃣ Next Steps (Response Plan)
- [x] Add domain to email security blocklist  
- [x] Check if user clicked the link (via proxy/DNS logs)  
- [x] Scan user endpoint with EDR  
- [x] Notify user and advise password reset (if credentials entered)  
- [x] Create awareness ticket for phishing campaign  
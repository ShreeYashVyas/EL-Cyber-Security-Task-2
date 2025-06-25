
# 📄 Phishing Email Analysis Report

**Tool Used:** Any.Run / Browser-based Email Analyzer  
**Detection Date:** 2025-06-25  
**Analyst:** Shree Yash Vyad

---

## 📌 Email Metadata

| Attribute            | Value                            |
|----------------------|----------------------------------|
| **From Address**     | no-reply@icici.com               |
| **Subject**          | Urgent: Account Verification     |
| **Attachments**      | Yes – HTML file                  |
| **Timestamp**        | [Extracted from the email header] |
| **Reply-To**         | Different domain (Suspicious)    |

---

## 🚩 Detection Summary

| Feature              | Status        |
|----------------------|---------------|
| SPF                  | ❌ Failed     |
| DKIM                 | ❌ Failed     |
| DMARC                | ❌ Failed     |
| IP Reputation        | 🚫 Blacklisted |
| Suspicious Links     | ✅ Present    |
| Obfuscation Scripts  | ✅ Detected   |
| Spoofed Sender       | ✅ Likely     |
| Malware Payload      | ❌ Not Found  |

---

## 🔍 Detailed Observations

1. **Email Header Forgery:** Fails SPF, DKIM, and DMARC – a strong indication of spoofing.
2. **Malicious Link:** Links in the email redirect to a login page mimicking ICICI Bank, intended to steal credentials.
3. **Obfuscated HTML:** The attached HTML file uses JavaScript to auto-fill phishing fields.
4. **Unusual Reply-To Domain:** The reply-to address does not match the sender's domain, which is a red flag.
5. **Blacklisted IP:** The sending IP is found in spam blocklists.

---

## ✅ Conclusion

> The email is classified as a **Phishing Attempt**. It attempts to trick the recipient into entering sensitive information on a spoofed banking site.

---

## 🔐 Recommendations

- Block sender's IP and domain at the mail gateway.
- Educate users to report suspicious emails.
- Regularly update anti-phishing filters and endpoint protection.
- Report the phishing domain to ICICI and local authorities.

---

## 📎 Evidence

- Attached HTML sample
- Network logs of redirection
- Screenshot of phishing landing page

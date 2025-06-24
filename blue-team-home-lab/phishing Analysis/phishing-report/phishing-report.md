# 🛡️ Phishing Analysis Report

This report contains the analysis of phishing samples involving a **malicious PDF file** and a **QR code phishing image**. Each sample was examined using tools like [ANY.RUN](https://any.run), and VirusTotal.

---

## 🧪 Samples Analyzed
| Type  | File Name                                   | Verdict      | Tool    
| PDF   | Contract\_Agreement9458250728.pdf          | 🟥 Malicious | ANY.RUN |
| Image | Screenshot-2025-06-22-185712.png (QR code) | 🟥 Malicious | ANY.RUN |

---

## 📌 Summary of Findings

### 🧾 1. Contract_Agreement PDF

- Pretends to be a contract or agreement to trick users into opening.
- When opened, drops files to Adobe cache folders.
- Connects to external link through Google redirect:  
  `https://marladesellc[.]com`
- Tags: `phishing`, `generated-doc`, `pdf-secudoc`

🔗 [Full IOC details](./iocs/contract-agreement-iocs.txt) 
 
📸 [Screenshot & Report Summary](./screenshots/contract-agreement.png)

---

### 📷 2. QR Code Phishing Image

- Image shows only a QR code and simple text like “Scan to login.”
- Redirects to:  
  `https://login-auth-verify[.]online/mobile`
- Likely used to bypass email link scanners (quishing).

🔗 [Full IOC details](./iocs/qr-code-iocs.txt)  
📸 [Screenshot & Report Summary](./screenshots/qr-code-anyrun-analysis.md)

---

## 📂 Indicators of Compromise (IOCs)

IOCs from both samples are stored in the `iocs/` folder. They include:

- ✅ File hashes (SHA-256, MD5)
- 🌍 URLs and phishing domains
- 📁 Dropped file paths
- 🧾 Metadata from PDF/QR image analysis

You can find them here:
- [`iocs/contract-agreement-ioc.txt`](./iocs/contract-agreement ioc.txt)
- [`iocs/attachment.txt`](./iocs/attachment ioc.txt)

---

## 🛠️ Tools Used

| Tool | Purpose |

| [ANY.RUN](https://any.run)             | Malware & phishing behavior analysis.
| [VirusTotal](https://virustotal.com)   | Scan URLs and hashes.
| [URLScan.io](https://urlscan.io)       | Analyze redirection and behavior.

---

## 🧠 Conclusion

These samples are good examples of how phishing can:
- Use **normal-looking documents and QR codes** to trick users
- **Drop hidden files** or redirect to phishing websites
- Target both desktop and mobile users

🔒 Avoid opening unknown PDFs or scanning unsolicited QR codes.  
Always inspect attachments and links in a **safe environment** like a sandbox.

---

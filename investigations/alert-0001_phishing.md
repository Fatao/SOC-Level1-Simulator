# 🚨 Alert #0001 – Introduction to Phishing

## 📜 Alert Summary
Phishing email delivered to internal employee inbox containing suspicious links mimicking a Microsoft login page.

## 📂 Investigation Actions
- Inspected email headers for suspicious domains
- Extracted link → `http://login-microsoft-auth-reset[.]com`
- Analyzed reputation using VirusTotal and URLscan

## 🔬 Findings
- Domain registered 3 days ago
- Hosted on AWS IP `3.85.101.100`
- No TLS certificate
- Fake Microsoft login page designed to harvest creds

## 🔒 IOCs
| Type       | Value                           | Description             |
|------------|----------------------------------|-------------------------|
| URL        | http://login-microsoft-auth-reset[.]com | Phishing site |
| IP Address | 3.85.101.100                    | Hosting C2 infrastructure |

## 🎯 MITRE Mapping
- **Initial Access:** T1566.001 (Phishing: Spearphishing Link)
- **Credential Access:** T1110.001 (Brute Force - Web Login)

## 🧾 Recommendation
- Block domain at firewall
- Add URL to spam filters
- Initiate password resets for affected user


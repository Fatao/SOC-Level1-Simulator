# 🚨 Alert #8816 – Access to Blacklisted External URL Blocked by Firewall

## 📜 Alert Summary
Firewall blocked an outbound request to a known malicious domain accessed by a host inside the network.

## 📂 Investigation Actions
- Checked firewall logs
- Identified user-agent: Chrome on Windows 10
- Reverse DNS lookup showed domain flagged in threat intelligence feeds

## 🔬 Findings
- Blocked domain: `hxxp://stealer-data-collector[.]ru`
- Associated with infostealer campaigns in 2024
- User may have clicked from suspicious ad or email

## 🔒 IOCs
| Type       | Value                           | Description             |
|------------|----------------------------------|-------------------------|
| URL        | hxxp://stealer-data-collector[.]ru | Blacklisted C2         |
| IP Address | 185.199.108.153                 | Known malicious host    |

## 🎯 MITRE Mapping
- **Command and Control:** T1071.001 (Web Protocols)
- **Exfiltration:** T1041 (Exfiltration over C2 channel)

## 🧾 Recommendation
- Monitor host behavior
- Deep scan device for trojans / infostealers
- Educate user on phishing awareness


# 🚨 Alert #[X] – [Title]

## 🕵️ Summary
Short description of the alert & attack (e.g., Powershell-based malware detected on host X).

## 📜 Logs Analyzed
- Splunk query: `index=sysmon EventCode=1 Powershell`
- PCAP filters: `http.request.method == "POST"`

## 🧠 Analysis
What did you find? What was suspicious?

## 🔒 IOCs Extracted
| Type       | Value                        | Description         |
|------------|------------------------------|---------------------|
| IP Address | 185.10.20.5                  | C2 Server           |
| Hash       | `a1b2c3d4...`               | Malicious EXE hash  |

## 🧠 MITRE ATT&CK
- **Execution:** T1059.001 (PowerShell)
- **Persistence:** T1547.001 (Registry Run Keys)

## 📎 Artifacts
Screenshots, links to PCAPs, or Sigma rule matches.


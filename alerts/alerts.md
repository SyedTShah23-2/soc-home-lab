# SOC Alerts

## Alert 1: Suspicious DNS Beaconing
- Detected by Suricata
- Matched known C2 domain on abuse.ch
- Resolved via DNS logs and Zeek

## Alert 2: Email Phishing Attempt
- Outlook 365 login redirect detected
- Logged by Wazuh agent via Winlogbeat
- Triaged as medium severity, false positive

# Additional Alerts

## Alert 1: Suspicious DNS Beaconing
- **Detected by:** Suricata
- **Source IP:** 192.168.1.100
- **Details:** Repeated DNS TXT queries to known C2 domain
- **Outcome:** Mapped to ATT&CK T1071.002, blocked IP

## Alert 2: Phishing Link Click
- **Detected by:** Zeek HTTP logs
- **User:** jsmith
- **Details:** User clicked on obfuscated redirect link leading to malicious domain
- **Outcome:** User contacted, credentials reset

## Alert 3: PowerShell Download Cradle
- **Detected by:** Wazuh Windows event log rules
- **Details:** PowerShell invoked with hidden base64-encoded payload
- **Outcome:** Payload extracted and flagged as malicious, host isolated

## Alert 4: Credential Dumping Attempt
- **Detected by:** Wazuh + Sigma rule match
- **Details:** Mimikatz signature match from temp directory
- **Outcome:** Memory dump blocked, SOC escalated to IR team

## Alert 5: Ransomware SMB Encryption Detected
- **Detected by:** Suricata
- **Details:** Unusual SMB encryption behavior and file rename patterns
- **Outcome:** Host isolated, backup initiated, incident escalated

## Alert 6: C2 over HTTP Detected
- **Detected by:** Suricata
- **Details:** HTTP POSTs with regular intervals to suspicious IP
- **Outcome:** Firewall rule added, alert tagged in PCAP

## Alert 7: SMB Brute Force Attack
- **Detected by:** Zeek SMB module
- **Details:** Multiple login failures from same host
- **Outcome:** Source reviewed, user account reset, behavior documented

## Alert 8: RDP Scan from External IP
- **Detected by:** Wazuh and Windows Event Log
- **Details:** Series of failed RDP attempts from unknown country
- **Outcome:** IP blacklisted, IOC added to threat list

## Alert 9: Encoded PowerShell Command Execution
- **Detected by:** Wazuh
- **Details:** Base64 encoded PowerShell attempting to download payload
- **Outcome:** Host quarantined, script analyzed, Tier 2 notified

## Alert 10: SMB Access Abuse from Internal Host
- **Detected by:** Zeek
- **Details:** Repeated unauthorized file accesses from internal host
- **Outcome:** Incident documented, permissions audited

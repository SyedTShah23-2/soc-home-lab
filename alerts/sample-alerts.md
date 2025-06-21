# SOC Alerts

## Alert 1: Suspicious DNS Beaconing
- Detected by Suricata
- Matched known C2 domain on abuse.ch
- Resolved via DNS logs and Zeek

## Alert 2: Email Phishing Attempt
- Outlook 365 login redirect detected
- Logged by Wazuh agent via Winlogbeat
- Triaged as medium severity, false positive

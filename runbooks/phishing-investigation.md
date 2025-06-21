# Runbook: Phishing Email Alert

- **Alert:** SURICATA PHISHING-EMAIL
- **Source IP:** 192.168.1.50
- **Destination IP:** 203.0.113.10

## Triage Steps
1. Verified alert in Kibana dashboard
2. Checked sender domain reputation
3. Noted suspicious link with obfuscated redirect
4. Escalated for deeper forensic analysis

## Mitre ATT&CK Mapping
- T1566.001 – Spearphishing Link

  # phishing-investigation.md

## Alert: SURICATA PHISHING-EMAIL
- **Timestamp:** 2025-06-21T14:32:10Z
- **Source IP:** 192.168.1.50
- **Destination IP:** 203.0.113.10

### Steps:
1. Reviewed Suricata signature and metadata
2. Cross-referenced with Threat Intel feed (abuse.ch)
3. **Result:** Confirmed phishing domain, escalated to Tier 2
4. Documented incident in ConnectWise ticket #1234

**Mitre ATT&CK techniques:** T1566 (Phishing)



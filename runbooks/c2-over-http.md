## Alert: SURICATA MALWARE-CNC-HTTP
- **Timestamp:** 2025-06-22T18:20:35Z
- **Source IP:** 192.168.1.103
- **Destination IP:** 192.0.2.22

### Steps:
1. Identified outbound HTTP POSTs to untrusted IP every 60 seconds
2. Reviewed payloads with base64-encoded beacon data
3. Confirmed known C2 signature match, blocked at firewall
4. Documented and tagged PCAP for future review

**Mitre ATT&CK techniques:** T1071.001 (Application Layer Protocol - Web)

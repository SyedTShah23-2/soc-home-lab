## Alert: SURICATA RANSOMWARE-ACTIVITY
- **Timestamp:** 2025-06-22T17:12:53Z
- **Source IP:** 192.168.1.77
- **Destination IP:** 198.51.100.90

### Steps:
1. Suricata flagged encryption-related traffic over SMB
2. Confirmed rapid file renames and extension changes via Zeek logs
3. Blocked host from network; initiated backup restoration
4. Opened incident ticket and alerted management

**Mitre ATT&CK techniques:** T1486 (Data Encrypted for Impact)

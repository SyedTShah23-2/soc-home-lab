## Alert: WAZUH: RDP Enumeration Attempt
- **Timestamp:** 2025-06-22T19:03:41Z
- **Source IP:** 203.0.113.24
- **Destination IP:** 192.168.1.72

### Steps:
1. Alert triggered from excessive failed RDP attempts in short timeframe
2. GeoIP lookup indicated external IP from known threat actor region
3. Blocked IP via perimeter firewall and created IOC alert
4. Added to threat list and scheduled for continuous monitoring

**Mitre ATT&CK techniques:** T1021.001 (Remote Services: RDP)

## Alert: WAZUH: Encoded Command Execution
- **Timestamp:** 2025-06-22T19:30:14Z
- **Host:** WIN-LAB02

### Steps:
1. Wazuh flagged obfuscated PowerShell with long base64 string
2. Decoded payload revealed attempt to download secondary payload
3. Stopped process and captured hash for sandbox analysis
4. Quarantined host and alerted Tier 2 for follow-up

**Mitre ATT&CK techniques:** T1059.001 (Command and Scripting Interpreter: PowerShell)

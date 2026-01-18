Incident Report: Brute Force Login Attempt

Incident Summary
  Multiple failed authentication attempts were detected against a Windows system from a single external IP address within a short time window. The activity was investigated and confirmed as a brute-force login attempt.

Detection Source
  SIEM Platform: Splunk / ELK
  Log Source: Windows Security Event Logs

MITRE ATT&CK Mapping
  Tactic: Initial Access
  Technique: T1110 – Brute Force

Alert Description
  The SIEM generated an alert due to a high volume of failed login attempts targeting multiple user accounts over a short period of time.

Evidence Observed
  Windows Event ID 4625 (Failed Logon)
  Repeated login attempts from a single source IP
  Targeted accounts included administrative and standard user accounts
  No successful authentication detected (Event ID 4624)

Investigation Steps
  1. Reviewed failed authentication events in the SIEM
  2. Correlated source IP activity across multiple login attempts
  3. Checked for any successful logins following the failed attempts
  4. Verified IP reputation and geolocation
  5. Confirmed no account compromise occurred

Impact Assessment
  No successful authentication was detected. The activity was classified as a brute-force login attempt with no impact on system integrity.

Response and Mitigation
  Source IP was blocked at the firewall
  Account lockout policy was reviewed
  Incident was documented and escalated according to procedure

Outcome
  The brute-force attempt was successfully detected and contained with no system compromise.


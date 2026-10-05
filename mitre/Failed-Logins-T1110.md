# Failed Windows Logins — MITRE ATT&CK Mapping

## Detection
Failed Windows Login Attempts

## Log Source
Windows Security Event Log

## Event ID
4625 — An account failed to log on

## SIEM
Splunk Enterprise

## MITRE ATT&CK
- Technique ID: T1110
- Technique: Brute Force

## Detection Logic
The detection monitors Windows Security Event ID 4625
and counts failed authentication attempts by username.

## Controlled Lab Test
A controlled failed authentication attempt was generated
using the test account:

FakeSOCUser

The failed login was successfully captured by Windows
Security logs and indexed in Splunk.

## Investigation
Relevant fields include:

- TargetUserName
- IpAddress
- WorkstationName
- LogonType
- Status

## Assessment
A single failed login is not sufficient evidence of brute force.
Repeated failures against an account or from a source may
indicate brute-force activity and require further investigation.

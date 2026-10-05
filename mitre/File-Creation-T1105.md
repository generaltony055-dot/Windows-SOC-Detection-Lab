# File Creation Monitoring — MITRE ATT&CK Mapping

## Detection
File Creation Monitoring

## Log Source
Sysmon Event ID 11 — FileCreate

## SIEM
Splunk Enterprise

## Detection Logic
The detection monitors file creation events in user-writable
locations and identifies the process and user responsible
for creating the file.

## Observed Activity
The lab captured PowerShell-created temporary files under:

C:\Users\Sahil\AppData\Local\Temp\

Example:

__PSScriptPolicyTest_*.ps1

## Investigation
Relevant fields include:

- TargetFilename
- Image
- User

## Assessment
The observed PowerShell temporary files appeared consistent
with normal PowerShell activity. File creation alone does not
establish malicious behavior and requires additional context.

## MITRE ATT&CK
File creation by itself does not map cleanly to a single
technique based on the evidence collected in this lab.
Additional context would be required before assigning a
specific ATT&CK technique.

## Result
Sysmon Event ID 11 successfully captured and indexed the
file creation activity in Splunk.

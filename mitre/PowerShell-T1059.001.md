# PowerShell Detection — MITRE ATT&CK Mapping

## Detection
PowerShell Process Execution

## Log Source
Sysmon Event ID 1 — Process Creation

## SIEM
Splunk Enterprise

## MITRE ATT&CK
- Technique ID: T1059.001
- Technique: Command and Scripting Interpreter: PowerShell

## Detection Logic
The detection monitors Sysmon process creation events for
Windows PowerShell execution and examines the command line.

## Controlled Lab Test
A controlled PowerShell process was executed:

Start-Process powershell.exe -ArgumentList '-NoProfile -Command "Write-Output SOC_TEST_123"'

The activity was successfully captured by Sysmon and indexed in Splunk.

## Result
The PowerShell execution was detected successfully.

## Assessment
The test activity was benign and performed for security monitoring
validation. PowerShell execution alone does not indicate malicious activity.

## Evidence
- Sysmon Event ID 1
- Process: powershell.exe
- Command line containing SOC_TEST_123
- Splunk detection result

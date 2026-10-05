# Process Creation — MITRE ATT&CK Mapping

## Detection
Process Creation Investigation

## Log Source
Sysmon Event ID 1 — Process Creation

## SIEM
Splunk Enterprise

## MITRE ATT&CK
- Technique ID: T1059.003
- Technique: Command and Scripting Interpreter: Windows Command Shell

## Detection Logic
The detection monitors Sysmon process creation events and
examines the process image, parent process, user, and command line.

## Controlled Lab Test
A controlled Windows command shell was executed:

Start-Process "C:\Windows\System32\cmd.exe" -ArgumentList "/c echo SOC_PROCESS_TEST"

The activity was successfully captured by Sysmon and indexed in Splunk.

## Evidence
- Process: cmd.exe
- Parent Process: powershell.exe
- Command line containing SOC_PROCESS_TEST
- Sysmon Event ID 1

## Assessment
The activity was intentionally generated for laboratory testing.
The presence of cmd.exe alone does not indicate malicious activity.
Additional context such as the parent process, user, command line,
and execution location should be investigated.

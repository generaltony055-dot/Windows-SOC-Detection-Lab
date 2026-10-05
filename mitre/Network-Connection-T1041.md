# Network Connection Monitoring — MITRE ATT&CK Mapping

## Detection
Network Connection Monitoring

## Log Source
Sysmon Event ID 3 — Network Connection

## SIEM
Splunk Enterprise

## Detection Logic
The detection monitors outbound network connections and
examines the process, source IP, destination IP, destination
port, and protocol.

## Observed Activity
The lab captured outbound connections from:

TrueViewManager.exe

Example traffic included external destinations over
TCP/443 and UDP/443.

## Investigation
Relevant fields include:

- Image
- SourceIp
- DestinationIp
- DestinationPort
- Protocol

## Assessment
The observed network connections were investigated in the
context of the executable and its other telemetry. Network
connections alone do not establish malicious activity.

## MITRE ATT&CK
The collected evidence does not by itself establish a specific
ATT&CK technique.

T1041 — Exfiltration Over C2 Channel should only be assigned
when there is evidence of data exfiltration over a command-and-
control channel. That evidence was not established in this lab.

## Result
Sysmon Event ID 3 successfully captured and indexed network
connection activity in Splunk.


Splunk · SPL · MITRE ATT&amp;CK
# SOC Detection Lab

A home lab simulating real SOC alert triage using Splunk Free.
Includes 5 detection rules mapped to MITRE ATT&CK techniques.

## What this lab does
- Ingests Windows Event Logs into Splunk
- Detects brute force, encoded PowerShell, new services, log clearing
- Produces dashboards showing alert trends

## Setup
```bash
# 1. Install Splunk Free (splunk.com/en_us/download)
# 2. Start Splunk
./splunk start

# 3. Ingest sample logs
./splunk add monitor /var/log/windows_events/ -index windows
```

## Detection rules included
| Rule | MITRE TTP | Event ID |
|------|-----------|----------|
| Brute force login | T1110 | 4625 |
| Encoded PowerShell | T1059.001 | 4688 |
| New service installed | T1543.003 | 7045 |
| Log clearing | T1070.001 | 1102 |
| Admin account created | T1136.001 | 4720 |

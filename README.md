# Mini SOC Lab: Attack Simulation & Detection

## Objective
To simulate a brute-force attack and detect it using log analysis and SIEM (Splunk), replicating a real SOC workflow.

---

## Tools Used
- Splunk Enterprise (SIEM)
- Windows Event Viewer
- Command Prompt

---

## Project Workflow

### 1. Attack Simulation
- Generated multiple failed login attempts using `runas`
- Simulated brute-force attack behavior

### 2. Log Collection
- Captured Windows Security logs (Event ID 4625)
- Exported and extracted relevant log data

### 3. SIEM Analysis
- Uploaded logs into Splunk
- Performed searches to identify failed login activity

### 4. Threat Detection
- Created detection query for brute-force behavior:
index=main 4625
| stats count by user, src_ip
| where count > 5

---

## Key Findings
- Multiple failed login attempts detected
- Repeated login failures from the same user/IP
- Pattern consistent with brute-force attack

---

## Skills Demonstrated
- Log analysis
- SIEM usage (Splunk)
- Threat detection
- Incident investigation
- SOC workflow simulation

---

## Conclusion
This project demonstrates the ability to simulate attacks, analyze logs, and detect threats using SIEM tools, reflecting real-world SOC analyst responsibilities.

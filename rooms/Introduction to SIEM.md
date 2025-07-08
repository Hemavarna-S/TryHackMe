# Introduction to SIEM

##  What is SIEM?
**Security Information and Event Management (SIEM)**  
A tool that collects data from various endpoints and network devices, then stores the logs in a centralized location for analysis and monitoring.

---

##  Network Visibility Through SIEM

![SIEM visibility diagram](https://github.com/user-attachments/assets/0d7fcad2-095e-4bcb-8303-8c20f7211dff)

###  Sysmon
**Sysmon** (System Monitor) is a Windows system service and device driver developed by Microsoft that logs detailed system events and helps in threat detection.

###  Host-Centric Log Sources
Logs generated directly on endpoints or hosts:
- Examples: **Windows Event Logs**, **Sysmon**

###  Network-Centric Log Sources
Logs produced when hosts interact over networks:
- Examples: **SSH**, **VPN**, **HTTP/HTTPS**, **FTP**

---

##  Importance of SIEM

- Modern networks generate hundreds of events per second across endpoints, servers, and infrastructure.
- Manual log analysis is impractical and inefficient—especially during security incidents.
- SIEM tools help detect threats in real-time.
  - Examples: **Splunk**, **Elastic SIEM**

---

##  Log Sources and Log Ingestion

###  Windows Machines
Use **Event Viewer** to inspect logs such as:
- Application logs
- Security logs
- System logs

###  Linux Workstations
Linux stores system logs in specific files:
- `/var/log/httpd` – HTTP request, response & error logs
- `/var/log/cron` – Cron job activity
- `/var/log/auth.log` or `/var/log/secure` – Authentication logs
- `/var/log/kern.log` – Kernel-related events

> **Cron Jobs**: Scheduled tasks that automatically execute scripts or commands at defined times.

###  Web Server Logs
- Apache stores logs in: `/var/log/apache` or `/var/log/httpd`

---

##  Log Investigation Techniques

![Log collection methods](https://github.com/user-attachments/assets/b8d8fa55-5192-4624-88e2-5a0c36267677)

- **Agent / Forwarder**: Lightweight tools (e.g., Splunk Forwarder) collect logs from endpoints.
- **Syslog**: Standard protocol to push real-time data from servers and devices to a centralized SIEM.
- **Manual Upload**: Offline data (CSV, JSON, etc.) can be uploaded for analysis.
- **Port Forwarding**: SIEM can be configured to listen on specific ports for incoming log streams from remote systems.

---
##  Log Investigation Techniques
It acts like the brain of the Security Operations Center (SOC)
###  SIEM Capabilities
* Connects dot of different events
* Cover both host-centric and network centric
* Triage Threats quickly and take action
* proactively search for hidden threats
###  SOC Analyst Responsibilities
* Monitor and Investigate
* Identify False positive
* Adjust Detection parameter and reduce noise and improve accuracy
* Generate report audit and meet regulatory standards
  
---
## Analyse Logs and Alerts
### SIEM Rule Execution & Detection
SIEM tools analyze these logs using predefined correlation rules. These rules are logical expressions that define patterns associated with suspicious behavior. If a log matches a rule’s conditions, an alert is triggered.
#### Example flow:

* SIEM detects logs showing failed login attempts.

* If a threshold (e.g., 5 failures in 10 seconds) is met, a rule is triggered.

* This initiates alert investigation by a SOC analyst.
  ### Dashboard
 * key alerts that need investigation
 * OS/ SIEM updates / warnings
 * brute force attempts
 * total logs pulled during a timeframe
 * summary of fired correlaton rules
 * DNS activity and possible threat
   ### Correlation Rules
   * 5 failure in 10 sec -> Raise allert
   * Success after failures
   * Alert on USB insertion
   * Outbound traffic > 25 MB -> Alert
   *  WinEventLog + EventID 104 ( log Clearing)
   *  WinEventLog + EventID 4688 + whoami (privilage recon)
     ![image](https://github.com/user-attachments/assets/d25d284c-0cc9-416e-9148-4b95770fd3e6)
## Lab Work
![image](https://github.com/user-attachments/assets/50979c6a-e964-4dea-a422-143aaa2038a8)
Answers
![image](https://github.com/user-attachments/assets/4feff115-7c47-412b-b269-a3b504358205)








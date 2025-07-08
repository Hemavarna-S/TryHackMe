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


https://mermaid.js.org/syntax/gantt.html


```mermaid
gantt 
	title Daily Schedule
	dateFormat HH:mm
	axisFormat %H:%M
	Day Start : milestone, m1, 07:00, 2m
	Email and coffee: 07:10,30m
	Typing Practice - Sit at folding table on divan, increase this time as it becomes more comfortable.: 07:40,15m
	Breakfast: 08:00,30m 
	Python Lesson: 08:30,30m
	Linux Lesson: 09:00, 30m
	Jobsearch: 09:30, 30m
	Revision: 10:00, 30m
	Get Ready for work: 10:30, 30m
	Work: 11:00, 6h
	Drive home: 17:00, 30m
	Dinner: 17:30, 1h
	relax - play a game/watch a movie or some TV/guitar practice: 18:30, 3h
	wind down - tea and a book: 21:30, 30m
	Day End : milestone, m2, 22:00, 4m
	


```

```mermaid
flowchart TD
  %% Retail to Cyber Security — label-safe (no edge labels)

  start([Start: Retail employee])
  A1["Self-assessment → strengths, time, budget"]
  A2{"Choose your first target role"}

  start --> A1 --> A2

  %% Phase 1 — Foundations
  F1["IT basics: OS, files/permissions, users, CLI"]
  F2["Networking: IP, DNS, DHCP, routing, ports"]
  F3["Home lab: 1×Windows + 1×Linux (VMs or old PC)"]
  F4["Scripting: Python or PowerShell (30–60 min daily)"]
  F5["Git + GitHub (version control)"]
  A2 --> F1 --> F2 --> F3 --> F4 --> F5

  %% Cert decision
  C1{"Need entry certs to unlock interviews?"}
  F5 --> C1
  Cyes["Earn A+ → Net+ → Sec+ (or equivalent)"]
  Cno["Skip/mark done"]
  C1 -->|Yes| Cyes --> P2a
  C1 -->|No| Cno --> P2a

  %% Specialization choices (fan-out nodes)
  O0["Helpdesk / IT Support"]
  O1["SOC Analyst (Blue Team)"]
  O2["GRC / Risk"]
  O3["Penetration Testing"]
  O4["Cloud Security"]
  A2 --> O0
  A2 --> O1
  A2 --> O2
  A2 --> O3
  A2 --> O4

  %% Track: Helpdesk / IT Support
  T0["Learn AD, M365/Google Workspace, ticketing"]
  T0a["Endpoint mgmt (Intune/MDM), imaging, backups"]
  T0b["Troubleshooting playbooks + customer comms"]
  O0 --> T0 --> T0a --> T0b --> P2a

  %% Track: SOC / Blue Team
  T1["Logs 101: syslog, Windows Events, NetFlow"]
  T1a["SIEM lab: Wazuh/ELK/Splunk; build 5 detections"]
  T1b["Network sec: Suricata/Snort; PCAP with Wireshark"]
  T1c["Hands-on labs (daily) + notes"]
  O1 --> T1 --> T1a --> T1b --> T1c --> P2a

  %% Track: GRC / Risk
  T2["Security principles & policy basics"]
  T2a["Risk register practice; vendor risk questionnaire"]
  T2b["Map controls to a framework (ISO/NIST/Essential 8)"]
  T2c["Write 3 sample policies + audit checklist"]
  O2 --> T2 --> T2a --> T2b --> T2c --> P2a

  %% Track: Penetration Testing
  T3["Web basics: HTTP, auth, SQL; Linux/Bash"]
  T3a["Tools: Burp, Nmap, Metasploit; OWASP Top 10"]
  T3b["CTFs/labs + 2 full sample reports"]
  O3 --> T3 --> T3a --> T3b --> P2a

  %% Track: Cloud Security
  T4["Cloud fundamentals (AWS/Azure/GCP) + IAM"]
  T4a["Secure demo app: logging, guardrails, alarms"]
  T4b["IaC basics (Terraform) + least privilege"]
  O4 --> T4 --> T4a --> T4b --> P2a

  %% Phase 2 — Portfolio & Proof
  P2a["Document 3–5 projects as case studies"]
  P2b["Public notes/blog; tidy GitHub READMEs"]
  P2c["One-page resume aligned to target role"]
  P2d["LinkedIn tuned; list 20 target companies"]
  P2a --> P2b --> P2c --> P2d --> P3

  %% Phase 3 — Job Search Sprints
  P3["Run 4–8 week application sprints"]
  J1["Warm intros: meetups/alumni/recruiters (weekly)"]
  J2["Apply 10–15/wk; tailor bullets to JD"]
  J3["Interview prep: STAR stories + lab demos"]
  J4["Track pipeline, iterate weekly on feedback"]
  P3 --> J1 --> J2 --> J3 --> J4 --> P4

  %% Phase 4 — First Role → Security Role
  P4["Land entry role (helpdesk/analyst/intern)"]
  R2["Automate a pain point; measure impact"]
  R3["Ask for security-adjacent tasks (EDR, patching, logging)"]
  R4["Update portfolio with on-the-job wins"]
  P4 --> R2 --> R3 --> R4 --> P5

  %% Phase 5 — Specialize & Advance
  P5["Pick path: Blue/Red/Purple/GRC/Cloud/AppSec"]
  S5a["Advanced cert or project tied to path"]
  S5b["Mentor others; present at meetup or blog"]
  goal([Cyber security professional in chosen track])
  P5 --> S5a --> S5b --> goal
```




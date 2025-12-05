# 🔐 Attack–Defense Cybersecurity Simulation
### **End-to-End Enterprise Attack Chain | Red Team vs Blue Team | SOC & IR Project**

This project is a full adversary emulation and incident response simulation completed inside an enterprise-style virtual lab.  
It demonstrates my ability to perform **offensive security**, **defensive detection**, and **SOC-style incident analysis** in a real-world multi-host environment.

---

## 🚀 Project Summary

A vulnerable enterprise network was deployed and attacked using real attacker techniques.  
The blue team then detected, analyzed, and responded using Wazuh SIEM + Snort IDS.

This project covers:

- ✔ Adversary simulation  
- ✔ Web exploitation & privilege escalation  
- ✔ Windows lateral movement  
- ✔ Active Directory compromise  
- ✔ SIEM-based detection  
- ✔ Full incident response workflow  
- ✔ MITRE ATT&CK mapping  

---

## 🏗️ Lab Architecture


📁 *Detailed diagrams located in `/Network-Architecture`*

---

# 🔴 Red Team: Attack Path (Kill Chain)

### **1. Reconnaissance — T1595**
- Nmap scan → discovered SSH & HTTP

### **2. Enumeration**
- Apache default page exposed  
- Gobuster → `/DVWA` directory found

### **3. Web Exploitation — T1190**
- Default DVWA credentials  
- Upload restriction bypass with BurpSuite  
- Reverse shell uploaded → meterpreter session

### **4. Linux Privilege Escalation — T1548**
- Misconfigured sudo allowed python as root  
- Full root compromise

### **5. Credential Attacks — T1110**
- Hydra brute-force → valid users: `spidey`, `antman`

### **6. Lateral Movement to Windows — T1021**
- Cracked RDP credentials for `BWidow`  
- RDP access obtained

### **7. AD Enumeration — T1069**
- SharpHound → identified high-value user: `svc_backup`

### **8. Kerberoasting — T1558**
- Kerberos hash dumped & cracked  
- Domain admin credentials revealed

### **9. Domain Compromise**
- Evil-WinRM → full Domain Controller access  

📸 Screenshots in: `/Screenshots/Red_Team`

---

# 🔵 Blue Team: Detection & Response

### **1. Visibility Setup**
- Wazuh agents installed  
- Snort IDS configured  
- Centralized log collection enabled

### **2. Key Detections**
| Attack Stage | Detection Source |
|-------------|------------------|
| Nmap scan | Snort |
| Gobuster | Wazuh (Apache logs) |
| Malicious file upload | Wazuh |
| SSH brute force | Wazuh |
| Suspicious sudo activity | Wazuh |
| Unauthorized RDP | Windows logs |
| SharpHound | Windows logs |
| Kerberoasting | Wazuh |
| Domain admin login | Wazuh |

### **3. Containment & Eradication**
- Isolated web server  
- Removed DVWA  
- Hardened Apache configuration  
- Forced key-based SSH  
- GPO password policy enforced  
- Removed unauthorized admins

### **4. Recovery**
- Verified clean logs  
- Restored normal operations  

📸 Screenshots in: `/Screenshots/Blue_Team`

---

# 🛠 Hardening Measures Applied

### 🔐 Network Hardening
- Blocked ICMP externally  
- Strict firewall rules on pfSense  

### 🛡 Linux Hardening
- Disabled directory listing  
- Removed insecure services  
- Enforced secure SSH configuration  

### 🪟 Windows Hardening
- Strong password policies  
- Privilege cleanup  
- Service account hardening  

---

# 📄 Documentation

Located in `/Documentation`:

- **Final Project Report (PDF)**  
- **Presentation Deck**  
- **MITRE Mapping**  

---

# 🎯 Key Skills Demonstrated

- SIEM detection engineering (Wazuh)
- Network IDS analysis (Snort)
- Malware / web exploitation analysis
- Linux & Windows log analysis
- MITRE ATT&CK mapping
- Incident response workflow
- Privilege escalation analysis
- Active Directory attack & detection
- Report writing & threat summarization

---

# 👤 Team Members
- Jay Patel  
- Vansh Patel  
- Chahakkumar Rupavatiya  
- Madhav  
- Harjas  

---
✔ Repository **tags & keywords**  
✔ A ready-to-post **LinkedIn announcement**

Just tell me: **“Make it more visual”** or **“Make it shorter”** or **“Add badges”**.

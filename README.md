# 🛡️ Penetration Testing Report – Mayo Industries  
**Simulated Lab Assessment (Metasploitable & DVWA)**  

**Test Duration:** 01 Sep 2025 – 03 Oct 2025  
**Environment:** 192.168.56.0/24 (Isolated Lab Network)  
**Teams Involved:** Red Team • Blue Team • Purple Team  

---

## 📘 Overview  
This repository contains the complete penetration-testing report for **Mayo Industries’ simulated lab environment**. The assessment was performed on **Metasploitable2** and **DVWA** systems to identify vulnerabilities, exploit weaknesses, and recommend effective defensive strategies.

All testing was fully authorized and conducted within an **isolated lab network**.

---

## 📂 Contents  
- Full penetration testing report  
- Tool usage examples  
- Proof-of-Concept exploitation steps  
- Vulnerability summaries  
- Business impact analysis  
- Blue Team recommendations  
- Purple Team validation overview  

---

## 🔍 Scope of Testing  

### **Targets**  
- Metasploitable2 (Linux)  
- DVWA Web Application  
- 192.168.56.0/24 internal lab network  

### **In-Scope Areas**  
- ✔ Network scanning  
- ✔ Service enumeration  
- ✔ Weak authentication testing  
- ✔ Web application testing (SQLi, RCE)  
- ✔ Password cracking  
- ✔ Exploitation & post-exploitation  

### **Out-of-Scope**  
- ✘ Social engineering  
- ✘ Physical security  
- ✘ External real-world networks  

---

## 🧰 Tools Used  

| Category           | Tools |
|-------------------|-------|
| Reconnaissance    | theHarvester, Dmitry, Nslookup, Ping |
| Scanning          | Nmap, Angry IP Scanner |
| Web Enumeration   | Dirb, Nikto |
| Exploitation      | Metasploit Framework |
| Password Attacks  | Hydra, John the Ripper |
| Remote Access     | Telnet, SSH, VNC |

---

## ⚠️ Key Findings (Summary)

| Vulnerability                 | Risk      | Impact                                |
|------------------------------|-----------|----------------------------------------|
| vsftpd 2.3.4 Backdoor        | Critical  | Remote root access                     |
| Telnet with weak credentials | High      | Credential theft & lateral movement    |
| VNC with weak/no auth        | High      | Full GUI takeover                      |
| SQL Injection (DVWA)         | High      | Data leakage & auth bypass             |
| Command Injection (DVWA)     | Critical  | Full remote code execution             |
| Weak Linux passwords         | High      | Escalation & account compromise        |

---

## 🚨 Business Impact  
- Full system compromise  
- Data theft (credentials, internal info)  
- Lateral movement across the network  
- Reputation and compliance risks  
- Operational downtime  

---

## 🔧 Blue Team Recommendations  
- ✔ Patch outdated services (vsftpd, Telnet, Apache, SSH)  
- ✔ Disable insecure protocols (Telnet, FTP)  
- ✔ Enforce strong password policies  
- ✔ Implement MFA for critical systems  
- ✔ Harden VNC (password + encryption)  
- ✔ Apply network segmentation  
- ✔ Deploy IDS/IPS and SIEM monitoring  
- ✔ Improve logging for authentication & web traffic  

---

## 🟣 Purple Team Role  
- Validate Blue Team mitigations  
- Test defenses against Red Team attacks  
- Verify SIEM detections and alert accuracy  
- Provide lessons learned and improvement steps  

---

## 📄 How to Use This Repository  
- Review the full penetration testing report (PDF/DOC).  
- Refer to PoC commands to replicate attack steps.  
- Apply fixes based on Blue Team recommendations.  
- Use Purple Team notes to test defensive improvements.  

---

## 🏁 Conclusion  
This penetration test highlights the importance of **patching**, **secure authentication**, **network segmentation**, and **proper monitoring**. The findings demonstrate how quickly an attacker can gain complete control when outdated services and weak access controls are present.


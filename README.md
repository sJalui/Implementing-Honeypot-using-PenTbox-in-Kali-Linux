# 🚀 **Implementation of Honeypot using PenTBox in Kali Linux**  
---  
## 🔐 **Information Security IA_1**  
---  
### 👥 **Group Members:**  
- Shubh Jalui - 16010122072 
- Manas Mapuskar - 16010122 
- Ninad Marathe - 16010122105
---  
## 🛠 **Introduction**  
### 🐧 **Kali Linux:**  
Kali Linux is a Debian-based Linux distribution designed for **penetration testing** and **digital forensics**. Maintained by **Offensive Security**, it comes preloaded with **600+ security tools**, including **Nmap, Wireshark, John the Ripper, SQLmap, Burp Suite, and OWASP ZAP**. It was developed by **Mati Aharoni and Devon Kearns** by rewriting **BackTrack**, a previous security-focused distribution. The name "Kali" is inspired by the Hindu deity.  
  
### 🎭 **Honeypot:**  
A **honeypot** is a decoy system designed to **attract and analyze cyber threats** by mimicking a legitimate target. It helps security researchers study different **attack methodologies** and can be classified into:  
- **Low-Interaction Honeypots** – Simulate limited services to log basic attack data with minimal risk.  
- **High-Interaction Honeypots** – Provide a full-fledged system to track sophisticated attacker behavior.  
While honeypots are a powerful tool for **cyber threat intelligence**, poorly configured ones can be exploited by **attackers for misinformation** or launching counterattacks.  
  
### 🔍 **PenTBox:**  
**PenTBox** is a **Ruby-based security suite** used in penetration testing. It includes various functionalities such as **hash cracking, DNS enumeration, stress testing, and an easy-to-configure honeypot**. It supports:  
- **Auto/Manual Configuration** – Quick setup for beginners and advanced options for experienced users.  
- **Port Monitoring** – Captures logs of unauthorized access attempts.  
  
---  
## 📜 **Stepwise Implementation**  
### 🖥 **1. Setting up the Virtual Environment**  
🔹 Created two Virtual Machines on **Oracle VirtualBox**:  
✅ **Kali Linux (Honeypot Host)** – Running PenTBox for monitoring.  
✅ **Windows OS (Simulated Target)** – Used for generating attack traffic.  
🔹 Configured **Bridged Network Adapter** to allow realistic interaction between VMs.  
  
### ⚙ **2. Installing and Running PenTBox**  
🔸 Downloaded **PenTBox** from GitHub using the command:  
```bash  
git clone <https://github.com/sJalui/Implementing-Honeypot-using-PenTbox-in-Kali-Linux>  
```  
🔸 Navigated into the **PenTBox directory**:  
```bash  
cd pentbox  
```  
🔸 Extracted the compressed file:  
```bash  
tar -xzvf pentbox.tar.gz  
```  
🔸 Entered the **Pentbox-1.8 directory** and listed files:  
```bash  
cd pentbox-1.8 && ls  
```  
🔸 Ran the **PenTBox script**:  
```bash  
./pentbox.rb  
```  
  
### 🛡 **3. Deploying the Honeypot**  
🟢 Selected **Network Tools** by typing `2` and pressing **Enter**.  
🟢 Chose the **Honeypot option** by typing `3`.  
🟢 Opted for **Auto Configuration (Option 1)** for quick deployment.  
🟢 The honeypot was successfully deployed on **port 80**, simulating a **web service**.  
  
### 🏹 **4. Attack Simulation and Testing**  
🛠 Simulated attacks using **Nmap** from the Windows VM:  
```bash  
nmap -p 80 <honeypot_ip>  
```  
🛠 Tested **brute-force attacks** using Hydra.  
🛠 Observed logs capturing **IP addresses, timestamps, and attack attempts**.  
  
### 📊 **5. Results and Analysis**  
📌 **Port scanning attempts** were detected and logged.  
📌 **Brute-force attempts** were captured, including repeated login failures.  
📌 **Attack patterns** were analyzed for security insights.  
  
---  
## 🚧 **Limitations**  
❌ **Limited Interaction:** Only logs basic attack data without engaging attackers.  
❌ **False Positives:** Some legitimate network activity can trigger alerts.  
❌ **Manual Log Review:** Lacks automation for real-time threat correlation.  
❌ **Restricted Attack Surface:** Only monitors specific ports, missing multi-vector attacks.  
❌ **Detection by Attackers:** Advanced hackers may identify and avoid interacting with the honeypot.  
  
---  
## 🎯 **Applications of Honeypots**  
✅ **Intrusion Detection & Monitoring** – Identifies unauthorized access attempts.  
✅ **Cyber Threat Intelligence** – Analyzes malware propagation and attack strategies.  
✅ **Network Security Enhancement** – Helps in discovering vulnerabilities.  
✅ **Forensics & Incident Response** – Provides valuable data for post-attack investigations.  
✅ **Deception Technology** – Diverts attackers away from critical systems.  
✅ **Security Training & Education** – Helps train cybersecurity professionals in attack detection.  
  
---  
## 🏆 **Conclusion**  
The successful deployment of a **PenTBox-based honeypot** in a **virtualized network environment** demonstrated its effectiveness in **cyber threat detection**. The honeypot captured **unauthorized access attempts, reconnaissance scans, and brute-force attacks**, providing crucial threat intelligence. While **low-interaction honeypots** are easy to deploy and low-risk, they have **limitations in detailed attacker engagement**. Future enhancements could involve **automated log analysis, IDS integration, and high-interaction honeypots** for deeper forensic insights.  

Honeypots are a vital tool in **proactive cybersecurity defense**, enabling organizations to **detect threats, analyze attack trends, and enhance security posture**. 🛡🔥


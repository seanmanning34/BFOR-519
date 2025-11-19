# BFOR-419/519
Ransomware Response & Recovery  
A Forensic Investigation and Incident Response Simulation

## 1. Project Overview  
Ransomware remains one of the most disruptive cybersecurity threats, often causing data loss, downtime, and costly recovery efforts. This project simulates the **analysis and recovery phases** of a ransomware incident response using publicly available forensic datasets. We examine both the network and disk components of a ransomware event to understand how investigators can identify indicators of compromise (IOCs), reconstruct attack timelines, and evaluate data recovery strategies—without using or executing live malware.

Our project focuses on correlating network-level malicious activity with host-level forensic artifacts to build a unified and realistic incident response workflow.

---

## 2. Project Relevance  
This project is directly related to digital forensics and incident response (DFIR). Ransomware attacks continue to grow in frequency and sophistication, making it essential for analysts to understand how to:

- detect malicious activity through logs and PCAPs  
- examine host artifacts to identify persistence mechanisms  
- build event timelines  
- determine what data can be recovered  

By completing this project, we develop practical skills in DFIR analysis, including network forensics (Wireshark), disk forensics (Autopsy), and timeline analysis (Plaso). These skills are used daily by SOC analysts, IR teams, forensic examiners, and cybersecurity professionals.

---

## 3. Methodology  

### **3.1 Setup & Environment**
All analysis is performed in a **safe, isolated environment**:
- macOS host system  
- VirtualBox VM (offline, no internet access)  
- Dataset copies stored safely (raw data remains read-only)  
- No execution of live malware  

### **3.2 Tools Used**
| Tool | Purpose |
|------|---------|
| **Wireshark** | Analyzing ransomware infection PCAPs, identifying IOCs, DNS queries, and suspicious traffic |
| **Autopsy** | Disk image analysis (file metadata, persistence, user activity) |
| **Plaso/log2timeline** | Creating a unified event timeline from disk artifacts |
| **VirtualBox** | Running an isolated VM environment if needed |
| **Draw.io** | Workflow and architecture diagrams |

### **3.3 Datasets**
We use **public, safe datasets** widely used for DFIR education:

**1. Ransomware Infection PCAP**  
Source: Malware-Traffic-Analysis.net  
Link: https://www.malware-traffic-analysis.net/2019/10/15/index.html  
Dataset: Shade (Troldesh) ransomware infection network capture  
Used for: detecting malicious domains, C2 connections, HTTP requests, and initial infection behavior  

**2. Windows Disk Image**  
Source: Digital Corpora  
Link: https://digitalcorpora.org/corpora/disk-images/  
Dataset: benign Windows disk image  
Used for: modeling disk forensics, examining metadata, persistence, and simulating recovery attempts  

### **3.4 Workflow**

Below is the project workflow:

1. **Collect Datasets**  
   - Download ransomware PCAP  
   - Download Digital Corpora disk image  
   - Verify integrity & store raw data safely  

2. **Network Forensics (Josh)**  
   - Load PCAP in Wireshark  
   - Identify suspicious DNS, domains, IPs  
   - Extract IOCs for correlation  

3. **Disk Forensics (Sean)**  
   - Load disk image in Autopsy  
   - Analyze file metadata & persistence mechanisms  
   - Identify changes resembling ransomware behavior  

4. **Timeline Correlation (Both)**  
   - Use Plaso/log2timeline  
   - Combine network + disk events  
   - Build incident timeline  

5. **Recovery Testing (Sean)**  
   - Simulate file carving  
   - Examine backup-related artifacts  
   - Assess what recovery methods succeed or fail  

6. **Documentation & Presentation (Both)**  
   - Build slides  
   - Write final report  
   - Prepare 10-minute presentation  

**Workflow Diagram Example:**  
_(add this using draw.io later)_

---

## 4. Results (To Be Added as Project Progresses)

As we complete the project, we will add:

### **4.1 Network Findings**
- Screenshots of Wireshark PCAP analysis  
- Suspicious domains, IPs, and requests  
- Indicators of compromise (IOCs) summary  

### **4.2 Disk Findings**
- Autopsy screenshots  
- File metadata tables  
- Persistence artifacts  
- Suspected ransomware behavior reconstruction  

### **4.3 Timeline Findings**
- Plaso-generated CSV timeline  
- Correlation of disk + network events  

### **4.4 Recovery Testing**
- File carving results  
- Recovery success/failure table  
- Lessons learned on what can and cannot be restored  

---

## 5. Conclusion  
This project demonstrates how DFIR analysts can safely reconstruct ransomware events using publicly available datasets. Through network, disk, and timeline analysis, we will show how incident responders identify malicious activity, correlate evidence across systems, and test recovery options. The final output will be a practical playbook for analyzing and responding to ransomware events—without ever using live malware.

---

## 6. Team Members & Responsibilities  
| Member | Responsibilities |
|--------|------------------|
| **Sean Manning** | Disk forensics (Autopsy), recovery testing, final report conclusions |
| **Josh Okanlawon** | Network forensics (Wireshark), dataset collection, slide design |
| **Both** | Workflow design, Plaso timeline analysis, documentation, presentation |

---

## 7. Repository Structure


`.gitignore` will exclude raw dataset files to prevent large uploads.

---

## 8. References  
- Malware Traffic Analysis – Shade/Troldesh Ransomware PCAP  
- Digital Corpora – Disk Images  
- Plaso Documentation  
- Autopsy/Sleuth Kit Documentation  
- Wireshark User Guide  


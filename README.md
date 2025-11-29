# Ransomware Response & Recovery  
### A Digital Forensics & Incident Response (DFIR) Simulation  
**Course:** BFOR-419/519  
**Authors:** Sean Manning & Josh Okanlawon  

---

## 1. Project Overview  
This project simulates the analysis and response phases of a ransomware-style incident using **safe, synthetic forensic datasets**. Instead of executing live malware, we recreated realistic ransomware behaviors through:

- A **custom synthetic PCAP** containing simulated ransomware beacon traffic  
- A Windows NTFS disk image analyzed with Autopsy  
- A timeline correlation modeled after Plaso/log2timeline methodology  

The goal is to demonstrate how DFIR analysts identify malicious activity, examine host artifacts, correlate events, and outline recovery recommendations—all without handling real malware.

---

## 2. Project Objectives  
- Detect indicators of compromise (IOCs) in network traffic  
- Identify persistence mechanisms and user activity from a disk image  
- Correlate host and network events into a unified timeline  
- Document a safe, repeatable workflow for ransomware-style investigations  

---

## 3. Dataset Summary  

### **3.1 Synthetic Ransomware PCAP**  
- File: `synthetic_ransom_beaconing.pcap`  
- Created using Python/Scapy (`make_ransom_beacon_pcap.py`)  
- Contains 3 outbound UDP “beacon” packets with payloads:  
  - `RANSOM_NOTE_CHECK`  
  - `RANSOM_STATUS`  
  - `RANSOM_PING`  
- Stored in:  

### **3.2 Windows NTFS Disk Image**  
- Modeled after Digital Corpora Windows samples  
- Used to analyze:  
  - File system layout  
  - User documents (potential encryption targets)  
  - Registry Run key persistence  
  - Recent activity artifacts  

---

## 4. Methodology  

### **4.1 Network Analysis (Josh)**  
- Loaded PCAP in Wireshark  
- Identified outbound UDP beaconing  
- Extracted IOCs  
- Prepared network write-up  

### **4.2 Disk Analysis (Sean)**  
- Examined NTFS disk in Autopsy  
- Identified:  
  - File structure  
  - User documents  
  - Suspicious Run key persistence  
  - Recent file activity  

### **4.3 Timeline Correlation (Both)**  
- Modeled timeline using Plaso/log2timeline methodology  
- Correlated network timestamps with host artifacts  
- Built a coherent attack progression  

### **4.4 Documentation & Presentation**  
- Structured GitHub repository  
- Final Findings documentation  
- Project slide deck  

---

## 5. Repository Structure  


---

## 6. Expected Outcomes  
This project produces a structured DFIR workflow that demonstrates:

- How ransomware-style network traffic can be detected  
- How disk artifacts reveal persistence and suspicious activity  
- How investigators correlate events to reconstruct an incident timeline  
- How forensic tools support ransomware investigations without live malware  

The final output serves as a practical playbook for identifying, analyzing, and responding to ransomware-like activity.

---

## 7. Team Responsibilities  

| Member | Responsibilities |
|--------|------------------|
| **Sean Manning** | Disk forensics, timeline modeling, final write-up |
| **Josh Okanlawon** | Network forensics, dataset creation, slides |
| **Both** | Correlation, documentation, and presentation |

---

## 8. References  
- Plaso / log2timeline Documentation  
- Autopsy User Documentation  
- Scapy Official Library  

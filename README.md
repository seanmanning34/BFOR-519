# BFOR-519
# Ransomware Response & Recovery

Course project focused on simulating the forensic investigation and incident response (analysis and recovery phases) of a ransomware incident using publicly available datasets.

## Project Overview

- **Title:** Ransomware Response & Recovery: Forensic Investigation and Incident Response Simulation  
- **Team Members:** Sean Manning and [Partner Name]  
- **Due Date:** December 10

## Setup

We will use isolated virtual machines (no internet access) and publicly available datasets rather than executing live malware. Tools we plan to use include:

- **Wireshark** – network traffic inspection (PCAP analysis)
- **Autopsy** – disk-level forensic analysis
- **Plaso/log2timeline** – event timeline reconstruction

Our main focus is on **Windows systems**, as most ransomware targets this platform.

## Data

We will analyze:

- A Shade (Troldesh) ransomware infection PCAP from Malware-Traffic-Analysis.net  
- A benign Windows disk image from Digital Corpora  

From these, we will focus on:

- Network indicators of compromise (domains, IPs, suspicious connections)
- File metadata and persistence artifacts
- Timeline correlations between network activity and host behavior

## Roles

- **Sean:** Disk forensics, recovery testing, and final report conclusions  
- **Josh:** Network forensics, dataset collection, and slide design  

Both team members will collaborate on timeline analysis, documentation, and presentation prep.

## Expected Outcomes

We aim to produce:

- A clear workflow for using network and disk forensics in the **analysis and recovery phases** of ransomware incident response.
- A short “playbook” of best practices for detecting ransomware activity, reconstructing an incident timeline, and evaluating data recovery options—without handling live malware.

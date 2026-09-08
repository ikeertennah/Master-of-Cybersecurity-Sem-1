# MECR1033 – Digital Forensics (Full Course Portfolio)

**Semester:** 1 | **Year:** 2025/2026 | **Instructor:** Assoc. Prof. Ts. Dr. Siti Hajar Othman | **GPA:** 4.00

---

## 🔍 Executive Summary

This repository showcases my comprehensive hands-on experience in **Digital Forensics and Incident Response (DFIR)**. It covers the complete investigative lifecycle—from metadata extraction and system artefact analysis to full-scale breach investigations and court‑ready reporting. Through a combination of structured labs and a capstone project, I have developed the technical proficiency and forensic rigor required to handle real‑world security incidents professionally.

---

## 🎯 Core Learning Objectives

- Master the use of industry‑standard forensic tools (FTK Imager, Autopsy, ExifTool, NirSoft utilities) for evidence acquisition and analysis.
- Extract and interpret **digital artefacts** (metadata, user activity logs, system uptime, browsing history) to reconstruct user behaviour.
- Apply **hash‑based integrity verification** (MD5, SHA‑1) to ensure evidence admissibility.
- Recover deleted files from **unallocated space** to uncover hidden or destroyed evidence.
- Correlate evidence across multiple sources (emails, logs, file systems, browser history) to build irrefutable timelines.
- Document investigations with **Chain of Custody** forms and produce professional, court‑ready reports.

---

## 🛠️ Tools & Technologies

| Category | Tools |
| :--- | :--- |
| **Forensic Imaging & Acquisition** | FTK Imager (E01 image creation, write‑blocking, hash verification) |
| **Platform Analysis** | Autopsy (file system parsing, deleted file recovery, email extraction, report generation) |
| **Metadata Extraction** | ExifTool (EXIF, document metadata, checksum calculation) |
| **User Activity Analysis** | LastActivityView (program execution, file opens, system events) |
| **System Uptime Forensics** | TurnedOnTimesView (startup/shutdown logs, crash analysis, sleep events) |
| **Web Browsing Forensics** | BrowsingHistoryView (aggregated Chrome/Edge/IE history) |
| **Integrity & Validation** | MD5 / SHA‑1 hashing, checksum verification |
| **Data Visualisation** | Microsoft Excel (pivot tables for domain/browser analysis) |
| **Reporting** | HTML export, Chain of Custody forms, court‑ready presentations |

---

## 📚 Key Skills Developed

### 🔐 Forensic Acquisition & Integrity
- Created **forensically sound** bit‑for‑bit images (E01) using FTK Imager with write‑blockers.
- Verified image integrity using **MD5 and SHA‑1** checksums to maintain a provable Chain of Custody.
- Documented evidence handling from collection to final storage, ensuring legal admissibility.

### 🖥️ Windows Artefact Analysis
- **Metadata Forensics (ExifTool):** Extracted authorship, timestamps, software provenance, and checksums from DOCX, PNG, JPEG, PDF, and XLSX files.
- **User Activity Tracking (LastActivityView):** Reconstructed timelines of program executions, file accesses, and system events.
- **System Uptime Analysis (TurnedOnTimesView):** Distinguished between unexpected crashes/system failures and user‑initiated shutdowns; correlated system availability with suspicious activity windows.
- **Web Browsing Forensics (BrowsingHistoryView):** Aggregated history across multiple browsers, applied date/browser filters, and used pivot tables to identify top domains and behavioural patterns.

### 🧩 Data Recovery & Exfiltration Tracing
- Recovered **deleted files** from unallocated space using Autopsy.
- Identified multiple exfiltration methods: external file‑hosting sites, unauthorised cloud applications, and unknown USB devices.
- Correlated browser history, USB logs, and server query logs to trace data movement.

### 📋 Legal & Communication Skills
- Generated comprehensive **HTML forensic reports** for case documentation.
- Created **Chain of Custody forms** for evidence items (#001 Patient Records, #002 Phishing Email).
- Produced a **court‑ready presentation** summarising findings for legal stakeholders.
- Filmed a **video demonstration** of the full investigative process to support peer and legal review.

---

## 📂 Course Breakdown

| Module | Focus Area | Key Outcomes |
| :--- | :--- | :--- |
| **Lab 1** | Metadata Forensics | Extracted hidden authorship, timestamps, and MD5 checksums from DOCX/PNG/JPEG files using ExifTool; compared file versions to detect tampering. |
| **Lab 2** | User Activity Tracking | Reconstructed program executions and file opens using LastActivityView; identified the 5 most recent system activities. |
| **Lab 3** | System Uptime Analysis | Analysed startup/shutdown timelines using TurnedOnTimesView; identified unexpected shutdowns (crashes/power loss) vs. user‑initiated power‑offs. |
| **Lab 4** | Web Browsing Forensics | Aggregated multi‑browser history using BrowsingHistoryView; applied date/browser filters; created pivot tables in Excel to identify most‑visited domains and browser distribution. |
| **Final Project** | End‑to‑End Breach Investigation | Led a complete investigation into a healthcare data breach—acquired forensic images (FTK Imager), recovered deleted files (Autopsy), identified phishing as the attack vector, traced data exfiltration via USB/cloud/file‑sharing, and delivered a court‑ready presentation with Chain of Custody documentation. |

---

## 🏆 Spotlight: HealthNS7 Data Breach Investigation

**Case ID:** MECR1033-HNS7-0226 | **Role:** Lead Forensic Investigator

This capstone project simulated a real‑world government healthcare data breach affecting millions of citizens. My investigation:

- **Identified the Attack Vector:** Recovered a phishing email (`Urgent Action Required_HealthNS7_Update.eml`) from the Outlook folder of the compromised workstation.
- **Traced Data Exfiltration:** Correlated browser history (external file‑hosting sites), USB device logs (unknown device connected), and server logs (spike in database queries) to prove multiple transfer methods.
- **Recovered Deleted Evidence:** Used Autopsy to recover `leaked_.zip` files from unallocated space; fragments matched the dark web leak.
- **Maintained Legal Admissibility:** Verified the forensic image with MD5/SHA‑1 hashes (`1c382af...`), documented a complete Chain of Custody, and produced a court‑ready presentation.

---

## 🎓 Why This Matters

This portfolio demonstrates that I am not just a "tool runner"—I understand the **methodology** behind digital forensics. I can:

- Enter an incident scene and **securely acquire** evidence without altering it.
- **Recover hidden data** that perpetrators think they have destroyed.
- **Connect the dots** between disparate logs (emails, browser history, USB events, system uptime) to build a coherent timeline.
- **Communicate complex technical findings** to non‑technical stakeholders (legal teams, management, juries) with clarity and professionalism.

These skills are directly transferable to roles in **Digital Forensics, Incident Response, eDiscovery, and Cybersecurity Consulting**.

---

## 📁 Repository Structure


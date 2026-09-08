# MECR1033 – Digital Forensics (Final Project: HealthNS7 National Portal Data Breach Investigation)

**Semester:** 1 | **Year:** 2025/2026 | **Instructor:** Assoc. Prof. Ts. Dr. Siti Hajar Othman

**Case ID:** MECR1033-HNS7-0226 | **Investigator:** Keertennah Devi A/P Ponnambalam | **Date:** 15 February 2026

---

## 📋 Project Overview

This project simulates a **real-world digital forensic investigation** into a major data breach affecting a government healthcare system (HealthNS7 National Portal). The breach resulted in the unauthorised exposure of sensitive patient records belonging to millions of citizens. As the lead forensic investigator, I was tasked with identifying the attack vector, tracing data exfiltration methods, recovering deleted evidence, and documenting the entire process in a **court‑ready format**.

The investigation followed industry best practices for **evidence acquisition, analysis, chain of custody, and reporting** to ensure findings are admissible in legal proceedings.

---

## 🎯 Learning Objectives

- Apply the **full forensic investigation lifecycle**—from evidence acquisition to court presentation.
- Use **FTK Imager** to create a verified, bit‑for‑bit forensic image (E01) of a suspect drive.
- Use **Autopsy** to analyse file systems, recover deleted files, and extract key artefacts (emails, browser history, USB logs).
- Identify and document the **attack vector** (phishing email) and **data exfiltration methods**.
- Recover **deleted files** from unallocated space to uncover hidden evidence.
- Maintain a **verifiable Chain of Custody** for all evidence items.
- Generate a **comprehensive forensic report** and **court‑ready presentation**.
- Produce a **video demonstration** of the investigation process for peer/legal review.

---

## 🛠️ Tools & Technologies Used

| Tool | Purpose |
| :--- | :--- |
| **FTK Imager 4.7.1** | Forensic imaging – created a verified E01 image of the employee workstation. |
| **Autopsy 4.21.0** | Digital forensics platform – file system analysis, deleted file recovery, email parsing, artefact extraction. |
| **MD5 / SHA-1 Hashing** | Integrity verification of the acquired forensic image. |
| **Chain of Custody Forms** | Documented evidence handling from collection to final storage. |
| **Microsoft PowerPoint** | Created a court‑ready presentation summarising findings. |
| **Video Recording** | Demonstrated the full investigation process. |

---

## 📚 Key Skills Developed

- **Forensic Imaging** – Created verified, bit‑for‑bit copies of storage media using FTK Imager, with hash verification (MD5/SHA‑1) to ensure integrity.
- **Artefact Analysis** – Extracted and examined emails, file metadata, browser history, USB device history, and application logs using Autopsy.
- **Deleted File Recovery** – Recovered files from unallocated space, including a `.zip` archive containing fragments of leaked patient data.
- **Attack Vector Identification** – Analysed a phishing email that led to credential theft and initial system compromise.
- **Data Exfiltration Tracing** – Correlated browser history, USB device logs, and server logs to identify multiple data transfer methods.
- **Evidence Documentation** – Maintained complete Chain of Custody records for all evidence items, ensuring legal admissibility.
- **Court‑Ready Reporting** – Produced a professional investigation report and presentation summarising findings for legal proceedings.
- **Process Repeatability** – Documented all steps, tools, and configurations to allow independent verification by another examiner.

---

## 🔍 Key Findings

### 1. Attack Vector (Phishing)
- A phishing email titled **"Urgent Action Required_HealthNS7_Update.eml"** was recovered from the employee's Outlook folder.
- The email tricked the employee into entering credentials on a fake portal (`http://healthns7-portal.com/verify`).
- **Impact:** Credential theft enabled unauthorised access to the HealthNS7 system.

### 2. Data Exfiltration Methods
The investigation identified **multiple** data transfer methods:

| Method | Evidence |
| :--- | :--- |
| **File Compression** | The employee accessed and compressed sensitive `.csv` patient records into a `.zip` archive. |
| **External File Hosting** | Browser history showed visits to external file‑sharing websites during the breach period. |
| **Unauthorised Cloud App** | An unknown cloud storage application was installed on the workstation. |
| **USB Device** | System logs showed an unknown USB device was connected—not recorded in the organisation's asset management system. |
| **Database Queries** | Server logs revealed a spike in database queries from the employee's IP address, culminating in large data downloads. |

### 3. Timeline of Events

| Date | Activity |
| :--- | :--- |
| **Jan 15** | Phishing email received and opened (confirmed from email metadata). |
| **Jan 18 - Jan 30** | Unusual spike in database queries from the employee's workstation (server logs). |
| **Jan 22 & Jan 28** | Files accessed, compressed, and external file‑sharing sites visited (file metadata & browser history). |
| **Jan 29** | Unknown USB device connected (USB history). |
| **Feb 1** | Leaked data first appears on dark web forums. |

### 4. Deleted File Recovery
- Deleted files (named `leaked_.zip`) were recovered from unallocated space.
- The recovered files contained fragments matching the leaked patient data found on the dark web.

### 5. Evidence Integrity
- **Forensic Image Hash:** MD5: `1c382af030dab30ee97caca3247c0e75` | SHA‑1: `3a4d0acb0e85409986a0056b9a21e2703ce2c718`
- **Evidence Item #001 (Patient Record):** MD5 `8b410373af0fe37ce3fcd39dd1cb8421`
- **Evidence Item #002 (Phishing Email):** MD5 `3d1123e0384de0cb5fe4236ad55cc9c`

---

## 📂 Folder Contents

| File | Description |
| :--- | :--- |
| `FINAL-AA-DIGITAL-FORENSIC_KEERTENNAHDEVI.pdf` | Comprehensive forensic investigation report. |
| `COURT-READY-PRESENTATION_KEERTENNAH.pdf` | Presentation summarising findings for legal proceedings. |
| `EVIDENCE-FORM_KEERTENNAHDEVI.pdf` | Chain of Custody forms for items #001 and #002. |
| `Video-Demonstration_Link.txt` | Link to video walkthrough of the investigation process. |

---

## 🔍 Reflection

This capstone project was the culmination of everything I learned in Digital Forensics. It pushed me beyond simply running tools—I had to **think like an investigator**, connecting disparate pieces of evidence (email metadata, browser history, USB logs, server logs) into a coherent narrative that would hold up in court.

The most valuable lesson was the importance of **integrity and repeatability**. Creating a verified forensic image with FTK Imager and maintaining a strict Chain of Custody ensured that no one could question the evidence's authenticity. This is the difference between a "hobbyist" and a **professional forensic examiner**.

Recovering deleted files from unallocated space was another highlight. The perpetrator had deleted the `leaked_.zip` files, but because the data clusters weren't overwritten, Autopsy allowed me to recover fragments that matched the dark web leak—proving the workstation was the source of the breach.

Finally, producing a **court‑ready presentation** taught me the importance of communicating technical findings to non‑technical audiences (judges, juries, legal teams). The ability to translate complex forensic artefacts into clear, compelling visuals is a skill I'll carry into my cybersecurity career.

---

## 🏆 Project Deliverables

- [x] Forensic image acquisition with hash verification
- [x] In‑depth analysis using Autopsy
- [x] Deleted file recovery and examination
- [x] Attack vector identification (phishing)
- [x] Data exfiltration tracing
- [x] Chain of Custody documentation
- [x] Comprehensive forensic report
- [x] Court‑ready presentation
- [x] Video demonstration of the process

---

*Last Updated: September 2026*

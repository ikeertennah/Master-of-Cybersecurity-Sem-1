# MECR1033 – Digital Forensics (Lab 1: Metadata Analysis with ExifTool)

**Semester:** 1 | **Year:** 2025/2026 | **Instructor:** PM Ts. Dr. Siti Hajar Othman 

---

## 📋 Lab Overview

This lab introduces the fundamental concepts of **digital forensics** by focusing on **metadata extraction and analysis**. Using **ExifTool**, I investigated file metadata to uncover hidden information about document authorship, edit history, file integrity, and format differences. This exercise demonstrates how digital evidence can be authenticated and contextualized using non‑visible file properties.

---

## 🎯 Learning Objectives

- Understand the role of **metadata** in digital forensics investigations (e.g., proving authorship, timelines, and tampering).
- Use **ExifTool** (CLI) and online alternatives to extract metadata from various file types (DOCX, PNG, JPEG, PDF, XLSX).
- Compare file versions using **checksums (MD5)** to verify file integrity and identify subtle alterations.
- Distinguish between **file formats** (PNG vs. JPEG) and understand how their metadata structures differ.
- Document digital evidence using a **Chain of Custody form** to maintain forensic integrity.

---

## 🛠️ Tools & Technologies Used

- **ExifTool** – Command-line utility for reading/writing metadata across hundreds of file types (images, documents, audio).
- **Metadata2Go.com** – Online tool for quick metadata analysis without local installation.
- **EZGIF.com** – Alternative online metadata viewer.
- **MD5 Checksum** – Used to generate unique digital fingerprints (hashes) for file integrity verification.

---

## 📚 Key Skills Developed

- **Metadata Forensics** – Extracted and interpreted file metadata (author, creation/modification dates, software used, revision history).
- **Integrity Verification** – Applied hashing (MD5) to compare files and confirm their uniqueness or authenticity.
- **Evidence Documentation** – Created detailed **Chain of Custody forms** for multiple evidence items (images, PDFs, spreadsheets).
- **File Format Analysis** – Compared PNG (lossless) vs JPEG (lossy) metadata and compression properties.
- **Investigative Thinking** – Correlated metadata inconsistencies (e.g., revision numbers, editing times) to reconstruct file histories.

---

## 🔍 Key Findings & Analysis

### 1. DOCX Metadata Analysis (Test 1 File)
- **Creator:** "Windows User" (generic)
- **Last Modified By:** "Siti Hajar Othman"
- **Timeline:** Created in 2020, modified in 2024
- **Software:** WPS Office (version 12.2.0.18283)
- **Stats:** 1 page, 19 words, 2 minutes editing time
- **MD5:** `102468fee024337ebb7405b0eb3a5d6a`

### 2. Comparing Test 1 vs Test 1a
Despite identical visible content, metadata revealed they are **distinct files**:
| Feature | Test 1 | Test 1a |
| :--- | :--- | :--- |
| **MD5 Checksum** | `102468...` | `3ee002...` |
| **Revision Number** | 2 | 3 |
| **Creation Time** | 03:42:00Z | 04:25:00Z |
| **Character Count** | 111 | 110 |

**Conclusion:** "Test 1a" is a later, re‑saved version with a minor content alteration—proving that metadata + hashing can detect tampering even when text appears identical.

### 3. Image Analysis (iasrg A vs iasrg B)
- **iasrg A:** PNG format (lossless compression, limited metadata fields).
- **iasrg B:** JPEG format (lossy compression, robust EXIF/IPTC/XMP metadata structure).
- **Content:** Both display the same text ("Information Assurance and Security Research Group").

### 4. Chain of Custody Documentation
Created forensic evidence forms (Items #002–#005) documenting:
- Image files, PDFs, and Excel spreadsheets.
- Tracking logs, personnel transfers, timestamps, and hashes to ensure admissibility in legal proceedings.

---

## 🔍 Reflection

This lab reinforced that **metadata is a goldmine for forensic investigators**. While a file's visible content may appear unchanged, its metadata tells a different story—who touched it, when, with what software, and whether it was altered.

The most valuable takeaway was understanding that **integrity (via hashing) + provenance (via metadata)** form the backbone of digital evidence admissibility. Practicing with ExifTool gave me hands‑on confidence in extracting actionable intelligence from everyday files (documents, images, spreadsheets)—a skill directly applicable to incident response, eDiscovery, and insider threat investigations.

I also learned the importance of **chain of custody documentation**; even the best forensic analysis is useless if the evidence trail is broken. This lab prepared me to handle evidence professionally in real‑world corporate or law enforcement scenarios.

---

*Last Updated: September 2026*

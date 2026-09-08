# MECR1033 – Digital Forensics (Lab 2: System Activity Log Analysis with LastActivityView)

**Semester:** 1 | **Year:** 2025/2026 | **Instructor:** PM Ts. Dr. Siti Hajar Othman | **GPA:** 4.00
---

## 📋 Lab Overview

This lab introduces **Windows system forensics** by analysing user and system activities logged by the operating system. Using **NirSoft's LastActivityView**, I reconstructed a chronological timeline of actions performed on a Windows machine—including program executions, file openings, software installations, and system events. This exercise demonstrates how investigators can quickly profile user behaviour, identify suspicious activities, and generate structured forensic reports without manually parsing raw Event Logs.

---

## 🎯 Learning Objectives

- Understand how Windows logs user and system activities across multiple sources (Registry, Event Logs, Prefetch files).
- Use **LastActivityView** to aggregate and visualise forensic artefacts in a single interface.
- Identify and interpret key activity types (e.g., program execution, file access, network events).
- Generate customisable HTML reports for evidence documentation and presentation.
- Apply timeline analysis to determine the sequence of events during an investigation.

---

## 🛠️ Tools & Technologies Used

- **LastActivityView (NirSoft)** – Lightweight Windows utility that collects and displays a comprehensive log of user actions and system events from multiple sources.
- **HTML Report Generation** – Exported forensic findings into structured HTML formats (full report and filtered report).

---

## 📚 Key Skills Developed

- **Windows Forensics** – Extracted and analysed system activity logs without requiring deep Event Viewer navigation.
- **Timeline Analysis** – Reconstructed chronological sequences of user behaviour (e.g., what executables ran, when files were opened).
- **Activity Profiling** – Identified patterns (e.g., frequent program launches, file access habits) to distinguish normal vs. suspicious behaviour.
- **Forensic Reporting** – Generated professional HTML reports with selected fields (`Action Time`, `File Name`, `Full Path`) for clear evidence presentation.
- **Artefact Correlation** – Understood how LastActivityView aggregates data from Prefetch, Registry, and Event Logs to provide a unified view.

---

## 🔍 Key Findings & Analysis

### 1. Output Components
The LastActivityView panel displays the following key columns for each event:
- **Action Time** – Timestamp of the activity.
- **Product Name** – Software product associated with the event.
- **File Name** – Executable or filename involved.
- **Full Path** – Complete directory path to the file.
- **Other Information** – Additional context (e.g., document title for file opens).

### 2. Last 5 Activities Retrieved
A chronological snapshot from the system history revealed:
| # | Activity |
| :--- | :--- |
| 1 | Program Execution – Windows Explorer (`explorer.exe`) started. |
| 2 | Program Execution – Security/Defender process (`MsMpEng.exe`) started. |
| 3 | Program Execution – Cloud storage service (`OneDrive.exe`) started. |
| 4 | Program Execution – Web Browser (`chrome.exe` or `msedge.exe`) started. |
| 5 | File Open – Document (`SHO CF Lab 2.docx`) opened in Microsoft Word (`WINWORD.EXE`). |

### 3. Latest Activity Timestamp
- **Date/Time:** `1/12/2025 3:12:30 PM`

### 4. Most Common Activity Types
- **Program Execution/Started** – Every application or background process launch (e.g., `chrome.exe`, `explorer.exe`, `svchost.exe`).
- **File Open** – Document, image, or other file access events through various programs.

---

## 🔍 Reflection

This lab highlighted the power of **aggregated system logging** in digital forensics. While tools like Windows Event Viewer are useful, they scatter information across hundreds of log IDs. LastActivityView consolidates these artefacts into a single, human‑readable timeline—saving investigators precious time during incident response.

The most valuable takeaway was **timeline reconstruction**. By observing the sequence of events (e.g., browser launch followed by document access), I can now build a narrative of user activity. This is critical for insider threat investigations, malware triage (identifying persistence mechanisms), and data exfiltration cases.

I also appreciated the **reporting flexibility**—generating custom HTML reports with only essential fields makes it easier to share findings with non‑technical stakeholders (e.g., legal teams or management) without overwhelming them with raw data.

---

*Last Updated: September 2026*

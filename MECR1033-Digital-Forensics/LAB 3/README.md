# MECR1033 – Digital Forensics (Lab 3: System Logon/Logoff Analysis with TurnedOnTimesView)

**Semester:** 1 | **Year:** 2025/2026 | **Instructor:** PM Ts. Dr. Siti Hajar Othman

---

## 📋 Lab Overview

This lab introduces **Windows system uptime forensics** by analysing event logs to reconstruct when a computer was turned on and off. Using **NirSoft's TurnedOnTimesView**, I extracted startup/shutdown timelines, identified system failures vs. user-initiated shutdowns, and interpreted hexadecimal shutdown codes. This exercise demonstrates how investigators can correlate system availability with suspicious activity timestamps and detect tampering attempts (e.g., shutting down a system to cover tracks).

---

## 🎯 Learning Objectives

- Understand how Windows Event Logs record system power events (startup, shutdown, sleep, crash).
- Use **TurnedOnTimesView** to aggregate startup/shutdown data across local, remote, and external disk sources.
- Interpret critical forensic fields: `Shutdown Reason`, `Shutdown Type`, `Shutdown Code`, and `Duration`.
- Identify patterns such as **System Failure** (crashes, power loss) vs. **User-Initiated** shutdowns.
- Apply system uptime analysis to validate alibis and detect evidence tampering.
- Export findings and utilise visual aids (`Mark Odd/Even Rows`) for clearer report presentation.

---

## 🛠️ Tools & Technologies Used

- **TurnedOnTimesView (NirSoft)** – Lightweight Windows tool that extracts and displays system startup/shutdown timelines from the Windows Event Log.
- **Windows Event Log** – Backend data source (Event IDs: 41, 42, 1, 1074, 6005, 6006) for system power events.
- **HTML Export** – Generated professional reports of system uptime data for legal documentation.

---

## 📚 Key Skills Developed

- **System Uptime Forensics** – Reconstructed system availability timelines to understand when a computer was actively running.
- **Event Log Analysis** – Interpreted critical Event IDs (Kernel-Power, USER32, EventLog) without manually navigating Event Viewer.
- **Crash & Failure Identification** – Distinguished between user-initiated shutdowns and unexpected failures (crashes, power outages, hardware issues).
- **Timeline Correlation** – Linked on/off states to potential windows of malicious activity (e.g., ransomware execution, data exfiltration).
- **Remote & External Disk Forensics** – Understood how to analyse logs from other machines or offline forensic images.
- **Visual Data Optimisation** – Used `Mark Odd/Even Rows` to improve log readability during analysis.

---

## 🔍 Key Findings & Analysis

### 1. Fields Displayed
Upon opening TurnedOnTimesView, the following key fields were observed:

| Field | Description |
| :--- | :--- |
| **Startup Time** | Exact date/time when the computer powered on. |
| **Shutdown Time** | Exact date/time when the computer powered off. |
| **Last System Event** | Last recorded activity before shutdown (useful when shutdown log is missing). |
| **Duration** | Total time the system remained turned on. |
| **Shutdown Reason** | Why the system shut down (e.g., System Failure, User action). |
| **Shutdown Type** | Normal, Unexpected, or Sleep. |
| **Shutdown Process** | Which process initiated the shutdown (e.g., `winlogon.exe`). |
| **Shutdown Code** | Hexadecimal code related to the shutdown event (e.g., `0x000500ff`). |
| **Computer Name** | The target machine (identified as **DUNE**). |

### 2. Findings from the Analysis
- **Total Logs Captured:** 287 startup/shutdown events.
- **Computer Name:** `DUNE`.
- **Sample Shutdown Code:** `0x000500ff`.

### 3. Shutdown Reasons Identified
- **System Failure** was present in the logs—indicating unexpected shutdowns due to:
  - System crashes (blue screens).
  - Hardware failures.
  - Power outages.
- **User-Initiated** shutdowns were also identifiable, showing normal system behaviour.

### 4. Visual Optimisation
- Enabled **"Mark Odd/Even Rows"** under the View menu to highlight alternating rows—this significantly improved readability when reviewing large log sets (first 20 rows were captured as a snapshot).

### 5. Key Event IDs Used by the Tool
Understanding the underlying sources:
- **EventID 41** – Kernel-Power: System rebooted without clean shutdown (crash/power loss).
- **EventID 42** – Kernel-Power: System entering sleep.
- **EventID 1** – Power-Troubleshooter: System resumed from sleep.
- **EventID 1074** – USER32: User or process initiated a shutdown.
- **EventID 6005** – EventLog: Event log service started (system boot).
- **EventID 6006** – EventLog: Event log service stopped (system shutdown).

### 6. Alternative Tools for Similar Analysis
To show broader context, I identified similar forensic tools:
- **Windows Event Viewer** – Manual review of startup/shutdown logs.
- **LastActivityView** – Aggregated user/system activity timeline.
- **Windows Reliability Monitor** – Visualises system stability and crash history.
- **LogonSessions (Sysinternals)** – Analyses active logon sessions.
- **FTK Imager** – Extracts system event logs from forensic images.

---

## 🔍 Reflection

This lab reinforced that **system availability is just as critical as file metadata** in a forensic investigation. A computer that was turned off during a critical time window could explain a gap in digital evidence—or conversely, a system that stayed on overnight might indicate automated malware activity or a malicious insider working after hours.

The most valuable takeaway was understanding **why** a system shuts down. Distinguishing between **System Failure** (crashes, power loss) and **User-Initiated** shutdowns provides vital context:
- A System Failure during an attack might indicate a **blue screen caused by exploit code**.
- A User-Initiated shutdown immediately after suspicious file access could suggest **tampering or cover-up**.

I also appreciated that TurnedOnTimesView can read logs from **external disks** (forensic images) and remote computers—this is a huge practical advantage for incident responders who need to triage multiple machines without booting them up (which would alter metadata). This lab prepared me to confidently integrate system uptime analysis into broader Digital Forensics and Incident Response (DFIR) workflows.


---

*Last Updated: September 2026*

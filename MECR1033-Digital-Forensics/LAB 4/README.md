# MECR1033 – Digital Forensics (Lab 4: Web Browsing History Analysis with BrowsingHistoryView)

**Semester:** 1 | **Year:** 2025/2026 | **Instructor:** Assoc. Prof. Ts. Dr. Siti Hajar Othman

---

## 📋 Lab Overview

This lab explores **web browsing forensics** by analysing browser history data using **NirSoft's BrowsingHistoryView**. The tool aggregates browsing history from multiple browsers (Chrome, Edge, Firefox, Internet Explorer, Opera) into a single, unified table. Through this exercise, I investigated user activity patterns, applied date-based and browser-specific filters, exported data for further analysis, and generated professional reports. This demonstrates how forensic investigators can reconstruct a user's online activities, correlate browsing behaviour with incident timelines, and identify potential indicators of compromise (IoCs).

---

## 🎯 Learning Objectives

- Understand how BrowsingHistoryView extracts and aggregates browsing history from multiple web browsers.
- Load and interpret local browsing history from the current user profile.
- Apply **date/time filters** to isolate activity within specific forensic windows (e.g., last 24 hours).
- Apply **browser-specific filters** to isolate activity by browser type (e.g., Chrome).
- Export filtered data into **CSV**, **TXT**, and **HTML** formats for documentation and further analysis.
- Create **pivot tables** in Excel to visualise visit frequency by domain and browser distribution.
- Generate a professional **HTML report** summarising browsing activity over a defined period.
- Discuss the forensic value of filtering by date, browser, and domain to reconstruct user behaviour and detect anomalies.

---

## 🛠️ Tools & Technologies Used

- **BrowsingHistoryView (NirSoft)** – Lightweight Windows tool that reads and displays browsing history from all major web browsers (Chrome, Firefox, Edge, Internet Explorer, Opera) in a single interface.
- **Microsoft Excel** – Used to create pivot tables for quantitative analysis of browsing patterns.
- **Windows File System** – Accessed browser history databases stored locally under user profiles.
- **HTML Export** – Generated comprehensive reports for legal documentation and case management.

---

## 📚 Key Skills Developed

- **Web Browsing Forensics** – Reconstructed user browsing timelines by analysing visited URLs, titles, visit times, and visit counts.
- **Multi-Browser Aggregation** – Learned to view browsing history from multiple browsers simultaneously without manually opening each browser's history.
- **Timeline Filtering** – Applied date-range filters to focus on specific forensic windows (e.g., incident timeframes, suspicious activity periods).
- **Browser-Specific Profiling** – Isolated activity from a single browser to identify patterns, most visited domains, and potential misuse.
- **Data Export & Visualisation** – Exported data in multiple formats (CSV, TXT, HTML) and used pivot tables to identify top domains and browser usage distribution.
- **Report Generation** – Produced structured HTML reports for documentation and case presentation.
- **Forensic Contextualisation** – Correlated browsing history with user behaviour to assess intent, detect anomalies, and build timelines.

---

## 🔍 Key Findings & Analysis

### 1. Tool Capabilities & Detected Browsers

Upon launching BrowsingHistoryView, the tool successfully detected and displayed history from:

| Browser | Detection Status |
| :--- | :--- |
| **Google Chrome** | ✅ Detected |
| **Microsoft Edge** | ✅ Detected |
| **Internet Explorer** | ✅ Detected |
| **Mozilla Firefox** | ❌ Not installed on the test system |
| **Opera** | ❌ Not installed on the test system |

**Figure 1 & 2** in the lab report confirmed that the tool successfully loaded browsing history tables for both Chrome and Edge/Internet Explorer.

---

### 2. Fields Displayed

The tool presented the following key forensic fields:

| Field | Description |
| :--- | :--- |
| **Visited URL** | Full web address accessed by the user. |
| **Title** | Page title of the visited website. |
| **Visit Time** | Exact date/time of the visit. |
| **Visit Count** | Number of times the URL was visited. |
| **Web Browser** | Which browser was used (e.g., Chrome, Edge). |
| **User Profile** | The Windows user profile associated with the browsing activity. |

---

### 3. Last 10 Websites Visited (Task 2)

From the current user profile, the **last 10 websites visited** were identified (all on **15 January 2026** using **Chrome**):

| No. | URL | Website Title | Visit Time | Browser |
|:---:|:---|:---|:---:|:---:|
| 1 | https://studentportal.utm.my/pdpa | Student Portal | 2:50 AM | Chrome |
| 2 | https://studentportal.utm.my/ | Student Portal | 2:50 AM | Chrome |
| 3 | https://my.utm.my/home | MyUTM Portal | 2:49 AM | Chrome |
| 4 | https://my.utm.my/login | MyUTM Portal | 2:48 AM | Chrome |
| 5 | https://web.whatsapp.com/ | WhatsApp | 2:48 AM | Chrome |
| 6 | https://odlsystem.utm.my/25261/course/view.php?id=93 | Course: MECR1013 | 2:46 AM | Chrome |
| 7 | https://odlsystem.utm.my/25261/my/ | Dashboard ODL | 2:46 AM | Chrome |
| 8 | https://odlsystem.utm.my/25261/mod/assign/view.php?id=7884 | Course: MECR1023 | 2:45 AM | Chrome |
| 9 | https://odlsystem.utm.my/25261/mod/assign/view.php?id=5649&forceview=1 | Course: MECR1033 | 2:42 AM | Chrome |
| 10 | https://odlsystem.utm.my/25261/login/index.php | Login into site | 2:40 AM | Chrome |

**Observation:** All 10 entries were from **Google Chrome**, suggesting it was the primary browser used during this session. The visits indicate academic activity (UTM portals, ODL system) with a brief use of WhatsApp.

---

### 4. Date Range Filtering (Task 3)

| Metric | Value |
| :--- | :--- |
| **Total History Entries (Before Filtering)** | **18,352** items |
| **Entries After Filtering (Last 24 Hours)** | **41** items |
| **Reduction** | ~99.8% reduction |

Filtering by date range drastically reduced data noise, allowing investigators to focus on **recent user actions**. This is critical in timeline analysis and intrusion investigations, where only activity within a specific window matters.

---

### 5. Browser-Specific Filtering (Task 4)

- **Filter Applied:** Only Google Chrome history displayed.
- **Most Frequently Visited Domain in Chrome:** `odlsystem.utm.my` (ODL System – UTM's online learning platform).

**Filtering by browser** is useful in forensic investigations because:
- Different browsers are often used for distinct purposes (work vs. personal), helping reconstruct behavioural patterns.
- Certain malware or exploits target specific browsers; filtering allows quick identification of malicious activity.
- It supports user profiling and intent analysis.
- It enables correlation with other forensic artefacts (e.g., network logs, system events) for a coherent timeline.

---

### 6. Exporting Data & Pivot Tables (Task 5)

#### Pivot Table 1: Visits per Domain
The domain with the highest number of visits was **odlsystem.utm.my**, reflecting consistent academic activity.

#### Pivot Table 2: Distribution of Visits Across Browsers
| Browser | Visit Count |
| :--- | :---: |
| **Google Chrome** | **Highest** (dominant) |
| **Microsoft Edge** | Lower |
| **Internet Explorer** | Minimal/None |

**Chrome dominated the browsing history**, which suggests the user predominantly used Chrome for academic and personal browsing.

---

### 7. Report Generation (Task 6)

An **HTML report** was generated for the **last 7 days**, including:
- Website Title
- URL
- Visit Time
- Browser Type

This report was exported and uploaded to the Google Drive folder for documentation and submission.

---

## 🔍 Reflection

This lab reinforced that **web browsing history is a treasure trove of forensic evidence**. It provides direct insight into a user's online behaviour, including academic activity, communication patterns, and potential exposure to malicious content. The ability to aggregate history from multiple browsers into a single view using BrowsingHistoryView is a significant time-saver compared to manually inspecting each browser's history individually.

The most valuable takeaway was the importance of **filtering**. By applying date and browser filters, I could isolate relevant data from thousands of entries, reducing noise and focusing on critical forensic windows. For instance, filtering by the last 24 hours revealed only 41 visits out of 18,352—a 99.8% reduction—demonstrating how filters can streamline an investigation.

Additionally, the use of **pivot tables** in Excel enabled me to quantify browsing patterns, identifying the most visited domains and the user's primary browser. This kind of analysis is essential for profiling user behaviour, detecting anomalies, and correlating activity with other artefacts (e.g., file downloads, login events).

Ultimately, this lab prepared me to confidently integrate web browsing forensics into broader Digital Forensics and Incident Response (DFIR) workflows, using tools like BrowsingHistoryView to reconstruct digital footprints efficiently and professionally.

---

## 📂 Folder Contents

| Task | File Name | File Type |
| :---: | :--- | :---: |
| 3 | `history_last24hours` | TXT file |
| 5 | `BrowsingHistory_Export` | CSV file |
| 5 | `BrowsingHistory_Export (Pivot 1 & Pivot 2).csv` | Excel file |
| 6 | `last7days_history` | HTML file |

All files are uploaded to the Google Drive folder:  
🔗 [https://drive.google.com/drive/folders/1pKbJgn0LqGn4QJa_j9DwrTC4wacqRh3L?usp=sharing](https://drive.google.com/drive/folders/1pKbJgn0LqGn4QJa_j9DwrTC4wacqRh3L?usp=sharing)

---

*Last Updated: September 2026*

# MECR1073 – Penetration Testing 

**Semester:** 1 | **Year:** 2025/2026

---

## 🔍 Executive Summary

This repository showcases my hands-on experience in **Penetration Testing** across the full attack lifecycle—from **reconnaissance** and **anonymisation** to **scanning, enumeration, vulnerability exploitation, and web application attacks**. Using industry-standard tools (Nmap, Metasploit, ZAP, BeEF-XSS, Netdiscover, Sherlock, DNSRecon, Proxychains, and TOR), I conducted realistic penetration tests against virtualised targets (Metasploitable 2/3, Windows 10, and DVWA). This portfolio demonstrates the technical proficiency, methodology, and reporting discipline required for roles in **Penetration Testing, Red Team Operations, and Security Assessment**.

---

## 🎯 Core Learning Objectives

- Apply the **Penetration Testing Execution Standard (PTES)** and reconnaissance methodology in black-box engagements.
- Conduct **passive and active reconnaissance** using Google dorking, WHOIS, DNS enumeration, and social media OSINT.
- Anonymise traffic using **Proxychains and TOR** to avoid attribution during active scanning.
- Perform **host discovery, port scanning, service enumeration, and OS fingerprinting** using Nmap, Netdiscover, and P0f.
- Conduct **vulnerability scanning** using Nessus and query CVE databases to identify exploitable weaknesses.
- Exploit real vulnerabilities (Apache Tomcat, BlueKeep, Apache Path Traversal) using **Metasploit**.
- Perform **web application penetration testing** against OWASP vulnerabilities (Brute Force, SQL Injection, XSS Reflected/Stored, CSRF) using ZAP and BeEF-XSS.

---

## 🛠️ Tools & Technologies

| Category | Tools |
| :--- | :--- |
| **Reconnaissance & OSINT** | Google Dorking, WHOIS, Sherlock, Netcraft, DMitry |
| **DNS Enumeration** | DNSRecon, DNSEnum |
| **Anonymisation** | Proxychains, TOR Network, TOR Browser |
| **Network Scanning** | Nmap (ping sweep, TCP/UDP scan, FIN scan, OS detection, banner grabbing), Netdiscover, Zenmap |
| **Vulnerability Scanning** | Nessus, CVE Databases (cvedetails.com) |
| **Exploitation** | Metasploit Framework, MSFVenom |
| **OS Fingerprinting** | Nmap (-O), P0f (passive) |
| **Packet Analysis** | Wireshark |
| **Web App Testing** | OWASP ZAP, Burp Suite, BeEF-XSS |
| **Targets** | Metasploitable 2, Metasploitable 3, Windows 10, OWASP Broken Web App (DVWA) |
| **Virtualisation** | VirtualBox (NAT Network 10.0.2.0/24), Kali Linux |

---

## 📚 Key Skills Developed

### 🔎 Reconnaissance & OSINT
- Executed **Google dorking queries** (`site:`, `inurl:`, `intitle:`) to discover UTM's public systems.
- Used **Sherlock** to identify social media accounts linked to a target username (`utm.my`).
- Queried **WHOIS** to extract domain registration data (registrar, creation date, name servers).
- Correlated **job postings** to map an organisation's technology stack (Cisco, Windows/Linux, PHP/Laravel, React.js, Azure, VMware, Active Directory).

### 🌐 DNS Enumeration
- Performed **subdomain enumeration** using DNSRecon and DNSEnum.
- Identified **A, CNAME, NS, and MX records**, and mapped IP ranges (161.139.17.0/24 – 161.139.250.0/24).
- Analysed **zone transfer failures** and understood why automated tools miss organisation-specific subdomains.

### 🕵️ Anonymisation Techniques
- Configured **Proxychains** with a chain of three SOCKS5 proxies (US-based) to mask traffic origin.
- Verified IP masking using **DNSLeakTest** (exit node: Roanoke, United States).
- Configured **TOR** with Proxychains and validated anonymised DNS queries.
- Navigated the **TOR Hidden Wiki** and explored `.onion` services.
- Understood why standard proxy chains cannot resolve `.onion` domains (TOR-exclusive).

### 🔍 Network Scanning & Enumeration
- Conducted **ping sweeps** with Nmap (`-sn`) to discover live hosts on a NAT network.
- Performed **active and passive ARP scans** with Netdiscover (`-r`, `-p`).
- Executed **TCP full scan** (`-sT`), **inverse/FIN scan** (`-sF`), and **UDP scan** (`-sU`) to discover open services.
- Used **Wireshark** to analyse FIN scan and UDP scan behaviour at the packet level.
- Mapped the network topology with **Zenmap**.

### 🖥️ OS Fingerprinting & Banner Grabbing
- Conducted **active OS fingerprinting** with `nmap -O`.
- Conducted **passive OS fingerprinting** with **P0f**.
- Performed **banner grabbing** with `nmap -A` to identify service providers and versions (e.g., Apache 2.2.8, MySQL 5.0.51a, OpenSSH 4.7p1).

### 🛡️ Vulnerability Scanning & Exploitation
- Ran **Nessus** scans against Metasploitable 3 to identify critical CVEs.
- Prioritised vulnerabilities by **CVSS score** (Apache Tomcat 8.0.x = 10.0; BlueKeep = 9.8; Apache 2.4.49 = 9.8).
- Successfully exploited:
  - **Apache Tomcat 8.0.x (CVE-2017-12615)** via `tomcat_jsp_upload_bypass` → Meterpreter session.
  - **Apache HTTP 2.4.49 Path Traversal (CVE-2021-41773)** via `apache_normalize_path` → reverse shell.
- Analysed a failed exploit attempt (**BlueKeep / CVE-2019-0708**) due to RDP port being closed.

### 🌐 Web Application Penetration Testing
- Exploited **Brute Force** login via **ZAP Fuzzer** with wordlists → cracked password (`admin`) in ~5 minutes.
- Exploited **SQL Injection** (manual `1' OR '1'='1` and ZAP fuzzing) → dumped all user records.
- Exploited **Reflected XSS** (`<script>alert('XSS')</script>`) and extracted **session cookie (PHPSESSID)**.
- Exploited **Stored XSS** and used **BeEF-XSS** for post-exploitation (Facebook credential theft via Pretty Theft module).
- Analysed **CSRF** attack mechanics and crafted a malicious URL to change a user's password.

---

## 📂 Course Breakdown

| Lab | Focus Area | Key Outcomes |
| :--- | :--- | :--- |
| **Lab 1** | Reconnaissance | Google dorking, WHOIS lookup, Sherlock OSINT, DNS enumeration (DNSRecon/DNSEnum), Netcraft/DMitry IP range discovery. |
| **Lab 2** | Anonymisation | Proxychains with 3 SOCKS5 proxies, TOR configuration, DNSLeakTest verification, Hidden Wiki exploration, .onion limitations. |
| **Lab 3** | Scanning & Enumeration | Nmap ping sweep, Netdiscover ARP scans, TCP/FIN/UDP port scanning, Wireshark analysis, OS fingerprinting (Nmap & P0f), banner grabbing, Zenmap topology. |
| **Lab 4** | Vulnerability Scanning & Exploitation | Nessus scanning, CVE prioritisation (CVSS), Metasploit exploitation (Tomcat, Apache Path Traversal), failed BlueKeep analysis. |
| **Lab 5** | Web Application Pentesting | DVWA exploitation: Brute Force, SQL Injection, Reflected/Stored XSS, CSRF, session hijacking, BeEF-XSS post-exploitation. |

---

## 🏆 Spotlight #1: Network Reconnaissance & Enumeration

**Target:** UTM Network (Black-Box Engagement)

| Phase | Tool | Key Finding |
| :--- | :--- | :--- |
| **OSINT** | Google Dorking | Discovered UTM portals: `my.utm.my`, `studentportal.utm.my`, `finance.utm.my` |
| **Social Media** | Sherlock | Found `utm.my` accounts on GitLab, Spotify, Giphy, Envato, EyeEm |
| **WHOIS** | WHOIS | Registrar: Exabytes Network; Domain created: 29 Sep 1996; NS: ns1.utm.my, ns3.utm.my |
| **DNS Enum** | DNSRecon + DNSEnum | Discovered 20+ subdomains (apps, blog, portal, VPN, web, www) and 9 Class-C IP ranges |
| **IP Range** | DMitry + Netcraft | UTM operates on 161.135.0.0 – 161.146.255.255 (AS133914, APNIC region) |

**Key Insight:** Zone transfers were explicitly blocked (returned "corrupt packet" and "REFUSED"), and brute-force wordlists lacked UTM-specific terms—demonstrating why reconnaissance must combine automated tools with manual OSINT.

---

## 🏆 Spotlight #2: Vulnerability Exploitation (Metasploit)

**Target:** Metasploitable 3 (Windows Server 2008 R2)

| Vulnerability | CVE | CVSS | Exploit | Result |
| :--- | :--- | :--- | :--- | :--- |
| Apache Tomcat 8.0.x Upload Bypass | CVE-2017-12615 | 10.0 | `tomcat_jsp_upload_bypass` | ✅ Meterpreter session gained as tomcat user |
| Microsoft RDP BlueKeep | CVE-2019-0708 | 9.8 | `cve_2019_0708_bluekeep_rce` | ❌ Failed — port 3389 closed |
| Apache HTTP 2.4.49 Path Traversal | CVE-2021-41773 | 9.8 | `apache_normalize_path` | ✅ Reverse shell as apache user |

**Key Insight:** Not every vulnerability is exploitable in every environment. The BlueKeep exploit failed because the target's RDP service was not exposed—demonstrating the importance of verifying service availability before attempting exploitation.

---

## 🏆 Spotlight #3: Web Application Penetration Testing (DVWA)

**Target:** OWASP Broken Web Application (Damn Vulnerable Web App)

| Vulnerability | Technique | Tool | Result |
| :--- | :--- | :--- | :--- |
| **Brute Force** | Fuzzing with wordlists | OWASP ZAP | Cracked password (`admin`) in ~5 minutes |
| **SQL Injection** | Manual payload + Fuzzing | Manual + ZAP | Dumped all user records (admin, Gordon, Hack, Pablo, Bob, user) |
| **Reflected XSS** | `<script>alert('XSS')</script>` | Manual + ZAP | Alert pop-up; extracted PHPSESSID cookie |
| **Stored XSS** | `<script>alert(document.cookie)</script>` | Manual + BeEF | Persistent execution; captured Facebook credentials via BeEF |
| **CSRF** | Crafted malicious URL | Manual (ZAP to intercept) | Changed admin password to `abcd0866` |

**Key Insight:** The **BeEF-XSS** post-exploitation demonstrated how a single stored XSS payload can escalate into a full **client-side takeover**—hooking browsers, launching fake login prompts (Pretty Theft), and stealing credentials.

---

## 🎓 Why This Matters

This portfolio demonstrates that I understand **the full penetration testing lifecycle**—not just individual tools. I can:

- **Plan and execute** black-box reconnaissance using OSINT, DNS enumeration, and social media intelligence.
- **Anonymise traffic** using proxy chains and TOR to avoid attribution during active scanning.
- **Discover live hosts** and enumerate services using Nmap, Netdiscover, and Wireshark.
- **Fingerprint operating systems** using both active (Nmap) and passive (P0f) techniques.
- **Identify and prioritise vulnerabilities** using Nessus and CVSS scoring.
- **Exploit real vulnerabilities** using Metasploit (Tomcat, Apache Path Traversal).
- **Attack web applications** using OWASP techniques (SQLi, XSS, CSRF, Brute Force).
- **Perform post-exploitation** using BeEF-XSS and session hijacking.
- **Document findings** professionally with screenshots and evidence.

These skills transfer directly to roles in **Penetration Testing, Red Team Operations, Security Assessment, Vulnerability Management, and Application Security**.

---


---

## 🔍 Reflection

This course gave me a complete, end-to-end view of what it means to be a **penetration tester**—from passive intelligence gathering to active exploitation and post-exploitation.

**Reconnaissance (Lab 1):** I learned that 80% of a successful penetration test happens before a single packet is sent. Google dorking and WHOIS lookups revealed publicly available information that could be used to map an organisation's attack surface. The DNS enumeration exercise was particularly eye-opening—zone transfer attempts were blocked, proving that defenders are increasingly aware of this technique.

**Anonymisation (Lab 2):** Configuring Proxychains and TOR taught me the importance of operational security during active engagements. Understanding the difference between proxy chains and TOR—especially why `.onion` domains require full TOR routing—was a critical insight.

**Scanning & Enumeration (Lab 3):** Wireshark analysis of FIN and UDP scans deepened my understanding of how Nmap operates at the packet level. The passive ARP scan with `netdiscover -p` was a powerful lesson in stealth—sometimes the best reconnaissance is simply listening.

**Exploitation (Lab 4):** The Metasploit exercises showed me that not every vulnerability is a guaranteed win. BlueKeep failed because RDP wasn't exposed—a reminder that **enumeration must precede exploitation**. Successfully exploiting Tomcat and Apache Path Traversal, however, demonstrated the raw power of a well-chosen Metasploit module.

**Web App Pentesting (Lab 5):** DVWA was the most impactful lab. From cracking passwords via ZAP fuzzing to hijacking sessions via XSS and BeEF, I saw firsthand how a small input validation flaw can lead to full account takeover. The CSRF exercise was equally valuable—crafting a malicious URL that changes a user's password without their knowledge is a stark reminder of why session tokens alone are not enough.

**Overall:** This course reinforced that penetration testing is not about "hacking"—it's about **methodology, patience, and documentation**. Every finding must be reproducible, and every step must be justified. I'm now confident in my ability to conduct structured penetration tests and communicate findings to both technical and non-technical stakeholders.




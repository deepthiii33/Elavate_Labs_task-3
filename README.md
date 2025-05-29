# 🔍 Network Vulnerability Assessment - Internship Task

This repository contains the findings from a vulnerability assessment conducted during a one-day cybersecurity internship task. The primary focus was to identify **Critical** and **High** severity vulnerabilities using tools like **Nessus** across a local network.

---

## 🖥️ Targeted IP Addresses

| IP Address     | Role         | Vulnerability Types Found         |
|----------------|--------------|-----------------------------------|
| 192.168.1.6    | Kali Linux   | ✅ Critical, ✅ High               |
| 192.168.1.1    | Router       | ✅ Critical, ✅ High               |
| 192.168.1.2    | Other Device | ⚠️ Medium only (not deeply analyzed) |

---

## 🎯 Scope of Work

- ✅ Focused **only on Critical and High vulnerabilities**
- ❌ Skipped in-depth analysis of Medium, Low, and Informational issues due to time constraints
- 🔐 Avoided unnecessary exploitation – this is a passive analysis for reporting only

---

## 🔒 192.168.1.6 – Kali Linux (Local Machine)

**Critical Vulnerabilities:**
- **OpenSSH User Enumeration (CVE-2024-6387)**
- **Node.js < 18.20.1 / 20.12.1 / 21.7.2 RCE & HTTP/2 DoS (Multiple CVEs)**

**High Vulnerabilities:**
- Node.js < 18.20.4, 18.20.6
- Apache < 2.4.59
- cURL < 8.7.0, < 8.12.0
- Tornado Python Library < 6.5.0

📄 [Full Report →](report/192.168.1.6_critical_high.md)

---

## 🌐 192.168.1.1 – Router

**Critical Vulnerability:**
- **SSL 2.0/3.0 Supported – POODLE / downgrade attacks (CVE-2014-3566)**

**High Vulnerability:**
- **SWEET32 – 3DES medium strength cipher support**

📄 [Full Report →](report/192.168.1.1_critical_high.md)

---

## 🚫 Other Hosts (Optional Medium-Only Findings)

- 192.168.1.2 – 6 Medium vulnerabilities
- 192.168.1.1 – 6 Medium vulnerabilities
- 192.168.1.6 – 7 Medium vulnerabilities

These were **not explored in depth** due to project scope limitations.

---

## 📌 Final Notes

This repository provides a high-level vulnerability analysis report suitable for submission as part of a security internship task. The vulnerabilities documented here highlight key weaknesses that should be addressed through patching or configuration changes.

📄 [Final Summary →](report/final_summary.md)

---

## 🛠️ Tools Used

- 🧪 **Nessus Essentials**
- 🐧 Kali Linux
- 📄 Markdown & GitHub for documentation

---

## 🔐 Disclaimer

This assessment was conducted in a **controlled lab environment** on a **private internal network** with explicit permission. Publishing these results does not pose a risk to external systems.


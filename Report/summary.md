# 🔍 Vulnerability Summary Report (Internship Task)

This report summarizes the **Critical** and **High** vulnerabilities identified through internal scanning using **Nessus**, performed on select IPs from the local network.

>  **Scan Date:** 29/05/2025]  
>  **Tool Used:** Tenable Nessus  
>  **Scope:** Only IPs with Critical/High vulnerabilities — 192.168.1.6 & 192.168.1.1  
>  **Note:** Medium, Low, and Informational vulnerabilities were not included due to time constraints.

---

## 📌 Summary Table – Critical & High Vulnerabilities

| IP Address     | Severity  | Count | Key Vulnerabilities                                 |
|----------------|-----------|-------|-----------------------------------------------------|
| 192.168.1.6    | 🔐 Critical | 2     | Node.js Multiple CVEs, Apache HTTPD < 2.4.60        |
|                | ⚠️ High     | 7     | Node.js, Apache, Curl, Tornado vulnerabilities      |
| 192.168.1.1    | 🔐 Critical | 1     | SSL v2/v3 Protocol Enabled                          |
|                | ⚠️ High     | 1     | 3DES/SWEET32 Cipher Support                         |

---

## 🔐 Critical Vulnerabilities (2 Hosts)

### ✅ 192.168.1.6
- **Node.js < 18.19.1 / 20.11.1 / 21.6.2** – Multiple CVEs (DoS, RCE, Path Traversal)
- **Apache HTTPD < 2.4.60** – Multiple CVEs (DoS, SSRF, Auth Bypass)

### ✅ 192.168.1.1
- **SSL v2/v3 Protocol Support** – Deprecated protocols allow downgrade and MITM attacks

---

## ⚠️ High Vulnerabilities (2 Hosts)

### ✅ 192.168.1.6
- **Node.js < 18.20.6** – Memory leaks, Permission model bypass, Import override
- **Apache HTTPD < 2.4.59** – HTTP Response Splitting, HTTP/2 DoS
- **Curl < 8.12.0** – Memory leaks, Gzip decompression overflow
- **Tornado < 6.5.0** – Log flood DoS via multipart parsing

### ✅ 192.168.1.1
- **SSL 3DES Cipher Support** – SWEET32 vulnerability

---


## 🖥️ Host-wise Vulnerability Summary:

| IP Address  | Critical | High | Medium | Low | Info |
| ----------- | -------- | ---- | ------ | --- | ---- |
| 192.168.1.6 | 2        | 7    | 7      | 2   | 76   |
| 192.168.1.2 | 0        | 0    | 6      | 0   | 60   |
| 192.168.1.1 | 1        | 1    | 6      | 3   | 30   |
| 192.168.1.8 | 0        | 0    | 0      | 1   | 5    |
| 192.168.1.4 | 0        | 0    | 0      | 1   | 3    |

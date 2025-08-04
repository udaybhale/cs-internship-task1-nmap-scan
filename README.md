# 🛡️ Cybersecurity Internship – Task 1: Local Network Port Scanning

This repository documents **Task 1** of a Cybersecurity Internship: performing a local network scan using Nmap to identify open ports and assess potential risks. All information has been anonymized for public sharing and educational use.

---

## 🎯 Objective

> Discover active devices, open ports, and running services in a local network to assess security exposure.

---

## 🧰 Tools Used

- **Nmap** – For port scanning
- **Wireshark** *(optional)* – For traffic capture and packet-level analysis

---

## 📊 Scan Summary

- **Scan Range:** `192.168.1.0/24` (Private/test network)
- **Scan Method:** TCP SYN Scan (`-sS`)
- **Total IPs Scanned:** 256
- **Hosts Up:** 3
- **Scan Duration:** ~67 seconds

---

## 🔍 Detected Hosts & Services (Anonymized)

### 🖥️ Host: `192.168.1.1`
- **Open Port:**
  - `53/tcp` – DNS service

---

### 🖥️ Host: `192.168.1.50`
- **No open ports detected**
- All scanned ports returned reset (closed)

---

### 🖥️ Host: `192.168.1.100`
- **Open Ports:**
  - `135/tcp` – MSRPC (Windows RPC)
  - `139/tcp` – NetBIOS-SSN
  - `445/tcp` – Microsoft-DS (SMB)
  - `902/tcp` – ISS RealSecure (VMware)
  - `912/tcp` – Apex-Mesh (App/IoT-related)

---

## 🔍 Observations & Analysis

| Port | Service         | Description / Risk Example                       |
|------|------------------|--------------------------------------------------|
| 53   | DNS              | Misconfig can allow DNS-based attacks            |
| 135  | MSRPC            | Common in Windows, may expose services           |
| 139  | NetBIOS          | Legacy protocol, risky to expose                 |
| 445  | Microsoft-DS     | SMB, commonly exploited by ransomware            |
| 902  | ISS RealSecure   | VMware service, access may lead to VM misuse     |
| 912  | Apex-Mesh        | Could be IoT/app-based, requires investigation   |

---

## 🧠 Optional Next Steps

- Analyze packets with Wireshark while scanning
- Use `nmap -sV` for version detection
- Use `nmap --script vuln` to identify known vulnerabilities

---

## 📂 Repository Contents


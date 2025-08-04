# 📘 Port Scanning FAQ – Cybersecurity Internship Task 1

This document answers common questions related to port scanning, Nmap usage, and network security as part of the internship task.

---

### ❓ 1. What is an open port?

An **open port** is a network port on a system that is actively accepting connections. It indicates a service (like HTTP, SSH, FTP) is listening for incoming requests.

---

### ❓ 2. How does Nmap perform a TCP SYN scan?

Nmap sends a **SYN packet** to the target port:

- If it receives **SYN-ACK**, the port is **open**
- If it receives **RST**, the port is **closed**
- If no response, the port is **filtered**

This method is also called a **half-open scan**, as it doesn’t complete the full TCP handshake.

---

### ❓ 3. What risks are associated with open ports?

Open ports can:

- Expose outdated or vulnerable services
- Be targeted for **unauthorized access**
- Enable **DDoS** or **brute-force attacks**
- Leak system info about services and devices

---

### ❓ 4. Explain the difference between TCP and UDP scanning.

| Feature            | TCP Scanning                | UDP Scanning                   |
|-------------------|-----------------------------|--------------------------------|
| Protocol           | Connection-based            | Connectionless                 |
| Accuracy           | High                        | Lower, due to silent drops     |
| Detection          | Easy to detect/log          | Harder to detect               |
| Use Cases          | Web, SSH, FTP, SMB, etc.    | DNS, SNMP, NTP, etc.           |

---

### ❓ 5. How can open ports be secured?

- Close unused ports
- Use **firewalls** to control access
- Enable **authentication and encryption**
- Patch services regularly
- Use techniques like **port knocking** or **VPNs**

---

### ❓ 6. What is a firewall’s role regarding ports?

A **firewall** filters traffic based on port, protocol, or IP:

- Blocks unwanted connections
- Protects internal services
- Logs or drops suspicious attempts
- Enforces access rules per port

---

### ❓ 7. What is a port scan and why do attackers perform it?

A **port scan** probes a host to identify:

- Open and closed ports
- Running services and versions
- Security weaknesses

Attackers use port scanning in **reconnaissance** to find exploitable services.

---

### ❓ 8. How does Wireshark complement port scanning?

**Wireshark** analyzes real-time network traffic:

- Verifies packet flow from tools like Nmap
- Detects handshake attempts, SYN/ACK flags
- Highlights abnormal or malicious traffic
- Useful in validating and troubleshooting scans

---

🛑 **Note:** Always perform port scanning in **authorized and ethical environments only**.


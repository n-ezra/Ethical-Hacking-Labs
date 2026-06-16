# 📡 TCP SYN Scan (-sS) – Nmap Stealth Scan Analysis Report

## 🔍 Executive Summary

This report documents a **TCP SYN Scan (`-sS`)** performed using Nmap against the target **192.168.56.1**.

The SYN scan is a **stealth scanning technique** that sends SYN packets without completing the full TCP handshake. The scan results indicate that all ports are **filtered**, suggesting strong firewall or packet filtering mechanisms.

---

## 🎯 Objectives

* Perform stealth-based TCP port scanning
* Identify port states (open, closed, filtered)
* Evaluate network security posture
* Document findings in a professional format

---

## ⚙️ Scan Configuration

### 🔧 Command Used

```bash
sudo nmap -sS 192.168.56.1
```

---

## 🧠 Command Explanation

| Parameter      | Description                               |
| -------------- | ----------------------------------------- |
| `sudo`         | Required for SYN scan (raw socket access) |
| `nmap`         | Network scanning and reconnaissance tool  |
| `-sS`          | TCP SYN Scan (Half-Open / Stealth Scan)   |
| `192.168.56.1` | Target IP address                         |

---

## 🔬 Scan Methodology

TCP SYN Scan works using a **half-open connection**:

1. SYN → Sent to target
2. SYN-ACK ← Received → Port is **OPEN**
3. RST → Sent by scanner (connection terminated)

👉 If RST received → **Port is CLOSED**
👉 If no response → **Port is FILTERED**

---

## 📊 Scan Results

```bash
Starting Nmap 7.95 ( https://nmap.org )
Nmap scan report for 192.168.56.1
Host is up (0.032s latency).
All 1000 scanned ports on 192.168.56.1 are in ignored states.
Not shown: 1000 filtered tcp ports (no-response)
Nmap done: 1 IP address (1 host up) scanned in 16.34 seconds
```

---

## 📈 Result Analysis

### ✅ Host Status

* Target system is **UP and reachable**
* Observed latency: **~0.032 seconds** (faster response compared to TCP Connect Scan)

### 🚫 Port Status Summary

* Total Ports Scanned: **1000**
* Open Ports: **0**
* Closed Ports: **0**
* Filtered Ports: **1000**

---

## 🛡️ Security Interpretation

The scan results strongly indicate:

* Presence of a **firewall or filtering mechanism**
* All incoming SYN probes are being **blocked or dropped**
* No direct service exposure is visible

### Possible Security Controls:

* Network Firewall
* Host-based Firewall
* IDS/IPS systems
* Access Control Lists (ACLs)

---

## ❗ Understanding "Filtered" State

A port is marked as **filtered** when:

* No response is received from the target
* Scanner cannot determine if the port is open or closed

### Common Causes:

* Firewall rules blocking packets
* Silent packet dropping
* Network-level filtering

---

## ⚠️ Key Observations

* SYN scan completed **faster (16.34s)** compared to TCP Connect Scan
* No ports responded → strong filtering in place
* Indicates a **hardened network environment**

---

## ⚖️ Advantages of SYN Scan

* Fast and efficient
* Stealthier than TCP Connect Scan
* Does not complete full handshake
* Widely used in penetration testing

---

## ❌ Disadvantages

* Requires root privileges
* May still be detected by advanced security systems
* Cannot bypass strong firewall filtering

---

## 📸 Screenshot Evidence

<img width="520" height="165" alt="image" src="https://github.com/user-attachments/assets/8bddf8c8-4432-49b4-ac48-7d1a1e34aa14" />


### 📌 Screenshot Guidelines:

* Include both command and output
* Ensure readability
* Avoid cropping important data


---

## 🎯 Conclusion

The TCP SYN Scan revealed that **all scanned ports are filtered**, indicating a **secure and restricted network environment**. The absence of open ports suggests that security mechanisms are actively blocking incoming traffic.

Further enumeration techniques and advanced scanning methods are required to identify hidden services or bypass filtering controls.

---

## 💡 Key Takeaway

> A fully filtered SYN scan result reflects strong defensive security controls, requiring deeper and more advanced reconnaissance techniques.

---


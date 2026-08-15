# 📡 Capture and Analyze Network Traffic Using Wireshark

## 📌 Task 5 — Network Traffic Capture and Analysis

**Cyber Security Internship**

This project demonstrates how to capture live network traffic using **Wireshark** and analyze captured packets to identify different network protocols and understand basic network communication.

The lab was performed on **Kali Linux**, where Wireshark was installed and an active network interface was selected for packet capture. Traffic was generated using commands such as `ping`, `nslookup`, and `curl`, and the resulting packets were analyzed using Wireshark protocol filters.

---

## 🎯 Objective

To capture live network traffic using Wireshark, analyze the captured packets, and identify different network protocols such as **DNS, TCP, and ICMP**. The task develops practical skills in packet capture, protocol filtering, packet analysis, and understanding basic network communication.

---

## 🛠️ Tools Used

* **Kali Linux**
* **Wireshark**
* **Ping**
* **NSLookup**
* **cURL**

---

## 🔧 Lab Setup

| Component         | Purpose                           |
| ----------------- | --------------------------------- |
| Kali Linux        | Operating system used for the lab |
| Wireshark         | Packet capture and analysis       |
| Network Interface | Source of live network traffic    |
| Ping              | Generated ICMP traffic            |
| NSLookup          | Generated DNS queries             |
| cURL              | Generated HTTP traffic            |

---

## 🚀 Procedure

### 1. Install Wireshark

Wireshark was installed using the Kali Linux terminal:

```bash
sudo apt update
sudo apt install wireshark -y
```

During installation, the option to allow non-superusers to capture packets was enabled. The user was then added to the Wireshark group:

```bash
sudo usermod -aG wireshark $USER
```

---

### 2. Identify the Active Network Interface

The available network interfaces were checked using:

```bash
ip a
```

The interface containing an active IP address was selected for packet capture. Examples include:

```text
eth0
wlan0
enp0s3
```

The report used the active `eth0` interface for capturing traffic.

---

### 3. Launch Wireshark

Wireshark was launched from the Kali Linux terminal:

```bash
wireshark
```

The active network interface was then selected from the Wireshark start screen.

---

### 4. Start Packet Capture

The active network interface was selected and the capture was started by double-clicking the interface.

Wireshark began displaying live packets and network traffic in real time.

---

### 5. Generate Network Traffic

While Wireshark was capturing packets, network traffic was generated from a separate terminal.

#### ICMP Traffic

```bash
ping -c 5 google.com
```

#### DNS Traffic

```bash
nslookup google.com
```

#### HTTP Traffic

```bash
curl http://example.com
```

These commands generated different types of traffic that could be observed and analyzed in Wireshark.

---

## 🔍 Protocol Analysis

After capturing traffic, Wireshark's display filters were used to identify individual protocols.

### DNS

Filter:

```text
dns
```

DNS packets were examined to observe domain-name queries and responses.

The capture contained DNS traffic generated during normal network activity and the `nslookup` command.

---

### HTTP

Filter:

```text
http
```

HTTP packets were examined to identify HTTP requests and responses generated using:

```bash
curl http://example.com
```

The Wireshark capture showed HTTP communication between the local system and the remote web server.

---

### TCP

Filter:

```text
tcp
```

TCP packets were analyzed to observe transport-layer communication, including TCP connection activity and packet exchanges.

The capture contained TCP traffic associated with the network connections generated during the experiment.

---

### ICMP

Filter:

```text
icmp
```

The `ping` command generated ICMP Echo Request and Echo Reply packets.

Example:

```bash
ping -c 5 google.com
```

These packets were analyzed in Wireshark to observe basic network connectivity testing.

The report includes screenshots showing DNS, HTTP, TCP, and ICMP traffic captured during the experiment.

---

## 📊 Protocols Identified

| Protocol | Purpose                          | Traffic Generated/Observed |
| -------- | -------------------------------- | -------------------------- |
| **DNS**  | Resolves domain names            | `nslookup google.com`      |
| **HTTP** | Transfers web content            | `curl http://example.com`  |
| **TCP**  | Reliable transport communication | Web/network connections    |
| **ICMP** | Network connectivity testing     | `ping -c 5 google.com`     |

---

## 📦 Packet Information Analyzed

During packet analysis, the following information was examined:

* Source IP address
* Destination IP address
* Protocol
* Source and destination ports
* Packet length
* Packet information
* TCP packet details
* ICMP Echo Requests and Replies
* DNS queries and responses
* HTTP requests and responses

These details helped demonstrate how different protocols are used for communication across a network.

---

## 💾 Export Packet Capture

After completing the analysis, the captured traffic was exported as a `.pcap` file.

In Wireshark:

**File → Save As → `capture.pcap`**

The saved PCAP file can be reopened in Wireshark for further analysis.

Example filename:

```text
task5-wireshark-capture.pcap
```

---

## 📸 Evidence

The project report contains screenshots demonstrating:

1. Wireshark installation
2. Active network interface identification
3. Wireshark launch
4. Packet capture
5. Network traffic generation
6. DNS packet analysis
7. HTTP packet analysis
8. TCP packet analysis
9. ICMP packet analysis
10. `.pcap` file export

---

## 🧠 Key Learning Outcomes

Through this task, the following practical skills were developed:

* Installing and configuring Wireshark
* Selecting an active network interface
* Capturing live network packets
* Generating network traffic
* Filtering packets by protocol
* Identifying DNS, HTTP, TCP, and ICMP traffic
* Examining packet-level information
* Understanding basic network communication
* Saving packet captures in `.pcap` format

---

## 📝 Summary

Wireshark was used to capture and analyze live network traffic. Protocol-based filters were applied to identify **DNS, HTTP, TCP, and ICMP** traffic. Packet details including source and destination addresses, protocols, ports, and packet information were examined to understand how data travels across a network.

The captured traffic was saved as a **`.pcap` file** for further analysis and documentation. Overall, the task provided practical experience in network packet capture, protocol identification, and basic traffic analysis.

---

## 👨‍💻 Author

**VIPIN KUMAR**

**Cyber Security Internship**

**Task 5 — Capture and Analyze Network Traffic Using Wireshark**

**Date:** 30-07-2026

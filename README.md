# Elevenlabs-Cybersecurity-intern
Task  1: Open your local network for open ports
You can add the following to your GitHub repository README:

# Network Port Scanning using Nmap

## Objective

The objective of this task is to discover open ports on devices within a local network and understand potential network exposure and security risks.

## Tools Used

* Nmap
* Wireshark (Optional)
* Windows Command Prompt

## Procedure

### 1. Identify Local Network Range

The local IP address and subnet information were obtained using:

```bash
ipconfig
```

Based on the IPv4 address, the local network range was identified (e.g., `192.168.1.0/24`).

### 2. Perform Network Scan

A TCP SYN scan was conducted using Nmap to identify active hosts and open ports:

```bash
nmap -sS 192.168.1.0/24
```

### 3. Save Scan Results

The scan results were saved for documentation and analysis:

```bash
nmap -sS 192.168.1.0/24 -oN scan_results.txt
```

### 4. Analyze Open Ports

Discovered open ports were mapped to their corresponding services to understand their purpose and potential security implications.

### 5. Optional Packet Analysis

Wireshark was used to capture and analyze network traffic generated during the scan, including SYN, SYN-ACK, and RST packets.

## Common Ports Observed

| Port | Service | Description                  |
| ---- | ------- | ---------------------------- |
| 22   | SSH     | Secure remote administration |
| 80   | HTTP    | Web server communication     |
| 443  | HTTPS   | Secure web communication     |
| 53   | DNS     | Domain Name System           |
| 445  | SMB     | Windows file sharing         |
| 3389 | RDP     | Remote Desktop Protocol      |

## Security Risks Identified

* Unnecessary open ports may increase the attack surface.
* Exposed SSH or RDP services can be targeted by brute-force attacks.
* HTTP services transmit data without encryption.
* SMB services may expose file-sharing vulnerabilities if not properly secured.

## Recommendations

* Disable unused services and ports.
* Use strong authentication mechanisms.
* Enable firewalls to restrict access.
* Prefer encrypted protocols such as HTTPS and SSH.
* Regularly monitor and audit network services.

## Learning Outcomes

* Learned how to identify devices on a local network.
* Gained experience using Nmap for port scanning.
* Understood the relationship between ports and network services.
* Analyzed potential security risks associated with open ports.
* Explored packet-level network analysis using Wireshark.

## Disclaimer
This scan was performed only on authorized devices within a controlled environment for educational and security assessment purposes. Unauthorized scanning of networks or systems may violate organizational policies and legal regulations.
This scan was performed only on authorized devices within a controlled environment for educational and security assessment purposes. Unauthorized scanning of networks or systems may violate organizational policies and legal regulations.

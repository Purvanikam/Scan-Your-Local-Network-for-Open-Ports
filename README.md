#Local Network Open Ports Scan Report

Date of Scan: [04/08/2025]


Tools Used: Nmap (planned), Wireshark (optional)


Objective: Discover open ports on devices in the local network to understand network exposure.
1. Scan Preparation
Nmap Installation:


 Download from nmap.org and follow installation instructions for your OS.

Find Local IP Range:


 Use ipconfig (Windows) or ifconfig/ip a (Linux/macOS) to determine the subnet, e.g., 192.168.1.0/24.

2. Scan Execution
Command Used: nmap -sS 192.168.1.0/24 
Performs a TCP SYN scan on all devices in the subnet.
Optional Packet Capture:


 Use Wireshark to capture and analyze network traffic during the scan.

3. Scan Results
| IP Address     | Open Ports       | Common Services    |
|----------------|------------------|--------------------|
| 192.168.1.10   | 22, 80           | SSH, HTTP          |
| 192.168.1.15   | 445              | SMB                |
| 192.168.1.20   | 80, 443          | HTTP, HTTPS        |
| ...            | ...              | ...                |

4. Service Analysis
| Port | Service | Description                   | Security Risk                 |
|------|---------|-------------------------------|-------------------------------|
| 22   | SSH     | Secure remote login           | Brute-force attacks possible  |
| 80   | HTTP    | Web server                    | Vulnerable to exploits        |
| 443  | HTTPS   | Secure web server             | SSL/TLS weaknesses possible   |
| 445  | SMB     | Windows file sharing          | Ransomware,unauthorized access|

5. Security Risks Identified
Unnecessary Open Ports: Devices with open ports/services not required for daily operation increase attack surface.
Default Credentials: Services like SSH or SMB may be vulnerable if default or weak credentials are used.
Old Firmware/Software: Known vulnerabilities in outdated systems may be exploited if ports are open.

6. Recommendations
Close Unused Services/Ports: Restrict unnecessary network exposure.
Update Devices: Regularly update firmware and software.
Monitor Network Traffic: Use Wireshark or similar tools for ongoing monitoring.
Strong Authentication: Use strong passwords and, where possible, key-based authentication.

7. References
Nmap Documentation
Wireshark Documentation
IANA Port Registry

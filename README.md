# Scan-Your-Local-Network-for-Open-Ports
# Scan Your Local Network for Open Ports

## Objective
Learn to discover open ports on devices in your local network to understand network exposure.

## Tools Needed
- Nmap (free)
- Wireshark (optional)
- Mobile alternatives: Fing (Android/iOS), Network Analyzer (iOS)

## Steps
1. Install Nmap from the official website.
2. Find your local IP range (e.g., 192.168.1.0/24).
3. Run: `nmap -sS 192.168.1.0/24` to perform a TCP SYN scan.
4. Note down IP addresses and open ports found.
5. (Optional) Analyze packet capture with Wireshark.
6. Research common services running on those ports.
7. Identify potential security risks from open ports.
8. Save scan results as a text or HTML file.

## Outcome
- Basic network reconnaissance skills
- Understanding network service exposure

## Disclaimer
**Only scan networks you own or have permission to scan. Unauthorized scanning may be illegal.**

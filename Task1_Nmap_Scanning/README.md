# Task 1 - Basic Network Scanning with Nmap

## Objective
Perform a network scan using Nmap to identify open ports and services.

## Tool Used
- Nmap

## Commands Used

### Basic Scan
```bash
nmap 127.0.0.1
```

### Service Detection Scan
```bash
nmap -sV 127.0.0.1
```

## Findings

| Port | Service | Significance |
|------|----------|--------------|
| 135 | msrpc | Microsoft Remote Procedure Call |
| 139 | netbios-ssn | Windows File Sharing |
| 445 | microsoft-ds | SMB Service |

## Conclusion
This task helped in understanding basic network scanning and identifying open ports/services using Nmap.

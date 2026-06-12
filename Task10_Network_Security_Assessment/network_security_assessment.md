# Network Security Assessment Report

## Objective

The objective of this assessment was to analyze a local network using Nmap and Wireshark, identify active services, observe network traffic, and evaluate potential security risks.

---

## Tools Used

- Nmap
- Wireshark
- Windows 11

---

## Network Scanning Results

A network scan was performed using Nmap on the local machine.

### Findings

| Port | Service | Status |
|--------|---------|---------|
| 135 | MSRPC | Open |
| 139 | NetBIOS | Open |
| 445 | SMB | Open |

*(Modify according to your actual Nmap output.)*

### Security Analysis

- Open ports increase the attack surface.
- SMB services may be targeted if not properly secured.
- Unnecessary services should be disabled.

---

## Network Traffic Analysis

Network traffic was captured using Wireshark.

### Observed Traffic

- HTTP requests
- DNS queries
- TCP communication

### Security Analysis

- HTTP traffic is unencrypted and can be intercepted.
- DNS traffic may reveal browsing activity.
- Sensitive communications should use encrypted protocols such as HTTPS.

---

## Identified Risks

1. Open network ports.
2. Exposure of unencrypted HTTP traffic.
3. Potential information disclosure through network services.

---

## Recommendations

1. Close unused ports.
2. Use HTTPS instead of HTTP.
3. Keep operating systems and applications updated.
4. Enable firewall protection.
5. Monitor network traffic regularly.

---

## Conclusion

The assessment demonstrated the use of Nmap and Wireshark for identifying active services and analyzing network communications. Proper network hardening and continuous monitoring can significantly improve security.

# Task 7: Vulnerability Scanning with Nikto

## Objective

To perform a vulnerability assessment on a web application using Nikto and identify potential security weaknesses.

## Tool Used

- Nikto v2.6.0
- DVWA (Damn Vulnerable Web Application)
- XAMPP Apache Server
- Windows 11

## Target

- DVWA hosted locally at https://localhost/dvwa

## Scan Command

```bash
perl nikto.pl -h localhost -ssl -root /dvwa
```

## Findings

### 1. Cookies Missing Secure Flag

Nikto detected that application cookies were created without the Secure attribute.

### 2. Missing Security Headers

The following security headers were missing:

- Content-Security-Policy
- Strict-Transport-Security
- Permissions-Policy
- Referrer-Policy
- X-Content-Type-Options

### 3. Outdated Software Versions

The scan identified outdated versions of:

- Apache 2.4.58
- OpenSSL 3.1.3
- PHP 8.2.12

### 4. HTTP TRACE Method Enabled

The HTTP TRACE method was enabled, potentially exposing the application to Cross Site Tracing (XST) attacks.

### 5. Directory Indexing Enabled

Directory listing was enabled on several DVWA directories including:

- /config/
- /tests/
- /database/
- /docs/

### 6. Configuration Information Exposure

Nikto reported that configuration-related information may be accessible remotely.

## Conclusion

The Nikto scan successfully identified multiple security weaknesses within the DVWA environment. The findings demonstrate common web application security issues including insecure cookie settings, missing security headers, outdated software versions, directory indexing, and configuration exposure. Regular vulnerability scanning helps organizations identify and remediate security risks before they can be exploited.

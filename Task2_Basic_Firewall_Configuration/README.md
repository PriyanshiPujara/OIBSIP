# Task 2: Basic Firewall Configuration with UFW

## Objective

The objective of this task was to configure a basic firewall using UFW (Uncomplicated Firewall) on a Linux system and verify the configured rules.

## Tools Used

- Ubuntu (WSL)
- UFW (Uncomplicated Firewall)

## Commands Used

```bash
sudo apt update
sudo apt install ufw -y
sudo ufw allow ssh
sudo ufw deny 80
sudo ufw enable
sudo ufw status
```

## Configuration Performed

1. Installed UFW on Ubuntu.
2. Allowed SSH traffic on port 22.
3. Blocked HTTP traffic on port 80.
4. Enabled the firewall.
5. Verified firewall rules using the status command.

## Verification

The firewall status confirmed:

- SSH (Port 22) → ALLOW
- HTTP (Port 80) → DENY
- Firewall Status → ACTIVE

## Conclusion

The firewall was successfully configured using UFW. SSH access was allowed while HTTP traffic was blocked, demonstrating basic firewall management on a Linux system.

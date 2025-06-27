
# Basic Firewall Configuration on Linux and Windows

This repository documents the setup and testing of basic firewall rules on *Kali Linux* using UFW and Windows using PowerShell. It includes rule configuration, screenshots, and configuration summaries.

## Objectives

- Enable and configure UFW on Kali Linux.
- Add allow/deny rules for common ports.
- Use PowerShell to manage Windows Firewall rules.
- Validate rules via command-line output and screenshots.
- Provide documentation and configuration references.

## Kali Linux (UFW)

### UFW Commands

bash
sudo apt update
sudo apt install ufw -y
sudo ufw enable
sudo ufw allow ssh
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw status verbose

Screenshot

See Elabs-Task4.txt

Summary (main.txt)
Linux UFW:
- Allowed: SSH, HTTP, HTTPS
- Default: Incoming Denied, Outgoing Allowed

How to Use
1. Clone this repository.
2. Run the provided commands on your test systems.
3. Review screenshots and logs.
4. Modify or extend rules as needed.

Notes
Always test firewall rules in a safe, isolated environment.
Make sure you do not block SSH access if working remotely on Linux.


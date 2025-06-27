 README.md

#  Firewall Setup on Linux & Windows

##  Objective

Configure and test basic firewall rules to allow or block traffic using UFW (Linux) and Windows Firewall.


## Tools Used

- *Linux (Kali)*: UFW (Uncomplicated Firewall)
- *Windows 10/11*: PowerShell & GUI (Windows Defender Firewall)

##  Steps Performed

### 1️ Enable the Firewall

#### Linux:
bash
sudo ufw enable

Windows:
Open wf.msc or use New-NetFirewallRule in PowerShell.

List Existing Rules

Linux:

sudo ufw status verbose

Windows:

Get-NetFirewallRule


Block Port 23 (Telnet)

Linux:

sudo ufw deny 23/tcp

Windows:

New-NetFirewallRule -DisplayName "Block Telnet" -Direction Inbound -Protocol TCP -LocalPort 23 -Action Block


Test the Rule

Use telnet localhost 23 or Test-NetConnection

Expected result: Connection refused or timeout


Allow SSH (Linux)

sudo ufw allow ssh


Remove Test Rule

Linux:

sudo ufw delete deny 23/tcp

Windows:

Remove-NetFirewallRule -DisplayName "Block Telnet"

How Firewalls Filter Traffic

Firewalls use rules based on:

Protocol (TCP/UDP)

Port (e.g., 22, 23, 80)

Direction (Inbound/Outbound)

They allow or deny traffic to protect systems from unauthorized access.

Deliverables

main: Command history

README.md: Documentation

screenshots/: Folder containing ufw_status.png, windows_rule.png

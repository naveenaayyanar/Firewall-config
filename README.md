🔐 Task 4: Setup and Use a Firewall (Linux + Windows)

📝 Objective
Configure and test basic firewall rules to allow or block network traffic using:
- UFW (Uncomplicated Firewall) on Linux
- Windows Defender Firewall on Windows

The goal is to demonstrate basic firewall configuration, test blocking and allowing specific ports, and understand how firewalls filter traffic.

🧪 Task Summary

🔧 Actions Performed on Both Systems:
1. Listed current firewall rules
2. Blocked inbound traffic on port 23 (Telnet)
3. Verified the block by attempting a Telnet connection
4. Allowed SSH (port 22) on Linux
5. Removed the block rule to restore original state
6. Documented steps and behavior
7. Captured relevant screenshots


🖥️ Windows Firewall Steps

Tools Used:
- Windows Defender Firewall with Advanced Security

GUI Steps:
1. Open "Windows Defender Firewall with Advanced Security"
2. Click Inbound Rules
3. Click New Rule
   - Rule Type: Port
   - Port: TCP 23
   - Action: Block the connection
   - Profile: All
   - Name: `Block Telnet (Port 23)`
4. Attempted Telnet to localhost → Connection failed (as expected)
5. Created another rule to allow port 22 (optional)
6. Deleted the block rule to restore settings

🐧 Linux (UFW) Steps

Tools Used:
- Terminal
- UFW (frontend for iptables)

Commands Used:
```bash
sudo apt update
sudo apt install ufw
sudo ufw enable
sudo ufw status
sudo ufw deny 23/tcp
telnet localhost 23
sudo ufw allow 22/tcp
sudo ufw delete deny 23/tcp

 🔥 Task 4: Setup and Use a Firewall (Windows)

 🎯 Objective

Configure and test basic firewall rules to allow or block traffic using Windows Defender Firewall.



 🛠 Tools Used

- Windows 10 with Windows Defender Firewall
- Telnet Client (optional, for testing)



 📝 Steps Performed

 ✅ 1. Open Windows Firewall (Advanced)
- Press `Win + R` → type `wf.msc` → press Enter
- This opens Windows Defender Firewall with Advanced Security

 ✅ 2. List Existing Inbound Rules
- In the left panel, click Inbound Rules
- Existing rules for system and third-party applications are shown

 ✅ 3. Add Rule to Block Telnet (Port 23)
- In Inbound Rules → click New Rule
- Choose Port, then TCP, specific port `23`
- Action: Block the connection
- Profile: Domain, Private, Public
- Name: `Block Telnet (Port 23)`

 ✅ 4. Test Rule (Optional)
- Enabled Telnet Client via:
  - `Control Panel > Programs > Turn Windows features on or off > Check Telnet Client`
- Ran: `telnet localhost 23` in Command Prompt
- Result: Connection failed as expected

 ✅ 5. Add Rule to Allow SSH (Port 22)
- Created another Inbound Rule
- Port: TCP 22
- Action: Allow the connection
- Name: `Allow SSH (Port 22)`

 ✅ 6. Remove the Telnet Block Rule
- Returned to Inbound Rules
- Located `Block Telnet (Port 23)` → Right-click → Delete



 🔍 How Firewalls Filter Traffic

A firewall acts as a barrier between trusted and untrusted networks. It filters traffic based on:
- Inbound/Outbound rules
- IP addresses
- Ports and protocols
- Application-level permissions

 Example:
- Blocked TCP port 23 to prevent Telnet connections
- Allowed TCP port 22 to permit SSH access

This controls which services are reachable from outside and protects the system from unauthorized access.


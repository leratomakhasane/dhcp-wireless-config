# dhcp-wireless-config
A Cisco Packet Tracer lab showing how to configure DHCP on a wireless router to automatically assign IPs to multiple clients. Demonstrates skills in IP addressing, DHCP setup, router management, and connectivity testing—key for network administration, SOC analysis, and cybersecurity roles.

## 📌 Objective
To configure a wireless router in CISCO Packet Tracer to automatically assign IP addressess to multiple connected PCs using DHCP. This project demonstrates understanding of **network topology setup**, **DHCP configuration**, **IP addressing**, and **connectivity verification**.
- Connect 3 PCs to a wireless router
- Change the DHCP setting to a specific network range
- Configure the clients to obtain their address via DHCP
<br>

## 🧠 Skills Learned
- Configuring DHCP on a wireless router
- Understanding IP addressing and default gateways
- Setting and modifying DHCP ranges and scopes
- Connecting end devices in a small LAN topology
- Verifying IP configurations using `ipconfig` and `ping`
- Network troubleshooting in CISCO Packet Tracer
<br>

## 🛠 Tools Used
- CISCO Packet Tracer (network simulation)
- Command prompt (network testing)
- Web browser router GUI (router setup and DHCP configuration)
<br>

## 🔎 Steps Performed
Scenario
A home user wants to use a wireless router to connect 3 PCs. All 3 PCs should obtain their address automatically from the wireless router.

**Part 1: Setting up the network topology**
1. Add three generic PCs
2. Connect each PC to an Ethernet port to the wireless router using straight-through cables.
![A screenshot of 3 PCs connected to a wireless router](images/part1.png "A picture of 3 PCs conneted to a wireless router")
<br>

**Part 2: Observe the default DHCP settings**
1. After the amber lights have turned green, click **PC0**. Click the **Desktop** tab. Select **IP Configuration**. Select **DHCP** to receive an IP address from **DHCP Enabled Router**.
![A screenshot of PC0 IP configuration](images/part2a.png "A picture of the IP Configuration of PC0")
Record the IP address of the default gateway
`192.168.0.1`


2. Close the IP Configuration window.
3. Open a Web Browser.
4. Enter the IP address of the default gateway recorded earlier into the URL field. When prompted, enter the username admin and password admin.
![A screenshot of the browser showing the default gateway web page](images/part2d.png "A picture of the IP address default gateway in the URL field")
![A screenshot of the login page for the default gateway web page](images/part2da.png "A picture of the login page")
5. Scroll through the Basic Setup page to view default settings, including the default IP address of the wireless router.
![A screenshot of the basic setup of the default gateway](images/part2e.png "A picture of the default gateway defaults settings")
6. Notice that DHCP is enabled, the starting address of the DHCP range and the range of addresses available to clients.
<br>
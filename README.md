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


2. Close the **IP Configuration** window.
3. Open a Web Browser.
4. Enter the IP address of the default gateway recorded earlier into the URL field. When prompted, enter the username **admin** and password **admin**.
![A screenshot of the login page for the default gateway web page](images/part2da.png "A picture of the login page")
![A screenshot of the browser showing the default gateway web page](images/part2d.png "A picture of the IP address default gateway in the URL field")

5. Scroll through the Basic Setup page to view default settings, including the default IP address of the wireless router.
![A screenshot of the basic setup of the default gateway](images/part2e.png "A picture of the default gateway defaults settings")
6. Notice that DHCP is enabled, the starting address of the DHCP range and the range of addresses available to clients.
<br>


**Part 3: Change the default IP address of the wireless router**
1. Within the Router IP Settings section, change the IP address to: **192.168.5.1**.
![A screenshot of the changed IP Address](images/part3a.png "A picture of the dchanged IP address")
2. Scroll to the bottom of the page and click **Save Settings**.
3. If it is done correctly, the web page will display an error message. Close the web browser.
4. Click **IP Configuration** to renew the assigned IP address. Click **Static**. Click **DHCP** to receive new IP address information from the wireless router.
![A screenshot of the changing from static IP addressing to DCHP IP addressing](images/part3d.png "A picture of changing the IP address from static to DCHP")
5. Open the web browser, enter the IP address **192.168.5.1** in the URL field. When prompted, enter the username **admin** and password **admin**.
![A screenshot of the IP address asking for login details](images/part3e.png "A picture of the new IP address webpage assinged to the laptop")
<br>



**Part 4: Change the default DHCP range of addresses.**
1. Notice the DHCP Server Start IP Address is updated to the same network as the Router IP.
![A screenshot of the updated IP address](images/part4a.png "A picture of the updated IP address")
2. Change the Starting IP Address from 192.168.5.100 to **192.168.5.126**.
![A screenshot of changing the IP address](images/part4b.png "A picture of changing the IP address")
3. Change the Maximum Number of Users to **75**.
![A screenshot of changing the maximum number of users](images/part4c.png "A picture of changing the maximum number of users")
4. Scroll to the bottom of the page and click **Save Settings**. Close the web browser.
5. Click **IP Configuration** to renew the assigned IP address. Click **Static**. Click **DHCP** to receive new IP address information from the wireless router.
Select Command Prompt. Enter ipconfig.
`192.168.5.126`
![A screenshot of the ipconfig](images/part4e.png "A picture of the ipconfig")
6. Select **Command Prompt**. Enter **ipconfig**.
![A screenshot of the command prompt](images/part4f.png "A picture of the command prompt")
Record the IP address for PC0:
`192.168.5.126`
<br>


**Part 5: Enable DHCP on the other PCs.**
1. Click **PC1**.
2. Select **Desktop** tab.
![A screenshot of PC1 and the desktop tab](images/part5a+b.png "A picture of PC1 and the desktop tab")
3. Select IP Configuration.
![A screenshot of PC1 and the IP Configuration](images/part5c.png "A picture of PC1 and the IP Configuration")
4. Click **DHCP**.
![A screenshot of the DHCP](images/part5d.png "A picture of the DHCP")
Record the IP address for PC1
`192.168.5.127`
5. Close the configuration window.
6. Enable DHCP on PC2 following the steps for PC1.
![A screenshot of DHCP being enabled on PC2](images/part5f.png "A picture of DHCP being enabled on PC2")
<br>


**Part 6: Verify connectivity**
1. Click **PC2** and select the **Desktop** tab.
![A screenshot of PC2 and the Desktop tab](images/part6a.png "A picture of PC2 and the desktop tab")
2. Select Command Prompt.
3. Enter **ipconfig** at the prompt to view the IP configuration.
![A screenshot of the command prompt and the ipconfig command](images/part6b+c.png "A picture of the command prompt and the ipconfig command")
4. At the prompt, enter **ping 192.168.5.1** to ping the wireless router.
![A screenshot of the command ping for the wireless router](images/part6d.png "A picture of the ping command for the wireless router")
5. At the prompt, enter **ping 192.168.5.127** to ping PC1.
![A screenshot of the command ping for PC1](images/part6e.png "A picture of the command ping for PC1")
6. The pings to all devices should be successful.
<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this project, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1 / Create Window & Linux Virtual machines
- Step 2 / Ensure both VMs are in the same Virtual Network / Subnet
- Step 3 / Using wireshark, observe and screen for ICMP Traffic only
- Step 4 / Retrieve the private IP address of the Ubuntu VM (linux-vm) and attempt to ping it from within the Windows 10 VM
- Step 5 / From The Windows 10 VM, open command line or PowerShell and attempt to ping a public website (such as www.google.com) and observe the traffic in WireShark
- Step 6 / Configuring a Firewall [Network Security Group] (disable ICMP and SSH traffic)
- Step 7 / Open the Network Security Group the Ubuntu VM is using and disable incoming (inbound) ICMP traffic
- Step 8 / Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity
- Step 9 / Re-enable ICMP traffic for the Network Security Group your Ubuntu VM is on
- Step 10 / Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity (should start working)



<h2>Actions and Observations</h2>

<p>
  
![wiresharkping](https://github.com/user-attachments/assets/fe0d6592-cd64-4083-b774-a5f21a4bc692)

</p>
<p>
Ping from windows Pc host to Linux host. screening to ICMP traffic on wireshark.
</p>
<br />

<p>
  
![wiresharkpinggoogle](https://github.com/user-attachments/assets/282a5b5b-8bbc-43f6-86d8-cb029e36fbfa)

</p>
<p>
Ping from windows pc to google for public ip.
</p>
<br />

<p>
  
![wiresharkicmpaccessdisable](https://github.com/user-attachments/assets/9b7a1702-20a7-4e79-90e2-6ef713dd4ffb)

</p>
<p>
ICMP traffic disabled on linux VM, monitoring ICMP traffic halt and re-enabling icmp traffic. 
</p>
<br />

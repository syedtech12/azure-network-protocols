<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />
<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (ICMP, SSH, DHCP, DNS, RDP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Create a Resource Group
- Create a Virtual Machine
- Observe ICMP Traffic
- Observe SSH Traffic
- Observe DHCP Traffic
- Observe DNS Traffic
- Observe RDP Traffic

<h2>Actions and Observations</h2>
</br>
</br>
<h3 align="center">
  Set up your virtual environment
</h3>
</br>
<p>
  First, let's create our Resource Group inside our Azure subscription.
</p>
<p>
  <img src="https://i.imgur.com/GXF2G7j.png" height="75%" width="100%" alt="Resource Group"/>
</p>
<p>
  Now create your Windows virtual machine. I typically create the VM in (US) South Central US.
</p>
<p>
  While creating the VM, select the previously created Resource Group and allow it to create a new Virtual Network (Vnet) and Subnet. Make sure to use the password option under the <strong>Administrator Account</strong> section:
</p>
<p>
  <img src="https://i.imgur.com/bC6we0m.png" height="75%" width="100%" alt="Windows VM"/>
</p>
<p>
  Create an Ubuntu virtual machine.
</p>
<p>
  While creating the VM, select the previously created Resource Group and allow it to create a new Virtual Network (Vnet) and Subnet. Make sure to use the password option under the <strong>Administrator Account</strong> section (not seen in image):
</p>
<p>
  <img src="https://i.imgur.com/IvH0C3d.png" height="75%" width="100%" alt="Ubuntu VM"/>
</p>

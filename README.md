<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


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

## High-Level Steps

1. **Setting Up Network Security Groups (NSGs)**
   - Create NSGs for inbound and outbound traffic.
   - Define security rules for SSH, RDP, DNS, HTTP/S, and ICMP protocols.
   - Associate NSGs with the Azure Virtual Network and subnet.

2. **Installing Wireshark on Ubuntu Server VM**
   - Update package repository.
   - Install Wireshark.
   - Configure Wireshark permissions.
   - (Optional) Restart the VM.

3. **Capturing and Analyzing Traffic with Wireshark**
   - Launch Wireshark on the Ubuntu Server VM.
   - Select the network interface.
   - Begin capturing packets.
   - Generate traffic for SSH, RDP, DNS, HTTP/S, and ICMP protocols.
   - Analyze captured traffic.

4. **Experimenting with NSGs**
   - Modify NSG rules for each protocol.
   - Test connectivity between Azure VMs after rule modifications.


# Tutorial: Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines

Welcome to our comprehensive guide on Network Security Groups (NSGs) and inspecting traffic between Azure Virtual Machines (VMs) using Wireshark! We'll explore how to set up NSGs, capture, and analyze traffic using Wireshark installed on an Azure VM running Ubuntu Server 20.04. We'll experiment with different network protocols including SSH, RDP, DNS, HTTP/S, and ICMP, providing specific examples and steps for each protocol.

## Estimated Time
Approximately 1 hour (may vary depending on experience)

## Prerequisites
Before we begin, ensure you have:
- An active Azure subscription
- Basic knowledge of Azure Virtual Machines and networking concepts
- Access to an Azure VM running Ubuntu Server 20.04
- Wireshark installed on the Ubuntu Server VM

## Step 1: Setting Up Network Security Groups (NSGs)

### 1.1. Create NSGs
- Log in to the Azure portal.
- Navigate to the Networking section and select "Network security groups".
- Define security rules for SSH, RDP, DNS, HTTP/S, and ICMP protocols.

### 1.2. Associate NSGs
- Associate NSGs with the Azure Virtual Network and subnet containing your Ubuntu Server 20.04 VM.

## Step 2: Installing Wireshark on Ubuntu Server VM

### 2.1. Update Package Repository
- SSH into the Ubuntu Server VM.
- Update the package repository using the command:

**sudo apt update**


### 2.2. Install Wireshark
- Install Wireshark using the command:

**sudo apt install wireshark**


### 2.3. Configure Wireshark Permissions
- Add your user to the `wireshark` group:

**sudo usermod -aG wireshark $USER**


### 2.4. Restart VM (Optional)
- Restart the Ubuntu Server VM to apply the changes:

**sudo reboot**


## Step 3: Capturing and Analyzing Traffic with Wireshark

### 3.1. Launch Wireshark
- SSH into the Ubuntu Server VM.
- Launch Wireshark with user privileges:

**sudo wireshark


### 3.2. Select Interface
- Select the network interface connected to the Azure Virtual Network.

### 3.3. Capture Traffic
- Begin capturing packets in Wireshark.

### 3.4. Generate Traffic for Each Protocol
- Initiate activities to generate traffic for SSH, RDP, DNS, HTTP/S, and ICMP protocols.

### 3.5. Analyze Traffic
- Stop packet capture in Wireshark.
- Analyze captured packets to observe traffic patterns and protocols.

## Step 4: Experimenting with NSGs

### 4.1. Modify NSG Rules
- Experiment with modifying NSG rules for each protocol.

### 4.2. Test Connectivity
- Test connectivity between Azure VMs after modifying NSG rules.


## Conclusion

Congratulations on completing my fun little tutorial! Thanks for exploring Azure networking concepts, inspecting traffic with Wireshark, and experimenting with Network Security Groups with me. I will continue to explore Azure and networking to further expand my skills and knowledge in the cloud.
Feel free to use and modify this Markdown-formatted tutorial!



Happy networking! 🌐🚀

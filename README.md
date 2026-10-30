#Cybersecurity Lab Environment Setup (Week 1 - PM1)

Building an isolated virtual lab environment for penetration testing and ethical hacking practice.

#Project Overview
This project focuses on setting up a virtual cybersecurity and penetration-testing laboratory using VirtualBox and Kali Linux.

The purpose of the lab is to create a controlled environment where cybersecurity tools, network scanning, reconnaissance, vulnerability assessment, and other security-testing activities can be performed safely and repeatedly.

The lab is configured on a private virtual network so that additional machines can be added later and used as targets for authorized security testing.

🎯 Objectives

The main objectives of this project are to:

Install and configure VirtualBox.
Install/import Kali Linux as a virtual machine.
Create a private NAT Network for the cybersecurity lab.
Configure network connectivity for Kali Linux.
Assign a consistent IP address to the Kali VM.
Verify network connectivity and DNS resolution.
Take a clean VM snapshot for recovery.
Document the complete setup process.
Prepare the environment for future cybersecurity projects.

🛡️ Purpose of the Lab


The lab provides an isolated and controlled environment for cybersecurity learning and authorized security testing.

It can be used for activities such as:

Network reconnaissance
Port scanning
Vulnerability assessment
Packet analysis
Web security testing
Exploitation practice
Security-tool experimentation

##Lab Architecture & Steps##

⚙️ Lab Configuration

🧩 Component	⚙️ Configuration
🖥️ Host OS: Windows 12
🧠 Host RAM	: 16 GB
⚡ Processor	Intel Core i7
🧰 Hypervisor	VirtualBox 7.2
🐉 Security OS	Kali Linux 2026.2
🌐 Virtual Network	NAT Network
📡 Network Address	10.0.0.0/24
🚪 Default Gateway	10.0.0.1
🌍 DNS Server	8.8.8.8
🔮 Future VM Range	10.0.0.3–10.0.0.99

🪜 Lab Setup Procedure

**Step 1. Install 7-Zip


7-Zip was installed to extract the Kali Linux virtual-machine package, which may be distributed as a .7z archive.

Tool: 7-Zip

**Step 2. Install VirtualBox

VirtualBox was installed as the hypervisor.

**Step 3. Create the NAT Network
A dedicated NAT Network was created in VirtualBox.

Configuration: Network Name: NatNetwork IPv4 Prefix: 10.0.0.0/24 DHCP: Enabled

<img width="756" height="467" alt="NAT Network setup" src="https://github.com/user-attachments/assets/99c94651-824f-4474-a9a4-a3ad593e51ea" />


A NAT Network was selected because multiple virtual machines connected to the same NAT Network can communicate with one another while also having outbound network connectivity.

This will allow future attacker and target VMs to communicate within the lab.

**Step 4. Import Kali Linux
The Kali Linux virtual machine was downloaded from the official Kali Linux website and imported into VirtualBox.

The VM network adapter was configured as follows:

Adapter 1

Attached to: NAT Network
Network:  NatNetwork
Adapter Type: Intel PRO/1000 MT Desktop

**Step 5. Configure the Kali Linux Network
The Kali Linux network configuration was checked and configured with a consistent IPv4 address.

Example configuration:

IP Address: 10.0.0.2
Subnet Mask: 255.255.255.0
Gateway: 10.0.0.1
DNS: 8.8.8.8
A consistent IP address makes it easier to document the lab and reference the Kali machine in future exercises.

<img width="955" height="508" alt="Kali Static IP" src="https://github.com/user-attachments/assets/a7ff9ffd-c3ca-4f3f-b20d-38f4528e06f8" />






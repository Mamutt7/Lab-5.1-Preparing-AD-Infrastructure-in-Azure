<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
In this home lab, I will set up a domain controller in Azure for the next few following lab series.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

Setup Domain Controller in Azure

Create a Resource Group

Create a Virtual Network and Subnet

Create the Domain Controller VM (Windows Server 2022) named “DC-1”

●	Username: labuser

●	Password: Cyberlab123!

After VM is created, set Domain Controller’s NIC Private IP address to be static

Log into the VM and disable the Windows Firewall (for testing connectivity)

 ![image](https://github.com/user-attachments/assets/92697741-60f8-439d-9c74-1cc8fd16f916)


Setup Client-1 in Azure
—
Create the Client VM (Windows 10) named “Client-1”

●	Username: labuser

●	Password: Cyberlab123!

Attach it to the same region and Virtual Network as DC-1

After VM is created, set Client-1’s DNS settings to DC-1’s Private IP address
 
![image](https://github.com/user-attachments/assets/830525e9-dfdd-4f3a-9793-740b4698779b)

From the Azure Portal, restart Client-1

Login to Client-1

Attempt to ping DC-1’s private IP address

●	Ensure the ping succeeded

From Client-1, open PowerShell and run ipconfig /all

●	The output for the DNS settings should show DC-1’s private IP Address

 ![image](https://github.com/user-attachments/assets/492b953e-6841-4d60-a19d-b5cbeab62683)



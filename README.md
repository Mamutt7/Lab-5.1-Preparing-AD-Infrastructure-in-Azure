# Lab-5.1-Preparing-AD-Infrastructure-in-Azure
In this home lab, I will setup a domain controller in Azure for the next few following lab series. (please refer to the rest of the Lab 5 repositories as they are all part of the project)


Setup Domain Controller in Azure
—
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



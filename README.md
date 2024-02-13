# Active Directory Lab

## Overview
This project utilizes VirtualBox to set up a domain controller running Active Directory on a Windows 2019 Server along with a Windows 10 host connected to that domain controller. For the purposes of this lab, the domain controller will connect to the internet and intranet, but the host will only have an internet connect through the domain controller. 

## Project Tasks
1. Windows Server 2019 Installation
   
Installed Windows Server 2019 with dual NIC configuration.
Configured one NIC for external access and another for internal access.

2. Active Directory Setup
   
Added Active Directory Domain Services role.
Established the domain as "Mydomain.com."
![AD1](https://github.com/DrewCrouch1/Active-Directory-Lab/assets/158229796/ef1f3312-e6eb-402c-99ff-9ed4ab9d6e81)

3. User Account Creation

Created a Domain Admin account with the username "a-dcrouch."
Ran a PowerShell script to generate 1002 user accounts in the Organizational Unit "_Users."
Usernames are based on the first letter of the first name and the last name.
All accounts share the password "Password1." for the sake of the project.

Before script:

![AD2](https://github.com/DrewCrouch1/Active-Directory-Lab/assets/158229796/0ae40c65-a624-45dd-b3a6-459f5a7e6e0e)

After Script:

![AD3](https://github.com/DrewCrouch1/Active-Directory-Lab/assets/158229796/3c48771f-6c0a-4466-844c-22b48e0f242a)

4. Network Configuration

Added Remote Access/Routing role for client internet access through the DC using NAT via the Internet NIC.
Configured DHCP Server role to assign IP addresses within the range of 172.16.0.100-200.

![AD4](https://github.com/DrewCrouch1/Active-Directory-Lab/assets/158229796/1668b4ae-a583-4f81-b161-c68530983e6a)


5. Windows 10 Host Configuration

Created a Windows 10 Host configured to use the intranet NIC.
Confirmed DHCP server functionality and successful client lease assignment within the specified IP range.
Verified the Domain Controller as the default gateway and confirmed internet access.

![AD5](https://github.com/DrewCrouch1/Active-Directory-Lab/assets/158229796/16815dc3-2f6c-499f-9be2-30d992a9f144)


6. Domain Join and User Login

Successfully joined the domain with the Windows 10 Host.
Verified the ability to log in using one of the user accounts created via the PowerShell script.

![AD6](https://github.com/DrewCrouch1/Active-Directory-Lab/assets/158229796/cfffe6be-cf8d-45d4-9875-27aa9d0c5b9e)

Conclusion
This project showcases the step-by-step implementation of an Active Directory Lab, demonstrating domain setup, user account creation, network configuration, and successful domain join and user login. The detailed documentation provides a comprehensive guide for understanding and replicating the environment.

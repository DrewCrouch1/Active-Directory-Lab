# Active Directory Lab

## Overview
This project utilizes VirtualBox to set up a domain controller running Active Directory on a Windows 2019 Server along with a Windows 10 host connected to that domain controller. For the purposes of this lab, the domain controller will connect to the internet and intranet, but the host will only have an internet connect through the domain controller. 

## Project Tasks
1. Windows Server 2019 Installation
Installed Windows Server 2019 with dual NIC configuration.
Configured one NIC for external access and another for internal access.

3. Active Directory Setup
Added Active Directory Domain Services role.
Established the domain as "Mydomain.com."
![alt text](https://imgur.com/3NouoKc)

4. User Account Creation
Created a Domain Admin account with the username "a-dcrouch."
Ran a PowerShell script to generate 1002 user accounts in the Organizational Unit "_Users."
Usernames are based on the first letter of the first name and the last name.
All accounts share the password "Password1."
5. Network Configuration
Added Remote Access/Routing role for client internet access through the DC using NAT via the Internet NIC.
Configured DHCP Server role to assign IP addresses within the range of 172.16.0.100-200.
6. Windows 10 Host Configuration
Created a Windows 10 Host configured to use the intranet NIC.
Confirmed DHCP server functionality and successful client lease assignment within the specified IP range.
Verified the Domain Controller as the default gateway and confirmed internet access.
7. Domain Join and User Login
Successfully joined the domain with the Windows 10 Host.
Verified the ability to log in using one of the user accounts created via the PowerShell script.
Before and After
Before: [Screenshot or description of initial state]
After: [Screenshot or description of final configured state]
Conclusion
This project showcases the step-by-step implementation of an Active Directory Lab, demonstrating domain setup, user account creation, network configuration, and successful domain join and user login. The detailed documentation provides a comprehensive guide for understanding and replicating the environment.

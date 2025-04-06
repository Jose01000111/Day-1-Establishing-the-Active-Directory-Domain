<p align="center">
<img src="https://i.imgur.com/6hzWjn5.png" alt="osTicket logo"/>
</p>

When I first imagined this scenario, I wanted to gain a deeper understanding of what an IT professional might encounter when setting up a new office space for a large organization. I chose the example of the Chicago Bears purchasing the Arlington Racecourse because it involves a dynamic, high-profile organization with varied IT needs, making it a perfect case study for applying Active Directory solutions.
This scenario isn’t just about configuring systems—it's about imagining what kinds of challenges IT professionals face when moving from one location to another, particularly in a business environment that needs a scalable, secure, and reliable IT infrastructure. Active Directory (AD) provides a solution for many of these challenges, and by walking through this setup, I could understand the core capabilities AD brings to the table, especially in terms of user management, resource access, security, and disaster recovery.

# Day 1: Establishing the Active Directory Domain
The initial step of setting up a Domain Controller (DC) is where Active Directory truly shines. It’s not just about having one system to manage everything—it’s about creating a centralized, scalable solution for the entire organization. With AD, I can easily control user access to resources, ensuring that all employees are part of the same trusted domain.
By creating organizational units (OUs), I could establish clear divisions between departments, ensuring that policies and permissions are applied uniformly and appropriately. This allows for an organized and efficient structure, a feature that I quickly realized is vital for managing a growing business like the Bears in their new headquarters.

# 🛠️ Lab Tasks

### 1. Install Windows Server & Prepare the Environment
   
•	Deploy Windows Server 2022 (or 2019).

•	Resource group: ArlingtonHQ-AD-Lab

•	Region: (US) Central US

https://imgur.com/D7noL6f

•	Assign a static IP address.

•	Rename the server to: AD-CHIBEAR-60005

https://imgur.com/A3REYtc

•	Password: ************

### 3. Promote to Domain Controller
   
• Use Server Manager to install the following roles:

   o	Active Directory Domain Services (AD DS)
  
   o	DNS Server

   https://imgur.com/HLQDkZk
  
### 4. Promote the server to a Domain Controller.
  o	New Forest: chicagobears.local
  
  o	Configure domain and DNS settings as needed.
  
  o	Restart upon completion.

### 5. Create Organizational Units (OUs)
   
• Use Active Directory Users and Computers (ADUC) to define departmental structure:

https://imgur.com/Mal9yWh

├── Admin

├── HR

├── IT

├── Operations

└── Staley the bear

https://imgur.com/61UgoRS

##### These OUs will help manage group policies, delegate administrative control, and organize users by department.

# 💻 Technology Stack

##### Technology	Role

##### Windows Server 2022	Domain Controller, DNS Server

##### Active Directory Domain Services (AD DS)	Centralized identity management

##### DNS	Domain resolution for internal network

##### Hyper-V / VirtualBox / VMware	(Optional) Virtual environment for lab setup

##### Windows 10/11 Client	Domain join & login test

##### Remote Server Administration Tools (RSAT)	ADUC and other management tools

# 🛠️ Summary of Lab Goals
•	Set up a Windows Server as the first Domain Controller

•	Create a new Active Directory domain: chicagobears.local

•	Configure Organizational Units (OUs) for each department

•	Create a domain user account: Staley the Bear

•	Join a client machine to the domain

•	Validate setup using built-in tools (dcdiag, domain login)

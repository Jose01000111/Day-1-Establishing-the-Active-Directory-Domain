<p align="center">
<img src="https://i.imgur.com/pqTjnLb.png" alt="osTicket logo"/>
</p>

## Active Directory Migration for the Chicago Bears' New Headquarters

When the Chicago Bears announced their move to the Arlington Heights Racecourse, it signaled more than a new stadium—it meant a full infrastructure overhaul. I was brought on as a Systems Administrator to build out their cloud-based IT environment from scratch. My job was to ensure that the Arlington Heights location could support secure, enterprise-grade IT operations from day one.

This five-day Active Directory lab simulates that real-world deployment. Throughout the process, I leaned on both my technical knowledge and tools like ChatGPT to clarify configurations, troubleshoot issues, and solidify my understanding of Microsoft Active Directory in Azure. Here's a breakdown of my journey:

## Day 1: Establishing the Active Directory Domain
The initial step of setting up a Domain Controller (DC) is where Active Directory truly shines. It’s not just about having one system to manage everything—it’s about creating a centralized, scalable solution for the entire organization. With AD, I can easily control user access to resources, ensuring that all employees are part of the same trusted domain.
By creating organizational units (OUs), I could establish clear divisions between departments, ensuring that policies and permissions are applied uniformly and appropriately. This allows for an organized and efficient structure, a feature that I quickly realized is vital for managing a growing business like the Bears in their new headquarters.

### 🧪 Lab Tasks

#### 1. Install Windows Server & Prepare the Environment
   
•	Deploy Windows Server 2022 (or 2019).

•	Resource group: ArlingtonHQ-AD-Lab

•	Region: (US) Central US

<p align="center">
<img src="https://i.imgur.com/D7noL6f.png" alt="osTicket logo"/>
</p>

•	Assign a static IP address.

•	Rename the server to: AD-CHIBEAR-60005

<p align="center">
<img src="https://i.imgur.com/A3REYtc.png" alt="osTicket logo"/>
</p>

•	Password: ************

#### 3. Promote to Domain Controller
   
• Use Server Manager to install the following roles:

   o	Active Directory Domain Services (AD DS)
  
   o	DNS Server

<p align="center">
<img src="https://i.imgur.com/HLQDkZk.png" alt="osTicket logo"/>
</p>
  
#### 4. Promote the server to a Domain Controller.
  o	New Forest: chicagobears.local
  
  o	Configure domain and DNS settings as needed.
  
  o	Restart upon completion.

<p align="center">
<img src="https://i.imgur.com/AmpbSWu.png" alt="osTicket logo"/>
</p>

#### 5. Create Organizational Units (OUs)
   
• Use Active Directory Users and Computers (ADUC) to define departmental structure:

<p align="center">
<img src="https://i.imgur.com/Mal9yWh.png" alt="osTicket logo"/>
</p>

├── Admin

├── HR

├── IT

├── Operations

└── Staley the bear

<p align="center">
<img src="https://i.imgur.com/61UgoRS.png" alt="osTicket logo"/>
</p>

##### These OUs will help manage group policies, delegate administrative control, and organize users by department.

## 💻 Technology Stack

##### Technology	Role

##### Windows Server 2022	Domain Controller, DNS Server

##### Active Directory Domain Services (AD DS)	Centralized identity management

##### DNS	Domain resolution for internal network

##### Hyper-V / VirtualBox / VMware	(Optional) Virtual environment for lab setup

##### Windows 10/11 Client	Domain join & login test

##### Remote Server Administration Tools (RSAT)	ADUC and other management tools

## 🛠️ Summary of Lab Goals
##### ✅ Set up a Windows Server as the first Domain Controller

##### ✅Create a new Active Directory domain: chicagobears.local

##### ✅Configure Organizational Units (OUs) for each department

##### ✅Create a domain user account: Staley the Bear

##### ✅Join a client machine to the domain

##### ✅Validate setup using built-in tools (dcdiag, domain login)

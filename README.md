<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles, Departments and Teams
- Configure Agents and Users
- Configure SLA and Help Topics





<h2>Acknowledging the Difference Between the Agent Panel and the Admin Panel</h2>

Before configuring anything, it’s important to understand the key distinction between the Agent Panel and the Admin Panel.

•	The Agent Panel is where individual agents carry out their daily tasks. It’s mostly execution: handling tickets, responding to inquiries, and engaging with customers.

•	The Admin Panel is where configuration happens. This is where roles, departments, and teams are defined, laying the foundation for an efficient workflow.

<h2>Configuration Steps</h2>



![Untitled design](https://github.com/user-attachments/assets/d6237115-80a4-4800-b4df-04176a6094c8)


Configure Roles (for grouping permissions)
Admin Panel -> Agents -> Roles
	•	Supreme Admin

Configure Departments
Admin Panel -> Agents -> Departments
	•	SysAdmins

Configure Teams
Admin Panel -> Agents -> Teams (Pull Agents from different Departments)
	•	Online Banking

<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

Allow anyone to create tickets
Admin Panel -> Settings -> User Settings (UNCHECK: unregistered users can create tickets)
	•	Registration Required: Require registration and login to create tickets 

Configure Agents (workers)
Admin Panel -> Agents -> Add New
	•	Jane (Dept: SysAdmins)
	•	John (Dept: Support)

Configure Users (customers)
Agent Panel -> Users -> Add New
	•	Karen
	•	Ken

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Configure SLA
Admin Panel -> Manage -> SLA
	•	Sev-A (Grace Period: 1 hour, Schedule: 24/7)
	•	Sev-B (Grace Period: 4 hours, Schedule: 24/7)
	•	Sev-C (Grace Period: 8 hours, Business Hours)

Configure Help Topics (For when users create a ticket)
Admin Panel -> Manage -> Help Topics
	•	Business Critical Outage
	•	Personal Computer Issues
	•	Equipment Request
	•	Password Reset
	•	Other

<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
Hey there! This is a guide on how to configure osTicket, an open-source help desk ticketing system, after the installation process. This includes setting up Users, Agents, and SLAs<br />

<b>Note:</b> To follow along with this guide, make sure you have completed the prerequisites and installation steps described in my previous demonstration, "osTicket-Setup". 

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- [osTicket Documentation](https://docs.osticket.com/en/latest/index.html)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)


<h2>Post-Install Configuration Objectives</h2>
Create and Configure Roles
Create and Configure Departments & Teams
Create and Configure Agents (workers) & Users (clients)
Configure SLA (Service Level Agreements)
Configure Help Desk Topics
<h2>Configuration Steps</h2>
<h3>&#9312; Prerequisites and Installation</h3>
This demonstration assumes a virtual machine is established with the prerequisite files installed for working osTicket. </br>
Credentials and configurations that will be used in this demonstration can be found in "Prerequisites and Installation". </br>

<hr>
<h3>&#9313; Admin Panel - Roles, Departments, Teams, & Agents</h3>
On the web browser (Microsoft Edge), go to the Help Desk Login Page and sign in to your osTicket Help Desk credentials (this example uses username ostuser / ostuser@email.com).
Help Desk Login Page -- http://localhost/osTicket/scp/login.php

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/d95fe1c5-92f6-4ec5-afc0-f14cc81c926e)


You will be brought to the Agent Panel, click on "Admin Panel" at the top-right of the page.

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/72567152-620c-49ad-9a8b-c7c61fa28b73)



Click on the "Agents" tab > "Roles" > "Add New Role".

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/02772996-20ec-4b70-b8e9-1cbfb7256425)



"Roles are the permissions granted to Agents per Department that they have access to."

In the Definition tab, type any Role name of your choice (this example uses Supreme Admin).
This role will be given all permissions.
Then, click on the Permissions tab.

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/96fb26a4-ae59-41ae-9505-b401978026d6)



In the Permissions tab, under the Tickets category, checkmark ALL boxes.
Go through both Tasks and Knowledgebase categories and checkmark ALL boxes as well.
Once done, click "Add Role".

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/5de7b7a7-75ff-4c10-9393-e382ada94a64)


Now we've created a Supreme Admin role with all permissions granted. Next, we'll create a Department.

Currently, in the Agents tab, click on the "Departments" category.
Click "Add New Department".

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/6c02d879-ee53-4f74-b203-d611a034d0b0)


Create a Department name of your choice (this example uses System Administrators).
Skip everything else for now and click "Create Dept".

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/b7fb22b9-cffb-4717-9456-b167bf27e551)


Next, we'll move on to creating a Team. <br>
"Teams allow you to pull Agents from different Departments and organize them to handle a specific issue or user via a Help Topic or Ticket Filter."

Currently in the Agents tab, click on the "Teams" category.

Click "Add New Team".

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/c5d6e587-b5a4-4b52-a333-808c91196794)



Create a Team name of your choice (this example uses Level II Support).
Click "Create Team".

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/5a55f39f-359b-4a09-b2d6-92b362e743a5)



Currently, in the Agents tab, click the "Agents" category, then "Add New Agent".

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/0258772f-e1ea-4548-ad42-b185b32ae720)


Create the required credentials for this user that are in bold:
First Name (this example uses Jane).
Last Name (this example uses Doe).
Email Address (this example uses jane.doe@osTicket.com).
Username (this example uses jane.doe).
Click "Set Password" and a windows prompt will appear:
Uncheck "Send the agent a password reset email".
Create a password for this user.
Uncheck "Require password change at next login".
Click "Set".

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/6da4e024-2cf2-414b-8305-fb4cd0848eab)



Click on the "Access" tab:
Assign this user the Department that we created (this example uses System Administrators).
Assign this user the Role that we created (this example uses Supreme Admin).
Under Extended Access, assign this user the "Support" department with the "Supreme Admin" role.
Click "Save Changes".

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/935eb874-a83f-4b32-987d-0f50d44694ac)




Click on the "Teams" tab:
Assign this user the Team that we created (this example uses Level II Support).
Once done, click "Create".

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/9d8cdd35-748e-4aa0-a712-2d7ce8cd6267)



Create another Agent following the steps, however assign it to a different Role and Department.</br>
This example creates Agent "John Doe" | Department: "Level I Support" | Role: "View only | Extended Access: Support".

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/86af5d5b-1631-420c-a284-b206f92def78)



<hr>
<h3>&#9314; Agent Panel - Creating Users</h3>
Click on "Agent Panel" on the top-right of the page.

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/4a96bc9d-3f5e-49ae-b713-4649affa5fcd)


Click on the "Users" tab.
Click on "Add User".
Create an Email Address and Full Name for this user (this example uses karen@osticket.com / Karen Karen).
Click "Add User".

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/b98ef4d8-61fd-488e-ab1c-873fa317fa4e)


![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/999f75cd-095d-4316-ba8b-b7fbbf5527b5)



Create another user of your choice (this example uses ken@osticket.com / Ken Ken)

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/c658a495-2015-4fc3-90e9-465797a38bbb)



<hr>
<h3>&#9315; Admin Panel - Configuring SLA</h3>
"SLA Plans or Service Level Agreements, are unlimited in osTicket. The purpose of the SLA Plan is to provide a length of time in which the help desk Administrator expects tickets to be closed."

Return to the "Admin Panel".
Navigate to "Manage" tab > "SLA".
Click "Add New SLA Plan".

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/a7efb170-b1e9-469f-bb7e-2e343fbd2dbd)


Create the following plans:
SEV-A

Grace Period: 1 hour (Amount, in hours, before tickets with this SLA will become overdue if not closed in allotted time.)
Schedule: 24/7 (Accounted for all days of the week, even on non-business days)
SEV-B

Grace Period: 4 hours
Schedule: 24/7
SEV-C

Grace Period: 8 hours
Schedule: Monday - Friday 8am - 5pm with U.S. Holidays
Click "Add Plan" for each.

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/e8fb31de-b2c6-4571-8599-8ebc33272416)


![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/08b699f2-2b86-4ae8-a13c-67c29c9d163a)



<hr>
<h3>&#9316; Configure Help Topics</h3>
Help Topics will help streamline your end-user’s help desk experience to ensure proper assignment and prompt response to the ticket.

Currently in the Admin Panel, navigate to "Manage" tab > "Help Topics".
Click "Add New Help Topic".

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/4ab22285-d24e-475d-b843-187ca7724bdc)



Create Help Topics with the following names:
Business Critical Outage
Personal Computer Issues
Equipment Request
Password Reset
"Internal Notes" can be written down for personal use, but not necessary.
After that, click "Add Topic".

![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/e6bfb31c-6861-4365-ae6e-e8409088f56a)


![image](https://github.com/ShayneSL/osTicket-BackEnd-Config/assets/88577075/76c7e07e-bd7c-4a48-89c4-dd43fb935d2c)



<hr>
<h1><p align=center>All Done</p></h1

<h2><p align=center>Next Demonstration:<br><a href="https://github.com/ShayneSL/Ticket-Lifecycle">Ticket Lifecycle Examples</a></p></h2>








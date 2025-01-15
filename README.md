<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Configure osTicket, post-installation](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Acknowladge Agent Panel vs Admin panel
- Configure Roles
- Add new agents
- Configure SLAs
- Configure Teams

<h2>Configuration Steps</h2>

<p>
If you are continuing from that last tutorial remember to start your VM in Azure portal and reconnect to the VM with your newly install osTicket.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

   In side your VM login into osTicket admin/analyst with this link [osTicket-Admin Login](http://localhost/osTicket/scp/login.php). Login using the username and password we created in the previous tutorial. At the top right corner of the webpage we can switch between the admin and agent panel. The first thing we are going to configure are roles. Roles give team members certain access to tickets and tasks and can be assgined to agents, teams, and departments.  Go to Admin Panel > Agents > Roles. Here we can view all of ours roles and if click on a role and go to permissions we can see what that role is allowed to do with tickets and tasks. From the roles page we can also create new roles. CLick add new role and name it supreme admin. On the permissions page check all the boxes to give the supreme adimin access to everything in tickets, tasks, and knowledgebase. Then click "add role".

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we will configure departments. Go to Admin panel > Agents > Departments. Here we can view, edit and create new departments. Click add new Department. Name the deparment Sysadmins. Under setting we can aslo assign SLAs, which we will do later. In the access panel you can assign agents to the department. For now click "create dept".
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we will configure teams. Teams are for creating a group of people who are all from different departments. Go to admin panel> agents > teams. Click on "add new Teeam" and name the team "Online Banking". On the members panel you can add agents to the team which we will do later after we create some agents. For now click "create team" at the bottom. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we'll configure who are able to create tickets. Go to admin panel > settings > users. Then under authentication settings make sure "Registration Required" is unchecked". This allows anyone to able create with out having to login.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Finally we are going to create some agents (workers). Go to admin panel > agents > "add New Agent". For this tutorial, name the agent "Dawn Smith" and the email to "Dawn@ticket.com" (fake email). Set the username to "Dawn" as well. Then click set password. Uncheck "send the agent a password rest email". Set the password to "Password1" and uncheck "require password change at next login". Then click reset. Next go to the access panel and make her deparment "sysadmin" and role "supreme admin". Then in the teams panel set her to the "online banking" and click add. Then hit create. Create another agent named "Peter Quill" a silmiar email and username as Dawn and the same password. Add him to the support department and give him limited access. Then hit create. 

   ***save the passwords into your notes***
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we create a User (customers). Go to agent panel > Users > add new. Name the user "Molly" and her email to "Molly@problem.com". Then click "add User".
   
   ***save the user and email into your notes***
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we'll configure 3 SLAs (Service Level Agreements). Go to admin panel > Manage > SLA. Click " New SLA Plan" create the following:

   |  | Sev-A |  Sev-B | Sev-c |
| ------------- | ------------- | ------------- | ------------- |
| Grace Period (in hours)  | 1 | 4  | 8  |
| Schedule | 24/7  | 24/7   | Mon - Friday  |
   
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lastly we will create Help Topics for when users create a ticket. go to admin panel > Manage > Help Topics > add new help topics. Then create the following:
   
   - Business Critical Outage - Report a Problem
   - Personal Computer Issues - Report a Problem
   - Equipment Request - General inquiry
   - Password Reset - Report a Problem
   - Other - General inquiry

Congradulation your osticket is now configured
in the next tutorial we will run through proccessing tickets
</p>
<br />








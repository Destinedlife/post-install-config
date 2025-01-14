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

<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1 align="center">osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket. This tutorial assumes you have fully completed, installed, set up login credentials, and perform clean up on osTicket in your Virtual Machine environment via following the previous tutorial <a href ="https://github.com/ColtonTrauCC/osticket-prereqs">"osTicket - Prerequisites and Installation"</a><br />

</br>

<h2>Environments and Technologies Used</h2>
<ul>
  <li>Microsoft Azure (Virtual Machines/Compute)</li>
  <li>Remote Desktop</li>
  <li>Internet Information Services (IIS)</li>
  <li>osTicket</li>
</ul>

</br>

<h2>Operating Systems Used </h2>
<ul>
  <li>Windows 10</li>
</ul>

</br>

<h2>Post-Install Configuration Objectives</h2>
<ol>
  <li>Familiarity with the UI of osTicket</li>
  <li>Creating and Configuring Roles</li>
  <li>Creation of Tickets</li>
  <li>Creating Agents and Users</li>
  <li>Setting up Service Level Agreements (SLA Plans) in ticketing system</li>
  <li>Configuring Help Topics</li>
</ol>

</br>

<h2>Configuration Setups</h2>

<!-- <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/> -->

<h3>Configuring Roles, Departments, & Teams</h3>

<p>
  
<ul>
  <li><b>Note</b>: There are two panels when navigating osTicket; <b>Agent Panel</b> and <b>Admin Panel</b>, you'll know which panel you are on if the <b>opposite panel</b> is displayed on the top right of the UI next to your user login name</li>
  <ul>
    <li>In this example, the user "Rogeric" is on the Agent Panel</li>
    <li><img src="https://github.com/RogericHarper44/post-install-config/assets/168601987/1a2a7417-c09f-4446-b5c6-cbf67a3b5c1d"
"Disk Sanitization Steps"/></li>
  </ul>
  <li><b>Roles</b> grant certain permisions to Agents in an Department they are assigned to</li>
  <ul>
    <li>In the <b>Admin Panel</b>, go to the <b>Agents</b> tab and click on <b>Roles</b>, then click on <b>Add New Role</b></li>
    <ul>
      <li><b>Note</b>: osTickets creates four Roles (All Access, Expanded Access, Limited Access, and View Only) by default.</li>
      <li><img src="https://github.com/RogericHarper44/post-install-config/assets/168601987/e9f8fd39-bad5-46ad-a46d-6b5f14b4e502"/></li>
    </ul>
    <li>Name the new Role <b>Supreme Admin</b>, and click on the <b>Permissions</b> tab; in this tab you can assign specific permissions to this role. For our "Supreme Admin" Role, we will check every box under the <b>Tickets</b>, <b>Tasks</b>, and <b>Knowledgebase</b> tabs. Click on <b>Add Role</b> to finish and create the role.</li>
    <ul>
      <li><img src="https://github.com/ColtonTrauCC/post-install-config/assets/147654000/306c368f-76fb-4b25-869b-d1a1f430ed76" height="80%" width="80%" alt="Disk Sanitization Steps"/></li>
    </ul>
  </ul>

  <li><b>Departments</b> are needed to route and resolve tickets based on their importance or instructions</li>
  <ul>
  <li>Still on the Agents tab, click on <b>Departments</b> and click on <b>Add New Department</b></li>
  <ul>
    <li><b>Note</b>: Much like Roles, osTicket also creates two Departments (Maintenance and Support) by default</li>
    <li><img src="https://github.com/RogericHarper44/post-install-config/assets/168601987/b5fdd35e-3d88-4cf7-93c3-b759cfc9a4b4"
/></li>
  </ul>
  <li>Name the Department <b>System Administrators</b> (we'll leave everything else by default for now), then click on <b>Create Dept</b> to create Department</li>
  <ul>
    <li><img src="https://github.com/RogericHarper44/post-install-config/assets/168601987/f65468e3-ecdc-4e6d-831f-4e1ed1d7a89f"
/></li>
  </ul>
  </ul>

  <li><b>Teams</b> allow us to organize Agents from different Departments in osTicket to handle specific issues and supersede Agents and their Departments' parameter rules</li>
  <ul>
    <li>In the Agents tab, click on <b>Teams</b> and click on <b>Add New Team</b></li>
    <ul>
    <li><b>Note</b>: Just like previous set ups, osTicket creates a Team (Level I Support) by default</li>
    <li><img src="https://github.com/RogericHarper44/post-install-config/assets/168601987/ef482234-f66f-4ec5-bd9d-3faeb446e5eb"
/></li>
    </ul>
    <li>Name the Team <b>Level II Support</b> then click on <b>Create Team</b> to create the Team</li>
    <ul>
      <li><img src="https://github.com/RogericHarper44/post-install-config/assets/168601987/e4a608c2-478a-49b5-a8e6-618768601afa"
/></li>
    </ul>
  </ul>
  
</ul>
  
</p>

</br>

<h3>Allowing anyone to create Tickets</h3>

<p>
  
<ul>
  <li>In the <b>Admin Panel</b>, head to the <b>Settings</b> tab and click on <b>Users</b>, make sure <b>Registration Required</b> is unchecked. This will allow us to create tickets anonymously</li>
  <ul>
    <li><img src="https://github.com/RogericHarper44/post-install-config/assets/168601987/a38f2bc2-b6f1-4bea-9cc4-70938bef4f08"
/></li>
  </ul>
</ul>
  
</p>

</br>

<h3>Adding Agents and Users</h3>

<p>
  
<ul>
  <li><b>Agents</b> (or Workers) are given the access to the help desk in osTicket to respond, resolve, and update the status of tickets</li>
  
  <ul>
    <li>In the <b>Admin Panel</b>, head to the <b>Agents</b> tab and click on <b>Add New Agent</b></li>
    <ul>
      <li><img src="https://github.com/RogericHarper44/post-install-config/assets/168601987/1aee6a0d-4727-4375-bc47-6697a9f83fa0"
/></li>
    </ul>
    <li>For this tutorial, we will be creating two new Agents <b>Jane</b> and <b>John</b>, it is advise to have a notepad ready to catalog login information as you enter their credentials, but we will set their user names as <b>[name].doe</b> and both of their passwords as <b>Password1</b> for convenience (which is our admin password from the installation tutorial)</li>
    <ul>
      <li>Fill in the Agent's basic info and set the Agent's email address as <b>[name].doe@osticket.com</b> and click on <b>Set Password</b></li>
      <li><img src="https://github.com/RogericHarper44/post-install-config/assets/168601987/98bbfc4e-6d35-4876-9970-1d07c68c1a63"
/></li>
      <li>Set the Agent's password to <b>Password1</b> and unchecked the boxes to prevent the Agent for our example from needing to reset password or change password after login</li>
      <li><img src="https://github.com/RogericHarper44/post-install-config/assets/168601987/f322cb0f-cbc1-46c8-a48c-3830f8a919aa"
/></li>
    </ul>
    <li>Go the <b>Access</b> tab to set the Agent's <b>Primary Department</b> (Mandatory to create the Agent). <b>Extended Access</b> can also be added to the Agent in order to access additional Departments</li>
    <ul>
    <li><img src="https://github.com/RogericHarper44/post-install-config/assets/168601987/23608e19-eda8-4d3d-b0a2-04f3a599f7f7"
/></li>
    </ul>
    <li>OPTIONAL: Head to the <b>Teams</b> tab to assign the Agent to a Team</li>
  </ul>
  
  <li><b>Users</b> (or Customers) are creators and owners of tickets and by using osTicket they are able to track the status of their tickets</li>
  
  <ul>
    <li>In the <b>Agent Panel</b>, go to the <b>Users</b> tab and click on <b>Add User</b></li>
    <ul>
      <li><img src="https://github.com/RogericHarper44/post-install-config/assets/168601987/223ec78c-63ca-4a61-a8f6-922e5909cc5d"
/></li>
    </ul>
    <li>For this tutorial, we will be creating two new Users <b>Ken</b> and <b>Karen</b> and setting up usernames, emails, and passwords similar to our Agents.</li>
    <ul>
      <li><img src="https://github.com/ColtonTrauCC/post-install-config/assets/147654000/8eadff14-b483-4781-9679-80b252a092c4" height="80%" width="80%" alt="Disk Sanitization Steps"/></li>
    </ul>
  </ul>
  
</ul>
  
</p>

</br>

<h3>Adding SLA Plans</h3>

<p>
  
<ul>
  <li><b>Service Level Agreements</b> or SLA Plans provide a length of time for the ticket Administrator when the ticket is expected be CLOSED. They can also be designated to specific Departments or Help Topics</li>
  <li>In the <b>Admin Panel</b>, go to the <b>Manage</b> tab and drop down to <b>SLA</b> then click on <b>Add New SLA Plan</b></li>
  <ul>
    <li><img src="https://github.com/RogericHarper44/post-install-config/assets/168601987/b2a2f9a0-c6c1-47f1-a46e-8e534731dd1e"
/></li>
    
  </ul>
  <li>osTicket by default has the SLA Plan <b>Default SLA</b>. We will be creating three SLA Plans each with their own length of time for different kinds of importance of the ticket, from highest priority to lowest priority:</li>
  <ol>
    <li>SEV-A with <b>1 hour Grace Period, 24/7 Schedule</b>, suitable for tickets that are business critical</li>
    <li>SEV-B with <b>4 hour Grace Period, 24/7 Schedule</b>, suitable for tickets affecting employees such as troubleshooting or PC problems</li>
    <li>SEV-C with <b>8 hour Grace Period, business hours Schedule</b>, suitable for tickets requesting new equipment</li>
  </ol>
  <li>Example of creating SEV-A SLA Plan, click on <b>Add Plan</b> to create the SLA Plan</li>
  <ul>
    <li><img src="https://github.com/RogericHarper44/post-install-config/assets/168601987/c97b89a2-2309-4687-842c-8f4eb0aa8c9f"
/></li>
  </ul>
</ul>
  
</p>

</br>

<h3>Configuring Help Topics</h3>

<p>
  
<ul>
  <li><b>Help Topics</b> are helpful to streamline the ticket entry experience for the user by helping them specify their ticket info and also determine what Department the ticket should go to</li>
  <li>In the <b>Admin Panel</b>, go to the <b>Manage</b> tab and click on <b>Add New Help Topic</b></li>
  <ul>
    <li><b>Note</b>: osTicket creates four Help Topics (Feedback, General Inquiry, Report a Problem, and Report a Problem / Access Issue) by default</li>
    <li><img src="https://github.com/RogericHarper44/post-install-config/assets/168601987/93bc5325-1984-41d7-9e35-bf75bac9361a"
/></li>
  </ul>
  <li>We will create four different Help Topics based on the potential serverity a ticket could have, from highest to lowest priority:</li>
  <ol>
    <li>Business Critical Outage</li>
    <li>Personal Computer Issues </li>
    <li>Equipment Request</li>
    <li>Password Reset</li>
  </ol>
  <li>Example of entering credentials for the Help Topic "Equipment Request," click on <b>Add Topic</b> to create the Help Topic</li>
  <ul>
    <li><img src="https://github.com/RogericHarper44/post-install-config/assets/168601987/68627f0e-7180-41b4-a2cf-1a4890e5ecdc"
/></li>
  </ul>
  
</ul>
  
</p>

</br>

<h3>Further Reading and Manual</h3>
<ul>
  <li>This concludes to basics of osTicket configuration, but further information and research on the features of osTicket can be found in the official online doccumentation <a href= "https://docs.osticket.com/en/latest/index.html">here</a></li>
</ul>

<br/>

<h3 align = "right">Next Tutorial - <a href = "https://github.com/ColtonTrauCC/ticket-lifecycle">osTicket: Ticket Lifecycle Examples</a></h3>

<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
<h1>osTicket - Post-Installation Configuration</h1>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- PHP
- osTicket (Help Desk Ticketing System)
<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Configuration Steps</h2>

After succesfully installing osTicket it is now time to make some adjustments and configurations to be able to use it as a proper ticketing system. It's important to mention that I alternate between the Admin and Agent panels, each capable of different configurations. You can determine the active panel by checking the upper right corner of the osTicket interface. If it displays "Agent Panel," it means the Admin panel is currently active, and vice versa.

The initial action is to establish a fresh role named "Supreme Admin." To generate this role, access the Admin panel > Agents > Roles. When creating the role make sure to give it full-access by checking all the boxes under the permissions tab and then save the changes made. 

![image](https://github.com/ricmarcano/osTicket-post-installation/assets/141169092/08af011f-d12b-4a60-9c8c-25384ee2f7ed)
![image](https://github.com/ricmarcano/osTicket-post-installation/assets/141169092/2415811e-c291-4aae-99d8-055e22d5c115)

Next step is to configure a Department. Admin panel > Agents > Department. Click "Add New Department" and make sure to name it "System Administrators". Departments are where tickets are routed through in Help Desk and there are many distinct settings that can be set for each one.

![image](https://github.com/ricmarcano/osTicket-post-installation/assets/141169092/6037f102-aff6-4a26-bda8-17bbfb90973f)
![image](https://github.com/ricmarcano/osTicket-post-installation/assets/141169092/aebbf166-6863-4b67-8dfa-23a9ab4960a3)

After creating a Department it's time to establish a new Team to complement the existing "Level I Support" Team in osTicket. To achieve this, access the Admin panel > Agents > Teams section and introduce "Level II Support". Teams enable the consolidation of Agents from various Departments to address specific issues or users through Help Topics or Ticket Filters, overriding Department rules and allowing, for instance, specialization in product-related support.

![image](https://github.com/ricmarcano/osTicket-post-installation/assets/141169092/d29eb853-26b7-49fe-9376-1bd150bec721)
![image](https://github.com/ricmarcano/osTicket-post-installation/assets/141169092/83d8d7bc-79e5-43cf-9b98-726b8790445e)

NOTE: Make sure to allow everyone to create tickets by navigating to Admin Panel > Settings > Users > Settings and making sure the "Registration Required" box is unchecked 

![image](https://github.com/ricmarcano/osTicket-post-installation/assets/141169092/56dd3fb8-7daf-419e-a914-67369fae6eb3)

It's necessary to generate new Agents who will be the ones resposible for handling tickets in the queue. To achieve this, access the Admin panel > Agents and select "Add New Agent," and establish account credentials for each Agent; for instance, in this scenario, Agents Jess and James Lee are being created.

![image](https://github.com/ricmarcano/osTicket-post-installation/assets/141169092/69a78a49-606b-4799-abe0-ade3acdd8ed3)
![image](https://github.com/ricmarcano/osTicket-post-installation/assets/141169092/3f866a61-cc8d-4def-8d9a-d569ea718f69)
![image](https://github.com/ricmarcano/osTicket-post-installation/assets/141169092/e26aeec7-ea28-4d16-acb5-f51fa6dad999)

Fresh Users will be generated to enable ticket creation, which Agents can subsequently receive and assess. To accomplish this, access the Agents panel > Users choose "Add User," and establish the required account credentials for each new user; in this instance, Haley and Kenny have been added.

![image](https://github.com/ricmarcano/osTicket-post-installation/assets/141169092/5cba0c31-79e8-4e4f-9a58-45a6a88e5412)
![image](https://github.com/ricmarcano/osTicket-post-installation/assets/141169092/88c4b2fe-cf4e-478a-9057-ee41b0c10878)
![image](https://github.com/ricmarcano/osTicket-post-installation/assets/141169092/c0f4ab99-715a-4b7f-b7b1-6380b84a3f71)

Service Level Agreements (SLAs) need to be established to classify tickets based on their impact levels. To create these new SLAs, enter the Admin panel > Manage > SLA and generate any necessary SLAs. In this particular case, SEV-A, SEV-B, and SEV-C have been generated to categorize tickets requiring resolution within 1 hour(24/7), 4 hours(24/7), and 8 hours (Bussiness hours)  respectively.

![image](https://github.com/ricmarcano/osTicket-post-installation/assets/141169092/d0c752dc-024e-4bda-b0e8-5226031f4552)
![image](https://github.com/ricmarcano/osTicket-post-installation/assets/141169092/14016463-f4ad-488e-ac6f-2afc0590098d)
![image](https://github.com/ricmarcano/osTicket-post-installation/assets/141169092/91dbf8be-053e-481f-aefd-af0e05d69e19)

Lastly, it's essential to generate Help Topics to guide users in choosing a suitable category that outlines their issue, aiding Agents in understanding the problem described in the ticket. To create a fresh Help Topic, go to Admin panel > Manage > Help Topics, and opt for "Add New Help Topic." In this instance, I have included the following topics for future ticket creation: Business Critical Outage, Personal Computer Issues, Equipment Reset, and Password Request.

![image](https://github.com/ricmarcano/osTicket-post-installation/assets/141169092/16871982-2e0a-42ff-abba-a643a8fe6da9)
![image](https://github.com/ricmarcano/osTicket-post-installation/assets/141169092/6930efd7-1aa4-43a0-a1ab-b048759a15ae)
![image](https://github.com/ricmarcano/osTicket-post-installation/assets/141169092/9da7f28b-b613-4067-99bd-434dd18840ea)

Congratulations! osTicket is now ready to function as a complete ticketing system.

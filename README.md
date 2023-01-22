<p align="center">
<img src="https://i.imgur.com/5c69OK7.png" alt="AD File Sharing"/>
</p>

<h1>Network-File-Shares-and-Permissions</h1>
In this tutorial, we observe how files and permissions work. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Domain Controller/Client Machine)
- Remote Desktop
- Shared Network Files

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

</p>
<p>
Setting up shared network files and permissions will be the focus of this lab. Certain files will have specific permissions when we create folders in the DC-1 VM and share them over the network. A few files will only be accessible to certain persons. Let's start now. Create 4 folders in the c:/ drive on the DC-1 machine first. 'read-access,"read/write access,' 'no access,' and 'accounting'.
</p>
<br />

<p>
<img src="https://i.imgur.com/ZkmVtWg.png" height="80%" width="80%" alt="Created 4 folders"/>
</p>

<p>
To enable the client-1 machine to view the folders after they have been made, share them across the network. The DC-1 folders' permissions can also be modified. Set the folders' permissions appropriately. For domain users, "read-access" should have read-only privileges, and "read/write access" should have read/write privileges. Finally, "no-access" should only be able to be viewed and written to by domain admins. We will get back to the "accounting" folder later in this tutorial.
</p>
<br />

<p>
<img src="https://i.imgur.com/VwqbFhR.png" height="80%" width="80%" alt="Giving permissions to folders"/>
</p>

<p>
<img src="https://i.imgur.com/VyDtiST.png" height="80%" width="80%" alt="Domain Users Permissions"/>
</p>

<p>
We can test the shared files we just established by logging onto the client computer using a normal user account. You can see that the permissions we set are effective.
</p>

<p>
<img src="https://i.imgur.com/hvOQtgq.png" height="80%" width="80%" alt="Permissions Effective"/>
</p>

<p>
Re-enter the DC-1 VM. Create a security group called "Accountants" in ADUC. We can do so by Creating a new OU, then creating a new group inside of that OU. 
</p>

<p>
<img src="https://i.imgur.com/Ei2j9ua.png" height="80%" width="80%" alt="Creating accountants security group"/>
</p>

<p>
<img src="https://i.imgur.com/cod64rQ.png" height="80%" width="80%" alt="Accountants Security Group"/>
</p>

<p>
Only users belonging to this group will have access to the "accountants" folder. Similar to what we did in the previous section, we must share the "Accountants" folder; however, this time, we will only share it with the group of accountants. This folder won't be accessible to normal users. A user would need to be a member of the "Accountants" security group if we wanted to grant them access to the accounting folder.
</p>

<p>
<img src="https://i.imgur.com/I1EoUgl.png" height="80%" width="80%" alt="Accountants Permissions"/>
</p>

<p>
<img src="https://i.imgur.com/3dAAHsD.png" height="80%" width="80%" alt="Permissions Effective"/>
</p>

<p>
If we were to grant a member access to the accounting folder, the followng can be observed.
</p>

<p>
<img src="https://i.imgur.com/RkKKQ72.png" height="80%" width="80%" alt="Permissions Effective"/>
</p>



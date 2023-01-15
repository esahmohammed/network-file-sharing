<p align="center">
<img src="https://i.imgur.com/AeiqMDZ.png" alt="Traffic Examination"/>
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
<img src="https://i.imgur.com/ZkmVtWg.png" height="50%" width="50%" alt="Created 4 folders"/>
</p>

<p>
To enable the client-1 machine to view the folders after they have been made, share them across the network. The DC-1 folders' permissions can also be modified. Set the folders' permissions appropriately. For domain users, "read-access" should have read-only privileges, and "read/write access" should have read/write privileges. Finally, "no-access" should only be able to be viewed and written to by domain admins. We will get back to the "accounting" folder later in this tutorial.
</p>
<br />

<p>
<img src="https://i.imgur.com/ZkmVtWg.png" height="50%" width="50%" alt="Created 4 folders"/>
</p>

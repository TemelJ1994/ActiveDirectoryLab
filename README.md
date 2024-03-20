<h1>Active Directory Lab</h1>



<h2>Description</h2>
This project consist of me setting a basic home lab running Active Directory with Oracle VirtualBox and adding users with PowerShell.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Oracle VirutalBoxy</b>
- <b>Windows 10 ISO</b>
- <b>Windows Server 2019</b>


<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Lab walk-through:</h2>

<p align="center">
Setup virtual box and create Domain Controller VM: <br/>
<img src="create_DC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
- created a domain controller to have 2 NICs, one for the internet and another for the internal network
<br />
<br />
<p align="center">
Run the VM and install the Windows server 2019 ISO:  <br/>
<img src="setup_winserver_2019.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="setup_winserver_2019gui.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="windowsserver_install.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Give default administrator account a password and login: <br/>
<img src="admin_default_p.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<p align="center">
Setup Ipv4 Addressing for the internal network:  <br/>
<img src="assign_ip.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install Active direcory Domain services and create domain:  <br/>
<img src="servermanager.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="install_roles.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="install_ADservices.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Process takes time to complete:  <br/>
<img src="install_ADservices_progress.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Post deployment configuration promote server:  <br/>
<img src="promote_server_domain1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="promote_server_domain2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create an Organzational Unit in Active directory users and computers :  <br/>
<img src="OU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Created new user in Admin folder:  <br/>
<img src="create_admin_user.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="create_admin_user2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Make created user a domain admin :  <br/>
<img src="add_user_to_admin2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="add_user_to_admin.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<br />
<br />
Sign in to new created admin account:  <br/>
<img src="signin-to-admin.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install and configure RAS/NAT for client computers:  <br/>
<img src="install_ras_nat1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="routing_and_remote_access1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="routing_and_remote_access2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="Nat_interface.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install DHCP server on DC:  <br/>
<img src="Install_DHCPserver.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure new DHCP scope:  <br/>
<img src="ipv4_scope1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="DHCP_scope.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Downloaded a custom PowerShell script that generates names and creates user accounts:  <br/>
[download script file here](https://github.com/joshmadakor1/AD_PS)
<br />
<br />
added a user to the generate name text file:  <br/>
<img src="add_name_generatedfile.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Run Powershell script:  <br/>
<img src="change_directory.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="run_script.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Open AD users and computers to check creation of users:  <br/>
<img src="find_created_users_AD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="find_created_users_AD2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="find_created_users_AD3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create new client VM change network settings to internal network:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create Windows 10 virtual client and configure Internet access:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

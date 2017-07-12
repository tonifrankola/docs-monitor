---
Title: Miscellaneous
Author: Andrea Budisa
Description: This article contains various miscellaneous questions and answers related to SysKit Monitor.
Date: 29/06/17
---
### Is it possible to remove a specific user from the reports?

You can remove a user from the filters for the reports that have already been captured.

If you wish to disable a user for monitoring, select __File__ > __Manage__ > __Users and Groups__, find the user you want to disable, double click on the user, and in the new dialog box, uncheck __Monitor activities for this user__.

This will exclude the user from the monitoring process.

### Can the software report on Citrix license usage?

Yes, you can track Citrix concurrent usage in detail.

These reports are under __User Reports__ > __Concurrent Usage Reports__.

If you select Concurrent Users per Day, you will see the usage of the farm for every day of the month. Clicking Concurrent Usage per Hour will enable you to see the time of the day when the licenses are most heavily used. By selecting the last Concurrent Usage report - Users per Hour—Details, you will see the usernames that are consuming your licenses.

### I am having problems running the application when User Access Control (UAC) is enabled.

1. Locate the SysKit Monitor installation directory in Program Files and find the __SysKitMonitor.exe__.   
(usually: C:/Program Files/SysKit/Monitor/)
2. Create a shortcut of that file on the desktop.
3. Execute the application by right-clicking and choosing __Run as administrator__.
4. UAC will prompt you to run as admin, and SysKit Monitor will start initializing.

> __Please Note!__ You are required to create a shortcut directly from the file in the installation directory, not from the shortcut in the Start menu.

### How can I check which database SysKit Monitor is using?

In __SysKit Monitor__, select __File__ > __Help__ > __About SysKit Monitor__, and then you will get something like the following:

    Database type: SQL  
    Integrated security: No  
    Assembly version: 8.0.0.xxxxx  
    Database version: 8.0.0  
    Service account: DOMAIN\syskitmonitor_user  
    Connection string: Server=__SQLSERVER__ or __(LocalDB)\.\SysKitMonitor__;Database=SysKit_Monitor_database;Trusted_Connection=yes; Asynchronous Processing=true;

This means that SysKit Monitor is using the SQL Server with the Windows integrated authentication. Please, send this data to us when we request you to do so.

### Should SysKit Monitor only be opened on the server console, or is it ok to access it through a RD session or XenApp session? Can I access the console from my workstation?

The application will work on both the console and the RDP/ICA session.  
Alternatively you can use the SysKit Monitor from your workstation if you wish to. In this case, you don’t need to open the session to the server. The workstation needs to be on the same subnet as the SQL Server, because the application will contact the SQL Server for data.

To configure the admin console on the workstation, copy the installation folder of the application (the default is in C:/Program files/SysKit/Monitor/). Then create a shortcut on the desktop that will point to __SysKitMonitor.exe.__

If you are using the same user account on the workstation as on the RD/XenApp server, the application will work fine. However, if the user is different, you will need to allow that user read/write privileges on the SysKit Monitor database on the SQL Server.

### I am having a problem installing the SysKit Monitor Web App on my server (Error code 80040154).

When installing or upgrading SysKit Monitor Web App you may encounter the following error:

    System.Runtime.InteropServices.COMException (0x80040154): Retrieving the COM class factory for component with CLSID {2B72133B-3F5B-4602-8952-803546CE3344} failed due to the following error: 80040154

This particular issue requires Internet Information Services (IIS) to be reinstalled. Please note that you are not advised to follow these instructions if you have other web instances installed on server besides the SysKit Monitor Web Application. In that case, we recommend you to contact our support team.

To fix the problem follow this steps:

1. In __Server Manager__, navigate to __Manage__ > __Remove Roles and Features__.
2. The __Remove Roles and Features Wizard__ will open. Click __Server Selection__ and choose the server where SysKit Monitor Web App will be installed, then click __Next__.
3. Under __Server Roles__, uncheck __Web Server (IIS) check box__ and click __Next__.
4. Under __Features__, just click __Next__.
5. Under __Confirmation__, click __When removal is completed__, then click __Close__. Restart the server if needed.

6. After the server restart, in __Server Manager__, navigate to __Manage__ > __Add Roles and Features__.
7. Click __Installation Type__, select the __Role-based or feature-based installation__ option and then click __Next__.
8. Under __Server Selection__, choose __Select a server from the server pool__.
9. Choose the server where you will be installing SysKit Monitor Web App and click __Next__.
10. Under __Server Roles__, select the __Web Server (IIS)__ role and then click on the __Add Features__ button. Click __Next__ to proceed.
11. Under __Features__, just click __Next__.
12. Under __Web Server Role__, click __Next__.
13. Under __Role Services__, click __Next__.
14. Under __Confirmation__, click __Install__ and when installation is completed click __Close__. Restart the server again if needed.

Now you can install SysKit Monitor Web App and start monitoring your servers!
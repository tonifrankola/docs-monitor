---
Title: Configure SysKit Monitor for Citrix XenApp 6.0/6.5 Published Application monitoring
Author: Andrea Budisa
Description: This article describes how to configure your server to monitor Citrix Published Applications with the SysKit Monitor.
Date: 29/06/17
---
In order for monitoring to be successful, these are the steps you will have to perform on __each Citrix XenApp Server__ where you run published applications.

### Enable the Remote Management

1. Run the __Server Manager__ and click on the __Configure Server Manager Remote Management__.
2. In the newly opened dialog, check in the __Enable remote management of this server from other computers__ option and click __OK__ to finish.
3. Alternatively, you can verify with PowerShell that WinRM is configured properly. Just open the PowerShell and type in __winrm quickconfig__.

   If you received access denied error run the PowerShell as Administrator.
   Otherwise, you will receive the message that the WinRM is already set up and running on this machine.
4. Confirm __Yes__ that you want to create a WinRM listener and enable the WinRM firewall exception.

### Add SysKit Monitor service user to the Citrix Farm Administrators group on the XenApp management server

1. Navigate to the __Start__ > __Administrative Tools__ > __Citrix__ > __Management Consoles__ > __Citrix AppCenter__.
2. Expand the __Citrix Resources__ section and the __XenApp__ subsection. Choose the Citrix farm and click on the __Administrators__ group.
3. Right click on the Administrators group, choose __New__ and select __Add Administrator__.
4. In the Add Citrix Administrator wizard, change the directory type to the __Operating System User Selector__ and click on the __Add…__ button.
5. Set the Object Types to __Users or Groups__ and the Locations to __Entire Directory__.
6. Enter the name of the __service user__ that you would like to add and click __OK__. After you added the chosen service user, click __OK__ and then __Next__.
7. In the last step of the wizard, choose the __View Only__ privilege level for the newly added administrator.

Your Citrix Management Server is now configured for the SysKit Monitor Published Applications monitoring.

__In case of any difficulties during the configuration feel free to [contact](https://www.syskit.com/contact-us) our support team__.

See [Configure SysKit Monitor for Citrix XenApp 5 Published Application monitoring](#internal/how-to/citrix-xenapp/monitor-citrix-xenapp5-published-applications) to learn more.  
See [Monitor Citrix Published Applications](#internal/how-to/citrix-xenapp/monitor-citrix-published-applications) to learn more.
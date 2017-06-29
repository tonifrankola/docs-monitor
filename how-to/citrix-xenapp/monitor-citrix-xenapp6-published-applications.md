---
Title: Configure SysKit for Citrix XenApp 6.0/6.5 Published Application monitoring
Author: Andrea Budisa
Description: This article describes how to configure your server to monitor Citrix Published Applications with the SysKit Monitor.
Date: 29/06/17
---
In order for monitoring to be successful, these are the steps you will have to perform on __each Citrix XenApp Server__ where you run published applications.

### Enable the Remote Management

1. Run the __Server Manager__ and click on the __Configure Server Manager Remote Management__.
1. Check in the __Enable remote management of this server from other computers__ option and click __OK__ to finish.
1. Alternatively, verify in PowerShell that WinRM is configured properly, open powershell and type in winrm quickconfig.

If you received access denied error run PowerShell as Administrator.

1. Confirm __Yes__ that you want enable to create WinRM listener and create firewall exception.

### Add SysKit Service User to the Citrix Farm Administrators group on the XenApp management server

1. Navigate to the __Start__ > __Administrative Tools__ > __Citrix__ > __Management Consoles__ > __Citrix AppCenter__.
1. Expand the __Citrix Resources__ section and the __XenApp__ subsection. Choose the Citrix farm and click on the __Administrators__ group.
1. Right click on Administrators group, choose __New__ and select __Add Administrator__.
1. Change the directory type to the __Operating System User Selector__ and click on the __Add…__ button in the first step of the Add Citrix Administrator wizard.
1. Set the Object Types to __Users or Groups__ and the Location to __Entire Directory__.
1. Enter the name of a __service user__ that you would like to add and click __OK__. After you added the chosen service user, click __OK__ and then __Next__.
1. In the second step of the Add Citrix Administrator wizard choose the __View Only__ privilege level for the newly added administrator.

Your Citrix Management Server is now configured for the SysKit Published Applications monitoring.

__In case of any difficulties during the configuration feel free to [contact](#internal/how-to/citrix-xenapp/monitor-citrix-xenapp6-published-applications/contact-us) our support team__.

See [Configure SysKit Monitor for Citrix XenApp 5 Published Application monitoring](#internal/how-to/citrix-xenapp/monitor-citrix-xenapp6-published-applications/configure-syskit-for-citrix-xenapp5-published-application-monitoring) to learn more.

See [Monitor Citrix Published Applications](#internal/how-to/citrix-xenapp/monitor-citrix-xenapp6-published-applications/monitor-citrix-published-applications) to learn more.
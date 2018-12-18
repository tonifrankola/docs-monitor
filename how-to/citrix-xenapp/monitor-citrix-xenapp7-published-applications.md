---
title: Configure SysKit Monitor for Citrix XenApp 7.x Published Application monitoring
author: Andrea Budisa
description: This article describes how to configure your server to monitor Citrix Published Applications with the SysKit Monitor.
date: 17/12/18
---
In order for Citrix XenApp 7.x Published Application monitoring to be successful, here are the steps you need to perform on __each Delivery Controller server__, which is responsible for brokering and optimizing user connections and access.

### Enable the Remote Management

1. Run the __Server Manager__ and click on the __Configure Server Manager Remote Management__.
2. In the newly opened dialog, check in the __Enable remote management of this server from other computers__ option and click __OK__ to finish.
3. Alternatively, you can verify with PowerShell that WinRM is configured properly. Just open the PowerShell and type in __winrm quickconfig__.

   If you received access denied error run the PowerShell as Administrator.
   Otherwise, you will receive the message that the WinRM is already set up and running on this machine.
4. Confirm __Yes__ that you want to create a WinRM listener and enable the WinRM firewall exception.

### Add SysKit Monitor service user to the Citrix Farm Administrators group on the Delivery Controller server

1. Navigate to the __Start__ > __Citrix__ > __Citrix Studio__ and choose the Citrix farm.
2. Expand the __Configuration__ section and right click the __Administrators__ subsection.
3. Select the __Create Administrator__ option from the right menu and the wizard will open.
4. In the __Add Citrix Administrator__ wizard, select __Browse...__ and set the Object Type to __Users or Groups__ and the Location to __Entire Directory__.
5. Enter the name of the __service user__ that you would like to add and click __OK__. After you added the service user, click __OK__ and then __Next__.
6. In the next step of the wizard, choose the __Read Only Administrator__ privilege level for the newly added administrator.

   > __Please note!__ You need to perform this on __all the Delivery Controller servers__ in your environment.

After you adjust the privileges on all the Delivery Controller servers, your Citrix environment will be configured for the SysKit Monitor Published Applications monitoring.

__In case of any difficulties during the configuration feel free to [contact](https://www.syskit.com/company/contact-us) our support team__.

Read more on how to [add Citrix servers to monitoring](#internal/how-to/computers/add-citrix-servers) to properly collect all the data.
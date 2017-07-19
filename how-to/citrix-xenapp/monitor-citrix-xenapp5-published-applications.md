---
title: Configure SysKit Monitor for Citrix XenApp 5 Published Application monitoring
author: Andrea Budisa
description: This article describes how to configure your server to monitor Citrix Published Applications with the SysKit Monitor.
date: 29/06/17
---
In order for monitoring to be successful these are the steps you will have to perform on your __Citrix Management Server__.

### Install Citrix XenApp 5.0 SDK

1. [Download the SDK](http://www.citrix.com/static/cdn/archivedsdks/mfcom/5.0/mpssdk.msi) from Citrix web site. 
   > __Please note!__ Turn off your User Account Control in order for installation to be successful.

2. Follow the __Installation Wizard__ steps.
3. Make sure that the __Register remote MFCOM server__ option is checked in.
4. Enter the __Citrix Management Server__ name and click __Next__ to proceed and finish the installation.

### Add SysKit Monitor service user to the Citrix Farm Administrators group

1. Navigate to the __Start__ > __Citrix__ > __Management Consoles__ > __Access Management Console__.
2. Expand the __Citrix Resources__ section and the __XenApp__ subsection. Choose the Citrix farm and click on the __Administrators__ group.
3. Right click on Administrators group, choose __New__ and select __Add Administrator__.
4. In the Add Citrix Administrator wizard, change the directory type to the __Operating System User Selector__ and click on the __Add…__ button.
5. Set the Object Types to __Users or Groups__ and the Locations to __Entire Directory__.
6. Enter the name of the __service user__ that you would like to add and click __OK__. After you added the chosen service user, click __OK__ and then __Next__.
7. In the last step of the wizard, choose the __View Only__ privilege level for the newly added administrator.

### Add SysKit Monitor service user to the Component Services Administrators

1. Start the __Component Services__ by typing in the __dcomcnfg__ in the Run window and pressing enter.
2. Expand the __Component Services__ section and __Computers__ subsection. Right click on the __My Computer__ and select __Properties__.
3. Select the __COM Security__ tab and click the __Edit Limits...__ button.
4. In the __Launch and Activation Permission__ dialog, click the __Add__ button and type in the name of the service user you want add the permissions to. Click __OK__ to proceed.
5. Select the newly added service user and grant him the __Local Launch__ and __Remote Launch__ permissions. Click __OK__ to finish.
6. Navigate to the __Default Properties__ tab and change the Default Impersonation Level to __Impersonate__. Click __OK__ to finish.

Your Citrix Management Server is now configured for the SysKit Monitor Published Applications monitoring.

__In case of any difficulties during the configuration feel free to [contact](https://www.syskit.com/contact-us) our support team__.

See [Configure SysKit Monitor for Citrix XenApp 6.0/6.5 Published Application monitoring](#internal/how-to/citrix-xenapp/monitor-citrix-xenapp6-published-applications) to learn more.   
See [Monitor Citrix Published Applications](#internal/how-to/citrix-xenapp/monitor-citrix-published-applications) to learn more.
---
Title: Configure SysKit Monitor for Citrix XenApp 5 Published Application monitoring
Author: Andrea Budisa
Description: This article describes how to configure your server to monitor Citrix Published Applications with the SysKit Monitor.
Date: 29/06/17
---
In order for monitoring to be successful these are the steps you will have to perform on your __Citrix Management Server__.

### Install Citrix XenApp 5.0 SDK

1. [Download the SDK](http://www.citrix.com/static/cdn/archivedsdks/mfcom/5.0/mpssdk.msi) from Citrix web site. __Please note! Turn off your User Account Control in order for installation to be successful__.
1. Follow the __Installation Wizard__ steps.
1. Make sure that “__Register remote MFCOM server__” option is checked in.
1. Enter the __Citrix Management Server__ name and click __Next__ to proceed and finish the installation.

### Add SysKit Monitor Service User to the Citrix Farm Administrators group

1. Navigate to the __Start__ > __Citrix__ > __Management Consoles__ > __Access Management Console__.
1. Expand the __Citrix Resources__ section and the __XenApp__ subsection. Choose the Citrix farm and click on the __Administrators__ group.
1. Right click on Administrators group, choose __New__ and select __Add Administrator__.
1. Change the directory type to the __Operating System User Selector__ and click on the __Add…__ button in the first step of the Add Citrix Administrator wizard.
1. Set the Object Types to __Users or Groups__ and the Location to __Entire Directory__.
1. Enter the name of a __service user__ that you would like to add and click __OK__. After you added the chosen service user, click __OK__ and then __Next__.
1. In the second step of the Add Citrix Administrator wizard choose the __View Only__ privilege level for the newly added administrator.

### Add SysKit Monitor Service User to the Component Services Administrators

1. Run the __Component Services__. (type in the __dcomcnfg__ in the Run.. and press enter to start it)
1. Expand the __Component Services__ section and __Computers__ subsection. Right click on the __My Computer__ and select __Properties__.
1. Select the __COM Security__ tab and click on Launch and Activation Permissions __Edit Limits__.. button.
1. Click on the __Add__ button and type in the name of the service user you want add the permissions to. Click __OK__ to proceed.
1. Select the newly added service user and grant him __Remote and Local Launch__ permissions. Click __OK__ to finish.
1. Go to the __Default Properties__ tab and change the Default __Impersonation__ Level to Impersonate. Click __OK__ to finish.

Your Citrix Management Server is now configured for the SysKit Monitor Published Applications monitoring.

__In case of any difficulties during the configuration feel free to [contact](https://www.syskit.com/support/contact-us/) our support team__.

See [Configure SysKit Monitor for Citrix XenApp 6.0/6.5 Published Application monitoring](#internal/how-to/citrix-xenapp/monitor-citrix-xenapp6-published-applications) to learn more.

See [Monitor Citrix Published Applications](#internal/how-to/citrix-xenapp/monitor-citrix-published-applications) to learn more.
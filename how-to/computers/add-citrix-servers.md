---
title: Add Citrix servers to monitoring
description: This article explains how to add Citrix servers to monitoring to properly collect all the data.
author: Andrea Budisa
date: 30/6/2017
---

If you have a __Citrix 7.x environment__ and you plan to __monitor user sessions and application usage__, there are just a few easy steps that you need to follow to get started. You need to add both __Delivery Controller servers__ and __Virtual Delivery Agent servers__ to the monitoring.

1. To __add Citrix servers__ click __Add__ in the Administration ribbon and then select the __Add Computers__ option from the dropdown menu.

2. The first step of this wizard will open. Select the desired __Organization Units__ and click __Next >__ to proceed with this wizard.

3. A list of computers from the __Active Directory__ will be displayed.
   
      > __Please note!__ If you have __Citrix 7.x environment__, you need to add both __Delivery Controller servers__ and __Virtual Delivery Agent servers__ to the monitoring. If you only add the Virtual Delivery Agent servers from your Citrix infrastructure, SysKit Monitor will be __unable to collect data and the reports will be empty__.

    This wizard screen also shows the number of remaining monitoring licenses. You must have enough licenses to add the computer for monitoring, please please [contact us](https://www.syskit.com/company/contact-us) to add additional licenses. Click __Next >__ proceed. 
    
4. The __License Summary__ step shows the number of computers that will be added and the remaining licenses. Click __Next >__ to proceed.

5. In the __Adding Computers__ step, a computer status check will be performed for a list of selected computers. This functionality will provide you with more information about possible misconfigurations if the load finishes with warnings or errors.
      > __Please note!__ Your computers will be added regardless of the listed warnings or errors!

      The __Status__ column will contain a link to our help page if warnings or errors occur. If you click on the link, you will be guided through the process on how to resolve the Offline and Unauthorized computer states. When the load is finished, you will have an option to save the warnings or errors that occurred to a log file in a .pdf or excel format. Click __Close__ to exit the wizard. Afterward, a list of added computers will appear.

---
title: We have just released SysKit 2016 R2 – 8.3.0
description: This article describes all new features, improvements and bug fixes delivered in SysKit 2016 R2 – 8.3.0.
author: Andrea Budisa
date: 12/7/2017
---

We have shipped SysKit 2016 R2 – 8.3.0. This minor release brings new features and improvements.

Thanks to our hardworking SysKit team, you can now create __PowerShell Alerts__ and have the results sent to your email. The team has also done a great deal of work in __improving__ and __optimizing the overall performance__ of the application! To dig out more details, read this release note.

SysKit’s __PowerShell Script Wizard__ includes significant new features that extend its use, allowing you to effectively monitor critical and important jobs that run in your Windows-based environment. The major features are in the areas of __defining alert conditions__ and __options__ for PowerShell scripts.

Now, you can select the alert conditions based on the __column types__ that the PowerShell script returns and specify when you want to be __notified__ if the alert condition is met. SysKit will generate the __.csv file__, which contains all data __matching the applied conditions__ and trigger an alert that allows you to control the administration of your environment and respond to issues more quickly.

SysKit comes with almost __fifty new PowerShell scripts, twenty custom reports,__ and __three monitoring templates__ that are ready for you to download and explore! Awesome, isn’t it?

[Click here to download the new release.](https://www.syskit.com/products/monitor/download)

Product version: 8.3.0  
Build number: 2046  
Database version: 8.3.0

Release date: Wednesday, April 12, 2017

### SysKit’s Features

#### PowerShell Scripts

+ Run functionality is now extended with the __Run on Selected Computers__ option. This allows you to run the desired PowerShell Scripts outside their scheduled hours—__on demand__ and on __different__ computers or computer groups.
+ Run __after another script__ functionality has been improved in case an error occurs in the previous script. Execution of all following scripts will not be performed.

#### Real-Time PowerShell Alerts

+ PowerShell Script Alerts are crucial for effective monitoring of any critical and important jobs that run in a server environment. SysKit will let you know when critical errors occur if you’ve configured the alert conditions for important PowerShell Scripts.
+ The built-in PowerShell Script Wizard comes with __two new steps__:
   + __Configure Conditions__ – In this step, you can enable and configure conditions for alerts sent after the script finishes. SysKit will detect PowerShell script column types and allow real-time alerts configuration based on the defined conditions.
   + __Alert Options__ – In this step, you can choose if the alert condition is met, whether you want to be notified immediately, or if the state remains unchanged after the specified time interval has passed.
+ PowerShell Script rows that match applied conditions and have triggered an alert will be painted light yellow after the script execution. These rows will be exported to .csv format and included in the email attachment of the alert.

#### Download Scripts

+ This dialog enables you to browse through and download the available __predefined PowerShell scripts__ from Acceleratio’s __repository__. There, you can find around __fifty__ PowerShell scripts categorized by their purpose.
+ Most of the available PowerShell scripts can run on all types of servers while others are tied to a specific server role— such as __Domain Controller, IIS,__ or __Hyper-V__—or have to be executed on the local machine. It is very important to read the script description on the right side.

#### Scripts Execution Status Bar

+ SysKit’s status bar now has a new PowerShell Scripts section. You can use this progress bar to check for PowerShell scripts __execution statuses__ and determine whether the script is still __in queue__ or if it’s currently __being executed__ or was recently __executed__.

#### PowerShell Wizard

+ SysKit’s PS Wizard now supports the __CredSSP authentication__. In some cases, a PowerShell script may need to access resources outside of the remote server machine. This requires that the credentials be delegated to the target machine.

#### Monitoring Templates

+ __Import Wizard / Export Wizard__ – This dialog provides options for importing and configuring Monitoring Templates in SYSmt format as well as exporting functionality.
+ __Download Templates__ – This dialog enables you to download and import the __predefined Monitoring Templates__ from Acceleratio’s __repository__. There, you can find three monitoring templates that are tied to a specific server role, such as __SharePoint, Citrix,__ or __Hyper-V__.

#### Download Custom Reports

This dialog enables you to download and import the __predefined custom reports__ from Acceleratio’s __repository__. There, you can find around __twenty__ custom reports created for various purposes and categorized by the data type they display.

### Improvements

+ Improved the __Add Computers__ wizard with an additional step in which the computer __status check__ is performed for a list of selected computers. This functionality provides the user with more information about possible misconfigurations if the load finishes with warning or errors.
+ New and improved __export__ of the __snapshot differences__ and __all data__. With the __Export to XLSX__ option in the Compare Result dialog, you can easily export the differences or all data to excel.
+ __Threshold lines with color ranges__ were added to the __Detailed Analysis__ report in the Performance Reports. The specified warning and critical thresholds are now visualized.
+ All export formats are now implemented in __only one button__! Just select the desired file format when saving.
+ Real-time alerts now contain an additional information – the __computer group membership__.
+ SysKit’s splash screen now has a new and exciting __animation__!
+ SysKit’s start screen is now improved with a new icon and some basic tips.
+ A new __info bar__ now appears on the reports when the Aggregation system job is enabled. The data were sometimes confusing for users who enabled the job with no real necessity.
+ Added a __new icon__ in the AD Integration dialog if custom credentials are used for a domain.
+ The __Add Services__ step in the Template Wizard has been improved and now includes an additional column – Service Name. The wildcard option for ‘non-listed services’ now has a proper name and tooltip with an explanation.
+ The __Enter PowerShell__ step in the PowerShell Wizard now has the script modules count displayed on the right, if there are any.
+ Increased the __timeout__ option for PowerShell scripts execution to five minutes.
+ Optimization of the SysKit application’s __initialization__. Feel a great difference in the startup of the application.
+ Load time has been __optimized__ for the following performance reports: __System Overview, Dashboard,__ and __Computer Overview__.
+ Completely __refactored__ and __optimized Performance Counters__ collection. Now, it’s even better and faster! Event logging for this system job is also improved.

### Bug Fixes

+ Handled the SQL exception when the execute permission was denied on the SysKit database for a user.
+ Monitored computers count in the left navigation wasn’t refreshing correctly upon changes on the Administration tab.
+ Deletion of old User Session data was not working due to reference constraint conflicts.
+ Gateway Sessions were not collected properly due to incorrect property retrieval from WMI.
+ The Installation Wizard could not replace old .dll files and finish the configuration process while upgrading to a newer version in some cases.
+ Adding computers from untrusted domains was not working properly due to issues with SQL connectivity and data access technologies.
+ Improved logic for server deletion and cases which caused timeouts and deadlocks.
+ WMI repository consistency check was failing due to incorrect handling of returned value.
+ Fixed the issues with access granting to the SysKit application for the same usernames but in different domains.
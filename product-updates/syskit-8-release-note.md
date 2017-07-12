---
title: SysKit 2016 R2 – Monitor and script all the things!
description: This article describes all new features, improvements and bug fixes delivered in SysKit 2016 R2.
author: Andrea Budisa
date: 12/7/2017
---

We are proud to present the newest version of SysKit! It’s a major release, and our development team definitely made a conscious effort to keep getting big things done and adding another set of powerful features. Read this release note to discover all the new features and improvements.

Thanks to our hardworking SysKit team, you can now make __PowerShell reports__ and import and execute any __script__ you can think of! How does it work?

SysKit provides you with a __built-in PowerShell editor__ for writing and saving scripts. With this feature, all defined PowerShell scripts will be automatically executed with the Inventory Snapshots system job! These scripts can be assigned to a number of servers through the __Computer Groups__.

The other great new feature in SysKit is the ability to __monitor custom performance counters in real time__. With this capability, you can now __load and monitor__ every available custom performance counter from your servers. These performance counters can be assigned to a number of servers through the __Monitoring Templates__.

SysKit comes with __predefined__ Monitoring Templates for some of the most common server roles, including __SQL, IIS,__ and __SharePoint__, to get you up and running quickly with performance monitoring!

SysKit has become the ultimate tool for real-time performance monitoring and remote administration of Windows environments. Awesome, isn’t it?

We’d also like to thank all of our customers for their continued patience. We’re working hard all the time to improve things. 🙂

We’re always eager to hear your feedback and suggestions!

[Click here to download the new release.](https://www.syskit.com/products/monitor/download)

Product version: 8.0.0  
Build number: 33871  
Database version: 8.0.0

Release date: Thursday, September 15, 2016

### SysKit’s Features

#### PowerShell Reports

+ The reports within the Inventory Reports category now include a __new report subcategory__ and __endless possibilities for creating new reports__.
+ PowerShell Reports within SysKit are designed to make it as easy as possible for you to take control of and simplify the management of your Windows environments whether you are writing scripts or administering software.
+ The __built-in PowerShell wizard__ brings syntax highlighting and colors to the editor and displays the results of the commands and scripts you have run. One of the key parts of the wizard is PowerShell script error handling, which is the same as in Windows PowerShell.
+ Our built-in PowerShell wizard supports __importing__ Windows PowerShell scripts with a __.ps1 extension__.
+ Created PowerShell scripts can be tied to a __specific server role__ and can be __scheduled to run__ for specific Computer Groups.

#### Performance Reports

+ The reports within the Performance Reports category now include one __new dashboard__ and __two new reports__:
   + __System Overview__: This dashboard provides a complete overview of the server environment’s health. It consists of six tiles that display interesting graphics and information, allowing you to gain insights into workloads and alerts from multiple systems in a single view.
   + __Detailed Analysis__: This report displays the history data for monitored custom performance counters, which are assigned to computers through the Monitoring Templates. It consists of charts that display detailed statistics for the selected custom performance metrics, Date Range, and Computers.
   + __Alert Overview__: This report displays all critical and warning alerts generated within the selected Date Range. It will help you get a clear overview of all the alerts raised in your environment.

#### Administration

+ The __Administration__ part of the application now includes __two new categories__ for adding and managing:
   + __Computer Groups__: This section enables the __logical grouping__ of monitored computers, so you can manage a large number of computers more easily. The computer groups will help you assign options, like monitoring templates, for an entire group of computers instead of an individual computer.
   + __Monitoring Templates__: This section provides several __predefined__ Monitoring Templates, which are basically collections of counters to be monitored, and they include the associated rules and suggested threshold values to detect out-of-bounds conditions.
   + The __Template wizard__ enables you to create your own Monitoring Templates within which you can add and configure performance counters and the Windows Services to be monitored.

#### LocalDB

+ If you do not have a SQL Server instance installed in your server environment, the SysKit installation will offer to __install SQL Server Express 2012 LocalDB__ (free license) automatically.
+ It provides the necessary SQL Server infrastructure, enabling the application to use the database without any complex configuration.

### Improvements

+ We have optimized our code to work better with different types of timeouts that can affect our WMI queries. We’ve also added an option for detailed WMI timeout error logging.
+ The __Administration__ part of the application has been completely redesigned. Now it includes __three__ separate categories for adding and managing the monitored __Computers, Computer Groups__ and __Monitoring Templates__.
+ The __Performance Counters Aggregation__ system job aggregates the metrics data collected by hour and by day to enhance query performance and help minimize the size of the product database.
+ Use the __Counter Settings__ dialog to configure the Performance Counters system job’s collection interval and to set after how long old counter data will be aggregated, as well as deleted from the product database.
+ To help identify issues with your product data, we’re excited to introduce the __Diagnostics__ section in SysKit. It includes the following __troubleshooting options__ for monitored computers: pinging, computer status check, WMI testing, WMI repository verification, PowerShell Remoting check, SysKit Event Log exporting.

#### UX

+ The __Save to FileShare__ and __SharePoint__ options now have proper tooltips with an explanation and a direct configuration link.
+ The __Take Snapshot__ ribbon button, which triggers the Inventory Snapshots collection job, now also enables the job if it is disabled for some reason.

### Retired Features

+ __Local System Account__: This predefined option for the SysKit service account is __no longer available__. Only the Custom User account can be used to run the SysKit service.

### What is the SysKit Licensing model and how does it affect existing SysKit customers?

+ SysKit is now available in three editions (__Standard, Professional,__ and __Enterprise__), and it can be bought in __license packs__. Choose the SysKit edition that’s right for you [here](https://www.syskit.com/products/monitor/pricing/features-by-edition).
+ We are introducing a __new type of SysKit license: Subscription__. This will allow customers to have usage rights to all releases while their subscriptions are active. This license can be purchased monthly, and it is renewable.
+ Existing SysKit customers who have valid Software Assurance can upgrade to SysKit’s __full-featured Enterprise version__ at no cost.
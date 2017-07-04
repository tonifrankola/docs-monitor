---
title: Predefined Monitoring Templates
description: Predefined templates are designed to quickly get you up and running with performance monitoring for the most common server roles—SQL, IIS, SharePoint, Hyper-V, and Citrix.
author: Andrea Budisa
date: 4/7/2017
---
SysKit Monitor comes with predefined Monitoring Templates created by SysKit team according to technology’s best practices. They can be used to monitor specific servers out-of-the-box, or modified to answer the specific requirements.

The following monitoring templates are included in SysKit Monitor and come with the installation:

+ __IIS Monitoring Template__ - tracks the most critical performance counters for web server functionality.
+ __SQL Monitoring Template__ - tracks the most critical performance counters for SQL Server functionality.
+ __ShrePoint Monitoring Template__ - tracks the most critical performance counters for SharePoint farms functionality.

The monitoring templates below are located in SysKit's __repository__ and are ready for you to download and use.

+ __Hyper-V Monitoring Template__ - tracks the most critical Hyper-V counters for virtual machine management.
+ __Citrix Monitoring Template__ - tracks the most critical Citrix performance counters for XenApp and XenDesktop functionality.
+ __Distributed Cache Monitoring Template__ - tracks the most critical SharePoint performance counters for caching functionality.  
Caching functionalities, provided by the Distributed Cache service which is built on Windows Server AppFabric Cache, enable the SharePoint features to quickly retrieve data without any dependency on databases stored in SQL Server as everything is stored in memory.

  It is essential to monitor the performance counters related to __SharePoint Distributed Cache__ as the SharePoint performance relies on the provision of caching functionalities. Windows Server __AppFabric performance counters__ allow you to monitor and troubleshoot caching. There are three counter categories related to the caching features.  
  The Distributed Cache Service should also be monitored for memory management, resiliency, and availability issues.  
  This is all very important to maintain the large amounts of information on the SharePoint Server – ensure that the information is fresh and readily available for the end user.

  This template does not have defined thresholds as they greatly depend on the SharePoint farm.

See the [Monitoring Templates](#internal/get-to-know-syskit-monitor/administration/monitoring-templates) article to learn more about monitoring the custom performance counters and important services. There, you can also find instructions and useful tips on how to __download, import,__ and __apply__ monitoring templates to computers or computer groups.
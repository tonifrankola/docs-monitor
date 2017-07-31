---
title: We have just released SysKit 2016 R2 – 8.0.1
description: This article describes all improvements and bug fixes delivered in SysKit 2016 R2 – 8.0.1.
author: Andrea Budisa
date: 12/7/2017
---

We have shipped SysKit 2016 R2 – 8.0.1. It’s one of the minor releases, with a couple of bug fixes.

[Click here to download the new release.](https://www.syskit.com/products/monitor/download)

Product version: 8.0.1  
Build number: 34186  
Database version: 8.0.0

Release date: Thursday, October 6, 2016

### Bug Fixes

+ SysKit was not working properly while gathering published applications in Citrix XenDesktop 7.x environment.
+ Quick Start Guide panel, shown on the right upon starting SysKit, has been updated with new screenshots.
+ Data retrieval while opening the __Manage Users__ dialog has been enhanced and optimized.
+ Unused __domains__ couldn’t be deleted in the __Data Retention__ system job. Missing reference for Computer Groups has been added upon deletion of a domain from the product database.
+ Memory leak during retrieval of Citrix virtualized applications has been fixed.
+ __WMI diagnostics__ option on the Administration was not working when a large amount of data was retrieved.
+ Improved deletion of large numbers of servers, which caused timeouts and deadlocks.
+ In some cases, the __Configuration Wizard__ was throwing exceptions while assigning a default schema to a SysKit’s service user on a SQL Server.
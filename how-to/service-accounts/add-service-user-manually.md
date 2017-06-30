---
title: Add Service User to Local Administrators Group Manually
description: This article explains how to manually add the SysKit Monitor service user to the Local Administrators security group.
author: Andrea Budisa
date: 30/6/2017
---
1. Log on to the server you plan to monitor.

1. Open **Computer management** under Administrative tools.

1. Select **Local user** and groups and then **Groups**.

1. Double-click the **Administrators security group**.

1. Add the SysKit Monitor service user simply by clicking Add and typing the name of your SysKit Monitor **service user** (usually). Your administrator security group will look like that shown below after adding the service user.
>_**Please note!**_ *You need to repeat this procedure for every server you plan to monitor with the SysKit. If you plan to monitor multiple servers, we recommend adding the SysKit service user via [Group Policy](#internal/how-to/service-accounts/add-service-user-group-policy).*
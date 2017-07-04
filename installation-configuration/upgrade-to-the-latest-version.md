---
title: Upgrade to the Latest Version
description: This article explains how to upgrade the SysKit Monitor to the latest major version.
author: Andrea Budisa
date: 23/5/207
---
SysKit Monitor database, application settings and data will be conserved in the upgrade process.

> __Please note!__ We recommend you to perform the database backup before proceeding with the upgrade process.

1. Download the latest SysKit Monitor version and run the __SysKitMonitorSetup.exe__.
2. __Install Wizard__ will inform you that previous version of product, if detected, will be __uninstalled automatically__.
3. Once the installation is completed, the SysKit Monitor __Configuration Wizard__ will appear.  
By default, the __Yes, use the same settings and upgrade__ check box is selected. Click __Next >__ to skip the following steps and finish the Configuration Wizard. Previously stored database and service account information will be used.  
If you decide to unselect this check box, you will have to go through all the steps in the [Configuration Wizard](#internal/installation-configuration/configuration-wizard/configure-monitor), including entering the database server name and service account information.

> __Please note!__ SysKit Monitor requires configuration with a dedicated [Service Account](#internal/requirements/user-permission-requirements), so you will be prompted to enter the password for such an account.
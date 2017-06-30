---
title: Upgrade to the Latest Version
description: This article explains how to upgrade SysKit Monitor to the latest major version
author: Andrea Budisa
date: 30/6/2017
---
SysKit Monitor database, application settings and data will be conserved in the upgrade process.

>_**Please note!**_ *We recommend you to perform the database backup before proceeding with the upgrade process.*

1. Download the latest SysKit Monitor version and run the **SysKitMonitorSetup.exe**.

1. **Installation Wizard** will inform you that **previous version of product**, if detected, **will be uninstalled automatically**.

1. Once the installation is completed, the SysKit Monitor **Configuration Wizard** dialog will appear. By default, the **Yes, use the same settings and upgrade** checkbox is selected. Click **Next >** to skip the following steps and finish the Configuration wizard. Previously stored database and service account information will be used. If you decide to unselect this check box, you will have to go through all the steps in the [Configuration wizard](#internal/installation-configuration/configuration-wizard/configure-monitor), including entering the database server name and service account information.

>_**Please note!**_ *SysKit Monitor requires configuration with a dedicated [Service Account](#internal/requirements/user-permission-requirements), so you will be prompted to enter the password for such an account.*
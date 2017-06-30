---
title: Product Migration – Installation and Configuration
description: This article explains the rebranding of our three server monitoring products into a new one.
author: Andrea Budisa
date: 30/6/2017
---
This article focuses on the product migration which will help you make a smooth transition from one product to the other.

### Product Migration

We’ve decided to take our three great products, **Terminal Services Log**, **Remote Desktop Gateway Monitor** and **Server Monitoring Toolkit** to the next level by rebranding them as the even-better **SysKit 2016**.

All monitoring and reporting features remain the same with SysKit, and we’ve added **exciting new features**. 

See the [Common Tasks](#internal/common-tasks) category to learn more.

SysKit allows you to **monitor connections** to your servers made via **RD Gateway**, so you don’t need to use our Remote Desktop Gateway Monitor tool anymore. SysKit has it all.

The upgrade to SysKit for existing **Terminal Services Log** and **Remote Desktop Gateway Monitor** customers is **fully supported** through the installation and configuration wizard. Unfortunately, the upgrade to SysKit for existing **Server Monitoring Toolkit** customers is **not supported**. These customers will need to configure SysKit with a new SQL database.

### Upgrade from TSL or RDGM with SQL Compact database (embedded)

As you read in the Product Migration section, we’ve decided to take our three great products, to the next level by **rebranding** them as **SysKit**.

**Embedded databases are no longer supported in SysKit**, so if you are using your Terminal Services Log or Remote Desktop Gateway Monitor with an embedded database and want to use SysKit, you will need to **upgrade to the SQL Express database**, which is free.

This section describes **how to upgrade from an Embedded database to an SQL Server database** without losing any data. Your data will be moved from the Embedded database to the SQL Server database. The TSL or RDGM database, application settings and data will be **conserved** in the upgrade process.

#### Upgrade from Terminal Services Log

The procedure for upgrading an Embedded database to an SQL Server database is described in the next few steps:

>_**Please note!**_ *We recommend you to perform the database backup before proceeding with the upgrade process.*

1. Download the latest SysKit version and run the **SysKitSetup.exe**.
1. **Installation Wizard** will inform you that previous version of **Terminal Services Log** will be **uninstalled automatically**.
1. Go through all the steps in the Installation Wizard.
>_**Please note!**_ *If you don’t have a Microsoft SQL Server instance, it is very important to select the **Quick Install** option to install a new instance of **SQL Server Express 2012 LocalDB** (free of charge) and use it for the SysKit database.*
1. Once the installation is completed, the SysKit **Configuration Wizard** dialog will appear and offer to **upgrade** your SQL Server Compact database to an SQL Server database. Click **Next >** to continue.
1. Go through all the steps in the [Configuration Wizard](#internal/installation-configuration/configuration-wizard/configure-wizard).

#### Upgrade from Remote Desktop Gateway Monitor

The procedure for upgrading an Embedded database to an SQL Server database is described in the next few steps:

>_**Please note!** *We recommend you to perform the database backup before proceeding with the upgrade process. Locate the RDGM installation directory and find the file **ReportingDatabase.sdf** (this is the embedded database).*

1. If you are upgrading from **Remote Desktop Gateway Monitor**, the SysKit installation will not detect this product and before proceeding with further steps, you need to uninstall it in Control Panel by using the Add or Remove Programs.

1. Run the new **SysKit setup** on the server which you want to use as a central monitoring location. Go through all the steps in the [Installation Wizard].(#internal/installation-configuration/install-wizard/install-monitor)
>_**Please note!**_ *If you don’t have a Microsoft SQL Server instance, it is very important to select the **Quick Install** option to install a new instance of **SQL Server Express 2012 LocalDB** (free of charge) and use it for the SysKit database.* 

3. Keep in mind that if you installed your old version of the RDGM in a **default installation folder C:\Program Files (x86)\Acceleratio Ltd\Remote Desktop Gateway Monitor**, SysKit installation will **automatically** copy and move the old configuration files and database file to a default SysKit installation folder. Proceed to step 5.

1. **Please Note!** If you installed your old version of the RDGM in a **different folder than C:\Program Files (x86)\Acceleratio Ltd\Remote Desktop Gateway Monitor** do not skip these steps:
   * Please uncheck the **Run SysKit Configuration Wizard now** option in the last installation step and click Finish.
   * Since the SysKit has a different default installation folder, in order to be able to upgrade automatically please **copy RDGM-config.xml file** and **ReportingDatabase.sdf** file from the old installation folder to a new installation folder **C:\Program Files\Acceleratio\SysKit or C:\Program Files (x86)\Acceleratio\SysKit**. Then **rename** the RDGM-config.xml to **SysKit-config.xml**. After you have successfully copied all the necessary files and renamed the old RDGM config file, proceed to step 5.
1. Go to the Start menu and run the **SysKit Configuration Wizard**.
1. The SysKit **Configuration Wizard** will offer to **upgrade** your SQL Server Compact database to an SQL Server database. Click **Next >** to continue.
1. Go through all the steps in the [Configuration Wizard](#internal/installation-configuration/configuration-wizard/configure-monitor).

### Upgrade from TSL or RDGM with SQL Server database

#### Upgrade from Terminal Services Log

Customers who are using **Terminal Services Log** with the **SQL Server database** can easily upgrade to SysKit. The TSL database, application settings and data will be conserved in the upgrade process. 

See the article [Upgrade to the Latest Version](#internal/upgrade/upgrade-to-the-latest-version) to learn more.
 

#### Upgrade from Remote Desktop Gateway Monitor

The procedure for upgrading from the **Remote Desktop Gateway Monitor** version 3.8.7 is described in the next few steps:

1. Connect to the SQL Server with the SQL Management Studio and **backup the RDGM database**.

1. Uninstall the current version of the Remote Desktop Gateway Monitor from all servers. Users with the **Professional edition** of the RDGM, please take special care to uninstall RDGM from the **each server it was installed on**.

1. Run the new **SysKit setup** on **only ONE server** which you want to use as a central monitoring location. Run the **SysKitSetup.exe** and go through all the steps in the [Installation Wizard](#internal/installation-configuration/install-wizard/install-monitor).

1. **Please Note!** If you installed your old version of the RDGM in a **default installation folder C:\Program Files (x86)\Acceleratio Ltd\Remote Desktop Gateway Monitor**, SysKit installation will **automatically** copy and move the old configuration files to a default SysKit installation folder. Proceed to step 6.

1. **Please Note!** If you installed your old version of the RDGM in a **different folder than C:\Program Files (x86)\Acceleratio Ltd\Remote Desktop Gateway Monitor do not skip these steps:**
   * Please uncheck the **Run SysKit Configuration Wizard now** option in the last installation step and click Finish.
   * Since the SysKit has a different default installation folder, in order to be able to upgrade automatically please **copy RDGM-config.xml** file from the old installation folder to a new installation folder **C:\Program Files\Acceleratio\SysKit** or **C:\Program Files (x86)\Acceleratio\SysKit**. Then **rename** the RDGM-config.xml to **SysKit-config.xml**. After you have successfully copied and renamed the old RDGM config file, proceed to step 6.
1. Go to the Start menu and run the **SysKit Configuration Wizard**.
An automatic upgrade will be offered, select **Yes, use the same settings and upgrade**.
You will be asked to provide **Service Account** details, and next you will see a quick **Overview** of the configuration settings that will be applied.
Once the SysKit is installed and configured, you can run the application and choose whether you want to participate in the Customer Experience Improvement Program.
 
If you have any problems with upgrading from the Remote Desktop Gateway Monitor or Terminal Services Log, please [contact](https://www.syskit.com/support/contact-us/) our support team, or via chat or phone at +1 (855) 855-5071.


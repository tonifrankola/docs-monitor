---
title: Configure SysKit Monitor
desription: This article will guide you through the steps you need to perform in order to configure SysKit Monitor to work properly.
author: Andrea Budisa
date: 30/5/2017
---
Once the installation is completed, the Configuration Wizard will start. If the wizard does not start automatically after installation, you can run it manually from: __Start > All Programs > SysKit Monitor > Configuration Wizard__.

1. In Step 1, you need to choose whether to __create a new__ or to __use an existing__ database. Click __Next >__ to proceed.
   > __Please note!__ In case you already have a SysKit Monitor database, choose the __Use existing database__ option.

2. In Step 2, you need to specify the __Database server__, __Database name__ and __authentication__ that will be used. If you have more than one instance of SQL Server, type __SERVER_NAME\INSTANCE_NAME__.  
You can also browse for existing local and network SQL Servers by clicking on the __Browse__ button next to the server field. For Database name, type in the name of the database you would like to use.
   > __Please note!__ If you chose __Create new database__ and checked the __Overwrite existing database__ option in the previous step, if there is already a database with the same name, data in the original database will be overwritten.  
   If you chose __Use existing database__ in the previous step, the installation will try to connect to the existing database.

    Next, you need to define the authentication that is going to be used to connect to your database. There are two options available:

    + Windows Authentication (make sure that the service account used for configuration has the proper privileges on the SQL Server).
    + SQL Authentication (make sure that SQL authentication is enabled on the SQL Server and the account has the proper privileges on the SQL Server).

See [SQL Permissions](#internal/installation-configuration/sql-permissions) to learn more about SysKit Monitor SQL Server database requirements.

If you plan to use the SysKit in a domain environment with an in-house SQL Server, we strongly __recommend__ choosing Windows authentication. Once you have entered the correct database information, click __Test Connection__ for verification. Click __Next >__ to proceed.

3. In Step 3, you need to enter information about the Service Account that will be used for running the SysKit Monitor Service. This account will be used to gather data from your server(s). Enter the custom user account in the following format:
__DOMAIN\USERNAME__ (or __MACHINE_NAME\USERNAME__ for workgroup scenarios).

   > __Please note!__ The service user must be in the local admin group to proceed with this step. For more information about the service account configuration, read the [Add Service User to a Local Administrators Group via Group Policy](#internal/) article.

   > __Please note!__ If the software is installed on a non-domain joined machine, the service account name should be entered in the following form: __machine_name\username__.

   Click __Validate Account__ to check the credentials. To finish the Configuration Wizard, click __Next >__.

4. If you have previously chosen to install the SysKit Monitor Web application as well, you will have the __Web settings__ step enabled. Enter the details for your new IIS website and virtual folder. Also, provide the __Service Account credentials__ to configure the application pool to run under a specific user identity. Once you have entered the correct information, click __Validate Account__ for verification. Click __Next >__ to proceed.

5. In Step 5, you can view the configuration settings that will be applied.
6. In Step 6, you can view which actions the application is performing while configuring all settings.
7. In Step 7, once the SysKit Monitor is installed, you can run the application and choose whether you want to participate in the Customer Experience Improvement Program.

## Installation of SysKit Monitor Web App on a Separate Server

The SysKit Monitor Web application can be installed on the same server as the desktop application or on a __separate server__. If you choose to install the SysKit Monitor Web application __separately__, please follow the steps below.

### Installation Wizard

In the Install Wizard, on the step which allows you to choose the program features that you want to install, select to install the __web feature only__. Once the installation is completed, the Configuration Wizard will start.

### Configuration Wizard

1. You need to enter the __Database server__ and the __Database name__ that the web application will connect to. This should be the database you are using for the desktop application.  
Once you have entered the correct database information, click __Test Connection__ for verification. Click __Next >__ to proceed.

2. Enter the details for your new IIS website and virtual folder, and provide the __Service Account__ credentials to configure the application pool to run under a specific user identity. Once you have entered the correct information, click the __Validate Account__ button for verification. Click __Next >__ to proceed.
3. The next step summarizes the configuration settings that will be applied.
4. Once the SysKit Monitor Web app is installed and configured, you can run the application and choose whether you want to participate in the Customer Experience Improvement Program.

See the [SysKit Web Application](#internal/) article to learn more.

### Problems with Installation and Configuration

Most problems are related to SQL Security and SysKit Monitor Service authentication against the Active Directory or Microsoft SQL Server. If you are experiencing problems with installation, please [contact us](https://www.syskit.com/support/contact-us/). Our team will schedule a support call and help you install the SysKit Monitor remotely.
---
title: Pre-Installation Requirements
desription: This article gives you an overview of the steps you will need to perform in order to prepare your server environment for the SysKit Monitor installation.
author: Andrea Budisa
date: 26/5/2017
---
The installation process consists of a few easy steps that you need to perform in order to get the SysKit Monitor up and running.

## Configure Active Directory

SysKit Monitor requires a service account in order to run. We recommend creating a dedicated Windows account for this purpose.

+ This account needs to have administrative privileges on each server you plan to monitor. You can configure this [manually](#internal/) or via [Group Policy](#internal/).
+ This account needs to have the [Logon as a service](#internal/) privileges.

> Please note! As a best practice, we recommend setting a service user that is in the Adminstrators or Domain Admins group.

## Configure SQL Server

The Installation wizard will create a database automatically. The user running the setup wizard needs to have the proper privileges to create new databases on the SQL Server (dbcreator or sysadmin).

During configuration you will be prompted to select the authentication type for SQL Server. You can choose between __Windows integrated__ authentication and __SQL Server__ authentication.

If you are running the SysKit in a domain environment, we strongly recommend using Windows authentication. SQL Server authentication should only be used in workgroup environments or in case of security restrictions in your domain.

### Windows-integrated authentication

If you plan to use Windows authentication, we recommend using our Configuration Wizard to create and configure the SysKit database. The Active Directory (Windows service) user running the configuration wizard needs to have __dbcreator__ and __securityadmin__ privileges on the SQL Server to create and configure the database.

See [SQL Permissions](#internal/) to learn more about SysKit SQL server database requirements.   
If you cannot obtain such privileges, install the SysKit Monitor database __manually__ (or your DBA will create a DB).

___

You need to create an empty database that will be used to store the SysKit data:

1. Open the __SQL Management Studio__.
2. Select __SQL Server name > Databases__.
3. Right click __Databases__ and select __New Database__.
4. Type a name in the __Database name__ field, e.g. SysKit_Monitor.
5. On the __Options__ page, choose __Simple__ as the __Recovery Model__.
6. Click __OK__ to create a new database.

> Please note! The service user that will be used for running the SysKit Monitor Service needs to have __db_owner__ membership assigned on the newly created database. See [SQL Permissions](#internal/) to learn more.

Proceed to: [Installation Guide](#internal/)

### SQL Server authentication

SQL Server authentication is used in environments without the Active Directory domain or if the SQL Server is outside the domain. Before installing the SysKit with SQL Server authentication, you need to perform additional steps to create a SQL user, which will be used to connect to the database.

#### How to create a SQL Server login
___

To use SQL Server authentication instead of Windows authentication please do the following:
1. Connect to the SQL Server using SQL Server Management Studio.
2. Right-click on the __Security__ folder, point to __New__ and select __Login__.
3. In the new dialog box, select __SQL Server authentication__ and in Login name field type a new SQL Server login.
4. Fill in the Password and Confirm password fields.
   > __Please note!__ You need to remember the login name and password as you will use them to connect to the SQL Server using SQL Server authentication.

5. Select __Server Roles__ page on the left side and make sure the user has __dbcreator__ role.
6. Click __OK__ and return to the Configuration Wizard > Database Configuration step.
7. If you are using the existing database, expand __Databases__ folder and then expand the database which you are trying to configure.
8. Expand the __Security folder__ and then the Users folder.
9. If the Login name you created in step 3. is not in the __Users__ list, right-click the __Users__ folder and click __New user__. In the __Username__ and __Login__ name enter the same Login name from step 3.
10. Select __Membership__ page, give user __db_owner__ role and click __OK__.

See [SQL Permissions](#internal/) to learn more about SysKit Monitor SQL Server database requirements.

## Install SysKit Monitor

If you have created a service account and prepared the SQL Server, you can proceed with the SysKit Monior [Installation Wizard](#internal/).  
If you need help with the installation, please [contact us](https://www.syskit.com/support/contact-us/).
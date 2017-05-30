---
title: Create a SQL Server Login
desription: This article will guide you through the steps you need to perform to allow the user running the Configuration Wizard to login and create the database.
author: Andrea Budisa
date: 30/5/2017
---
This article covers the following scenario:
__User running the Configuration Wizard is not allowed to login on the specified SQL server.__

Error message which occurs in the Configuration Wizard: Login failed for user DOMAIN\username.

SOLUTION:

User running the Configuration Wizard is not allowed to login on the specified SQL server.

To allow this user to login and create the database please perform the following steps:

1. Connect to the SQL Server using Microsoft SQL Server Management Studio.
2. Right-click on the __Security__ folder, point to __New__ and select __Login__.
3. In the new dialog box, select __Windows authentication__ and in __Login name__ field type the user’s username in __DOMAIN\username__ format.
4. Select __Server Roles__ page on the left side and make sure the user has __`dbcreator`__ and __`securityadmin`__ roles.
5. Click __OK__ and return to the Configuration Wizard – Database Configuration step. 
6. Click __Test Connection__ button. The connection will now be successful. Please continue with the SysKit Monitor configuration.

> __Please note!__ If you are using the __SQL authentication__ to access the database, make sure to allow this user to login on the specified SQL Server, and depending on your scenario, you need to assign the following permissions:
> + __Create a new database__ – To allow the user using SQL authentication to create a new database, make sure the __`dbcreator`__ role is selected.
> + __Configure an existing database__ – To allow the user using SQL authentication to configure the existing database, make sure the __`db_owner`__ membership is assigned.
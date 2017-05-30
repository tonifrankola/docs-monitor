---
title: Create a SQL Server Database
desription: This article will guide you through the steps you need to perform to allow the user running the Configuration Wizard to configure the database and the service account.
author: Andrea Budisa
date: 30/5/2017
---
This article covers the following scenario: 
__User running Configuration Wizard does not have permission to create a database on the SQL server.__

Error message which occurs in the Configuration Wizard: Domain\username running Configuration Wizard does not have permission to create a database on the SQL server.

SOLUTION:

To allow the user running the Configuration Wizard to configure the database and the service account, please perform the following steps:

1. Connect to the SQL Server using Microsoft SQL Server Management Studio.
2. Expand the __Security__ folder and then expand the __Logins__ folder.
3. Right-click on the __user running the Configuration Wizard__ and click __Properties__.
4. Select __Server Roles__ page on the left side and make sure the user has __`dbcreator`__ and __`securityadmin`__ roles.
5. Click __OK__ and return to the Configuration Wizard.
6. Click __Retry__.
7. You will see that the database was successfully created. Click __Finish__ to complete the SysKit Monitor configuration.
 
> __Please note!__ If you are using the __SQL authentication__ to access the database, make sure to allow this user to login on the specified SQL server, and depending on your scenario, you need to assign the following permissions:
> + __Create a new database__ – To allow the user using SQL authentication to create a new database, make sure the __`dbcreator`__ role is selected.
> + __Configure an existing database__ – To allow the user using SQL authentication to configure the existing database, make sure the __`db_owner`__ membership is assigned.
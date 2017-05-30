---
title: Connect an Existing Database
desription: This article will guide you through the steps you need to perform to allow the user running the Configuration Wizard to configure the existing database and the service account.
author: Andrea Budisa
date: 30/5/2017
---
This article covers the following scenario: __The database does not exist or User running the Configuration Wizard does not have the correct privileges to connect to it.__

Error message which occurs in the Configuration Wizard: The database you have entered does not exist or DOMAIN\username running the Configuration Wizard does not have the correct priviledges to connect to it.

SOLUTION:

If the database does exist, you need to assign __`db_owner`__ role on the database to the user running the Configuration Wizard. To do so, please perform the following steps:

1. Connect to the SQL server using Microsoft SQL Server Management Studio.
2. Expand __Databases__ folder and then __expand the database__ which you are trying to configure.
3. Expand the __Security__ folder and then the __Users__ folder.
4. If the user running the Configuration Wizard is __not on the list__, right-click the Users folder, click New user and __add a new user__.
5. Right-click on the __user running the Configuration Wizard__ and select __Properties__.
6. Select __Membership__ page, give user __`db_owner`__ role and click __OK__.
7. Return to the Configuration Wizard and continue with the SysKit Monitor configuration.

> Please note! If you are using the __SQL authentication__ to access the database, make sure to allow this user to login on the specified SQL Server, and depending on your scenario, you need to assign the following permissions:
> + __Create a new database__ – To allow the user using SQL authentication to create a new database, make sure the __`dbcreator`__ role is selected.
> + __Configure an existing database__ – To allow the user using SQL authentication to configure the existing database, make sure the __`db_owner`__ membership is assigned.
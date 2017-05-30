---
title: Create a Service User Login
desription: This article will guide you through the steps you need to perform to allow the user running the Configuration Wizard to create a new database and configure the service account.
author: Andrea Budisa
date: 30/5/2017
---
This article covers the following scenario: __User running Configuration Wizard does not have permission to create a service user login on the SQL server – new database.__

Error message which occurs in the Configuration Wizard: Domain\username running Configuration Wizard does not have permission to create a service user login on the SQL Server.

SOLUTION:

To allow the user running the Configuration Wizard to configure the database and the service account, please perform the following steps:

1. Connect to the SQL server using Microsoft SQL Server Management Studio.
2. Expand the __Security__ folder and then expand the __Logins__ folder.
3. Right-click on the __user running the Configuration Wizard__ and click __Properties__.
4. Select __Server Roles__ page on the left side and make sure the user has __`dbcreator`__ and __`securityadmin`__ roles.
5. Click __OK__ and return to the Configuration Wizard.
6. Click __Retry__.
7. Click __Finish__ to complete the SysKit Monitor configuration.
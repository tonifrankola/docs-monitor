---
Title: Move database to a new server
Author: Andrea Budisa
Description: This article explains how to move the SysKit Monitor database to a new server.
Date: 29/06/17
---
Please follow these steps to move a SQL Server database to another location:

1. Stop the __SysKit Monitor Service__ on a computer where the SysKit Monitor is installed.
2. Close the SysKit Monitor application.
3. Connect to the SQL server and open the __SQL Management Studio__.
4. Locate the SysKit Monitor database and back it up to a bak file.
5. Once the backup is finished, locate the bak and copy the file to the new SQL server.
6. Restore the DB using SQL Management Studio.
7. If the restore is successful, go to the SysKit Monitor server.
8. Start the __SysKit Monitor Configuration Wizard__ on the SysKit Monitor server.
9. Uncheck the __Use the same settings and upgrade__ option.
10. Use the __existing database__ and locate the new SQL server and the old database.
11. Type in the new SQL Server instance and the database name.
12. On the next screen, type in the service user that has same permissions as the old service user.
13. Click __Finish__.

See [SQL Permissions](#internal/installation-configuration/configuration-wizard/sql-permissions/create-sql-login) to learn more about SysKit Monitor SQL server database requirements.
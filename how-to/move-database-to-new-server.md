---
Title: Move database to a new server
Author: Andrea Budisa
Description: This article explains how to move the SysKit Monitor database to a new server.
Date: 29/06/17
---
This article explains how to move the SysKit Monitor database to a new server.

Please follow these steps to move a SQL Server database to another location:

1. Stop the __SysKit Monitor Service__ on a computer where the SysKit Monitor is installed.
1. Close the SysKit Monitor application.
1. Connect to the SQL server and open __SQL Management Studio__.
1. Locate the SysKit Monitor database and back it up to a bak file.
1. Once the backup is finished, locate the bak and copy the file to the new SQL server.
1. Restore the DB using SQL Management Studio.
1. If the restore is successful, go to the SysKit Monitor server.
1. Start the __SysKit Monitor Configuration Wizard__ on the SysKit Monitor server.
1. Uncheck the __Use the same settings and upgrade__ option.
1. Use the __existing database__ and locate the new SQL server and the old database.
1. Type in the new SQL Server instance and the database name.
1. On the next screen, type in the service user that has same permissions as the old service us
er.
1. Click __Finish__.

See [SQL Permissions](#internal/how-to/move-database-to-new-server/common-sql-permission-errors) to learn more about SysKit Monitor SQL server database requirements.
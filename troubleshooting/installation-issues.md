---
Title: Installation Issues
Author: Andrea Budisa
Description: 
Date: 29/06/17
---
### Error: SysKit Monitor Service won't start or times out while starting

#### Problem:

I’m trying to install SysKit Monitor on Windows Server 2008, or Windows Server 2008 R2, and the SysKit Monitor service does not start. The following error events appear in the Windows Application log:

Timeout (30000 milliseconds) waiting for a transaction response from the ServiceName service.

or

A timeout was reached (30000 milliseconds) while waiting for the ServiceName service to connect.

or

The SysKit Monitor Service failed to start due to the following error:
‘The service did not respond to the start or control request in a timely fashion.’

#### Solution:

1. Click __Start__, click __Run__, type __regedit__, and then click __OK__.
1. Locate and then click the following registry subkey: HKEY_LOCAL_MACHINE/SYSTEM/CurrentControlSet/Control
1. In the right pane, locate the __ServicesPipeTimeout__ entry.
__Note__: If a ServicesPipeTimeout entry does not exist, you must create it. To do this, follow these steps:
  * On the __Edit menu__, point to __New__, and then click __DWORD Value__.
  * Type __ServicesPipeTimeout__ and then press ENTER.
1. Right-click __ServicesPipeTimeout__ and then click __Modify__.
1. Click __Decimal__, type __360000__, and then click __OK__.
This value represents the time in milliseconds before a service times out.
1. Restart the computer.

#### Read more on this issue:

[The service did not respond to the start or control request in a timely fashion](#internal/troubleshooting/installation-issues).

### I am getting a messagse stating "The service did not respond to the start or control request in timely fashion."

This is an issue on servers that don’t have access to the Internet. Windows Server will try to check the code signing certificate that was used to sign application executables. Allow access to the Internet for the server once and then start the service to solve the issue. Please note that it is required to do this only once; the first time, Windows will check Acceleratio’s code signing certificate, and then it will work fine.

If this is not possible, [contact us](#internal/troubleshooting/installation-issues/contact-us) and we will provide you with a certificate and the instructions on how to import the certificate to your problematic server.

### Installing SQL Server on a domain controller.

#### Problem:

I’m trying to install the SQL Server trial in our Navision server. However, I got a warning message while installing.
Warning: Rule “Computer domain controller” generated a warning! Installing SQL Server on a domain is not recommended.
Should I proceed?

#### Solution:

You have a few options here:

1. Install [SysKit Monitor with a SQL Server Express LocalDB database](#internal/troubleshooting/installation-issues/install-syskit-application). This does not require SQL Server to be installed, and you can proceed with such an installation on a domain controller.
1. You can install SQL Server on another box in your domain and then connect the server to an existing SQL server. Learn more in our [installation guide](#internal/troubleshooting/installation-issues/install-syskit-application).
3. Microsoft does not recommend installing SQL Server on a domain controller. However, if you only have a single server in your organization, you can choose to install it on top of your domain controller. Before proceeding with this operation, you should check out the [following article](https://docs.microsoft.com/en-us/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server#DC_support).

### I am getting "Cannot start SysKitMonitorService."What is wrong?

1. Try to return to the previous page using the Back button.
1. Click Next again.
1. The installation will be restarted, and the service will start.

If the service fails to start again, access the SysKitMonitorService manually from __Administrative tools__ > __Services__. If there are any further issues, [contact us](#internal/troubleshooting/installation-issues/contact-us).
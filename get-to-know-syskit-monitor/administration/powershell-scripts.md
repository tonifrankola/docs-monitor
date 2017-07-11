---
title: PowerShell Scripts
description: This article discusses the options for creating PowerShell reports and management tasks through SysKit Monitor.
author: Andrea Budisa
date: 23/6/2017
---
__PowerShell Scripts__ on the __Administration__ tab are designed to make it as easy as possible for you to take control and simplify reporting and administration of your Windows environments.  
If you navigate to Administration > PowerShell Scripts, you will find endless possibilities for the creation of new report and management scripts.  
This section is completely different from the one on Inventory Reports > PowerShell Reports. It consists of __Reports__ and __Management Tasks__ subsections within which you can __categorize the scripts__ you want to create.

## Reports

This subsection contains all PowerShell scripts that always return results in the form of __multiple columns / rows__ and are meant for reporting purposes. Saved and executed report scripts can return varying amounts of data, but these report scripts can also return __`Error`__ results for some computers.  
Reports subsection comes with __two report categories__ and __three predefined PowerShell scripts__ for you to explore:

+ __Computers by OUs__ – The script is located in the AD category. Note that it can only be executed on the Domain Controller(s) in a server environment.  
This report displays a list of all computers in a domain and their corresponding Organizational Units.
+ __Installed Features__ – The script is located in the Roles and Features category. It can be executed on any monitored computer.  
This report displays information about Windows Server features that are available for installation and installed on the target computer(s).
+ __Installed Roles__ – The script is located in the Roles and Features category. It can be executed on any monitored computer.  
This report displays information about Windows Server roles and role services that are available for installation and installed on the target computer(s).

PowerShell scripts saved as Reports, depending on the scripts’ purpose, will have multiple columns displayed, but some of the default columns are: __Computer__ on which the script was executed, __Date/Time__ at which the script was triggered, and __Status__ in which the script returned from target computers.

## Management Tasks

This subsection contains all PowerShell scripts that perform some kind of management task and only return details on whether the specified task was successfully completed or an error occurred. PowerShell scripts saved as Management Tasks will only have three columns displayed: __Computer__ on which the script was executed, __Date/Time__ at which the script was triggered, and __Status__ in which the script returned from target computers.

Error results are returned from the target computers in the following cases:

+ If executing PowerShell script(s) on target computers with lower Operating System versions, which have a certain number of cmdlets available and do not support the usage of cmdlets available in the newer OS versions.
+ If PowerShell is not installed on target computers for some reason.
+ If PSRemoting is disabled on target computers for some reason.
+ If PowerShell command timed out on target computers for some reason.
+ If user has insufficient rights on target computers.
+ If other errors are thrown by Windows PowerShell.

> __Tip!__ If an executed report or management script has the Status marked __`Error`__, you will be able to see the error message returned from the destination computer by __hovering over the column__ marked ‘Error.’ This applies to all PowerShell Scripts.

> __Tip!__ If run __after another script__ functionality is enabled and an error occurs in the previous script, execution of all following scripts will not be performed. 

All PowerShell Scripts available on the Administration tab have the __filter panel__ available to the right. It contains three filter types—__Date Range, Computer Groups,__ and __Computer__—so you can filter your data more easily. Use the __Date Range__ filter to select any day, week, month, or custom date range.

> __Please note!__ You will not be able to see any PowerShell script data outside 30 days, unless you change the [PowerShell Scripts Data Retention](#internal/get-to-know-syskit-monitor/backstage-screen/configuration/options/#data-retention) settings. The default is set to delete PowerShell script data older than 30 days.

PowerShell is known as an excellent tool for automating repetitive tasks, so you can start building your __report__ and __management__ scripts using the __PowerShell Script editor__ within SysKit Monitor. You can import PowerShell scripts into the wizard (with __.ps1__ extension only), write your own PowerShell code, and create some amazing reports and management tasks.

With the built-in PowerShell Script Wizard, you can also import and edit [PowerShell Script Modules](#internal/how-to/powershell-scripts/import-and-use-ps-script-modules) with __.ps1__ and __.psm1__ extensions. A script module allows you to use a number of rules and cmdlets in your scripts. In simple terms, a script module is just a grouping of functions and code that can be applied to a specific group of scripts. __PowerShell modules__ are actually highly recommended when writing PowerShell scripts, because they are created for applications such as Microsoft Exchange, Active Directory, VMware, etc., to manage all aspects of various applications. The PowerShell module feature within the __PowerShell Script Wizard__ allows the combining of multiple scripts to simplify code management, accessibility, and sharing.

The PowerShell Wizard also comes with __PowerShell Script Alerts__, which are crucial for effective monitoring of any critical and important jobs that run in a server environment. SysKit Monitor will let you know when critical errors occur if you’ve configured the __alert conditions__ for important PowerShell Scripts. PowerShell Script rows that __match the applied conditions__ and have __triggered an alert__ will be painted light yellow after the script executes. These rows will be exported to __.csv format__ and included in the __email attachment__ of the alert.

Read this article to learn more on how to:
## [Enhance your reporting using PowerShell Script Wizard](#internal/how-to/powershell-scripts/powershell-wizard)

#### PowerShell Scripts Ribbon

Ribbon provides a set of basic functions for managing the __created or imported__ report and management scripts.

+ __Create__ – Create a new PowerShell report or management task.
+ __Edit__ – Edit the selected PowerShell report or management task.
+ __Delete__ – Delete the selected PowerShell report or management task.
+ __Edit Trigger__ – Edit the conditions that will trigger the PowerShell script.
+ __Download Scripts__ – Download and import the predefined PowerShell scripts from Acceleratio’s repository.
+ __Refresh__ – Refresh items in the left navigation panel, filters, and main view.
+ __Default Layout__ – Reset the current layout of the main view to the default layout.
+ __Run__ – Run the selected PowerShell script on target computers.
+ __Run on Selected Computers__ – Run the selected PowerShell script outside its scheduled hours — on demand and on different computers or computer groups.
+ __Enable__ – Enable the selected PowerShell script for execution.
+ __Disable__ – Disable the selected PowerShell script for execution.
+ __Export__ – Export the script results and retrieved information to PDF, Excel, HTML, or CSV files.

#### Execution Status Bar

If you click the __Status bar__ at the lower left side of the screen, information about currently running system jobs and PowerShell scripts will be shown. You can use this progress bar to check for the PowerShell scripts’ __execution statuses__ and determine whether each script is still in the __queue__, it’s __being executed__ or it was recently __executed__.

> __Please note!__ The PowerShell status bar will always show execution history for the last five minutes.

Read these articles to learn more on how to:

## [Manage Scripts](#internal/how-to/powershell-scripts/manage-scripts)

## [Import / Export PowerShell Script](#internal/how-to/powershell-scripts/import-ps-script)

## [Import and use PowerShell script modules](#internal/how-to/powershell-scripts/import-and-use-ps-script-modules)

## [Download Scripts](#internal/how-to/powershell-scripts/download-scripts)
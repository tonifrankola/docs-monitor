---
title: Manage Scripts
description: This article describes how to manage all available PowerShell scripts that are created or imported through SysKit Monitor.
author: Andrea Budisa
date: 23/6/2017
---
This dialog shows all available PowerShell scripts created or imported through SysKit Monitor. Scripts are grouped by type to two folders, like in reports’ left navigation: Reports and Management Tasks. The script execution is performed periodically, and you are able to configure the triggers as you wish. When you configure each script according to your preferences, it will run periodically as configured. You can also manually run __specific or multiple scripts__, which will be executed at the next tick of service.

The following options are available:

+ __Run, Enable, Disable, Edit Trigger__ – previously described in the upper part.
+ __Select Computers__ – Use this option to configure the computers on which to execute the script(s).
+ __Remove__ – Use this option to delete the selected script(s).
+ __Add, Edit,__ and __Remove Category__ – Use these options to manage the created categories and subcategories for your scripts. Note that the Remove Category button will delete the whole category with all its containing scripts.
+ __Refresh__ – Use this option to refresh the dialog items and script status.

All of the available options for script configuration and execution can be managed easily with the multi-select option supported in grid-view.

The grid-view in Manage Scripts displays the following elements:

+ __Name__ – the name of the script.
+ __Triggers__ – information about the script’s execution schedule.
+ __Last Run Time__ – the last time a script was executed.
+ __Next Run Time__ – the next time a script will be executed. It depends on the configured trigger conditions.
+ __Run On__ – Indicates whether the script is configured to run on __all or specific__ computers or computer groups.

The Script icon on this dialog will change its appearance, depending on the script’s state, which can be __disabled or executing__. A green arrow will be shown while the script is executing.
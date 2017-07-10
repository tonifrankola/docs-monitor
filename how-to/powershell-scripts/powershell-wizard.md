---
title: PowerShell Wizard
description: This article outlines all necessary steps for creating report or management scripts and the successful administration of your Windows environments.
author: Andrea Budisa
date: 23/6/2017
---
We’ll break down how you can create report and management scripts in SysKit Monitor using PowerShell Script Wizard.

1. In Step 1, specify the PowerShell script type you wish to create. The wizard offers two different script types: __PowerShell Report__ and __PowerShell Management Task__.
   > __Tip!__ The first option can be useful for retrieving a wealth of information about a server’s configuration, usage, or performance. The second option is useful for performing various administration and maintenance jobs.

2. In Step 2, simply enter the PowerShell script name and select the desired category. Note that based on the script type you have selected in the previous step, your script will be added to the corresponding category. The report category option will help you categorize your reports and management tasks so you can manage large amounts of scripts more easily.  
For more advanced scripts, you can also enable the __CredSSP authentication__ to avoid double-hop problems. In cases where a PowerShell script may need to access resources outside the remote server machine, the credentials must be delegated to the target machine.  
_How to enable the CredSSP authentication_  
If the entered PS script requires the credentials to be delegated and you have enabled the __CredSSP__ option, the error dialog will be shown upon validation of the script. It will guide you on how to switch to __custom credentials__. Just click the __Configure__ button in this dialog, and the __Edit domain__ dialog will be shown. Select the __Specify credentials__ option and re-enter the service credentials.
   > __Tip!__ It is recommended that you enable the __Use credentials only for PowerShell__ option as the custom credentials are meant for authentication when monitoring computers from untrusted domains.

   See the [Configuring CredSSP for use with PowerShell](#internal/troubleshooting/credssp-for-use-with-powershell) article to learn more on how to delegate the user’s credentials through SysKit Monitor.

3. In Step 3, you will need to enter the PowerShell script you want to use to create reports or management tasks. Here you can also __import the script modules__ whose members can contain functions, variables, and more. To avoid incorrectly generated reports, the report script first needs to be tested on a selected computer. SysKit will run it against the computer that you specify.  
If you have selected the __management task__ script type in the first step, the management script will __only be validated for syntax errors__.  
__All referenced modules will also be validated in both cases__ before the wizard returns and displays the results of the script and modules you have run.  
After entering script, click Next> to see the results.
   > __Please note!__ If you have troubles with writing script, or you want to know more about PowerShell rules and limitations, please read [this article](https://technet.microsoft.com/en-us/library/bb978526.aspx).  

   See the article on the [PowerShell script modules](#internal/how-to/powershell-scripts/import-and-use-ps-script-modules) to learn more how and when to import and use script modules.

4. In Step 4, if the script and module syntax are valid, the results of the __report script__ will be returned in a grid view. Please verify whether the script returned the desired results, then continue to the next step. As mentioned previously, if you are creating a __management script__, your script will only be validated; you will not have this step.
   > __Please note!__ The approximate size of the query result can wary depending on the entered script purpose. Take into consideration that large query results can significantly increase server resource utilization.

   > __Please note!__ If an entered PowerShell query is returned without results after validation in PowerShell wizard, it cannot be saved.

5. In Step 5, you will need to select the computers you want to run the PowerShell script on.  
Created PowerShell script can be scheduled to run on:
   + All computers;
   + Specific computers; or
   + Specific computer groups.

   > __Please note!__ Query results may vary depending on the PowerShell version used on a specific computer.

6. In Step 6, you will need to specify the __conditions__ that will trigger the PowerShell script.  
The following __schedule options__ are available:
   + __Manual only__—the script will be executed only when the __Run__ button is clicked.
   + __Automatic__—the script will be executed automatically on a __defined schedule__, which has two types: __Recurrence__ or __After another script__.
   
   > __Tip!__ If the __Recurrence__ option is selected, you will be offered __several recurrence types__: one time, minutely, hourly, daily, weekly, monthly, and quarterly. Here, you can select the start date and time for the selected recurrence type.

   > __Tip!__ If the __After another script__ option is selected, you will be offered a drop-down menu that contains all PowerShell scripts available in SysKit. The script for which you configure the trigger will be executed after the script selected from the drop-down.

7. In Step 7, you can __enable__ and __configure conditions__ for alerts sent after the script finishes. SysKit will __detect and set__ the PowerShell script __column types__ and allow configuration of real-time alerts based on the __desired conditions__. A PowerShell script can return different column types. The ones that are __discoverable__ by SysKit are String, DateTime, UInt64, UInt32, Int64, Int32, Double, Boolean, and Decimal.

8. In Step 8, if the alert condition is met you can choose whether you want to be notified immediately. Alternatively, you can be notified if the state remains unchanged after the specified time interval has passed. Note: in both cases, you will receive an alert when the condition is met and you will also receive an email after everything returns to the normal state.  
SysKit will generate a __.csv file__, which contains all the data __matching the applied conditions__ and include it in the email attachment of the alert.
Here you can also select whether to send alerts to email addresses defined in the __Options__ dialog or you can specify different ones.

All created and saved PowerShell scripts, depending on the script’s type, will be added to the Administration tab > PowerShell Scripts > Reports or Management Tasks group.
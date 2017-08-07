---
title: SysKit 2016 R2 8.2.0 - Release Note
description: This article describes all new features, improvements and bug fixes delivered in SysKit 2016 R2 – 8.2.0.
author: Andrea Budisa
date: 12/7/2017
---

We have shipped SysKit 2016 R2 – 8.2.0. This minor release brings new features and improvements.

The SysKit team stepped up the capabilities of the __PowerShell Script Wizard__ with __PowerShell script modules__, and the team has continued to add features and improve other functionality in SysKit 2016 R2 – 8.2.0. We’ll highlight the features and some of the key improvements. To dig out more details, read this release note.

SysKit’s __PowerShell Script Wizard__ includes significant new features that extend its use, improve its usability, and allow you to control and manage Windows-based environments more easily and comprehensively. The major improvements are in the areas of __importing__ and __referencing__ PowerShell script __modules__ and script __scheduling__. Now you can specify the PowerShell __script type__ you wish to create and categorize the __report__ and __management__ scripts so you can more easily manage large amounts of different scripts.

[Click here to download the new release.](https://www.syskit.com/products/monitor/download)

Product version: 8.2.0  
Build number: 1060  
Database version: 8.2.0

Release date: Tuesday, December 6, 2016

### SysKit’s Features

#### PowerShell Scripts

+ PowerShell Scripts on the __Administration__ tab are designed to make it as easy as possible for you to take control and simplify __reporting__ and __administration__ of your Windows environments.
+ This category includes __two script subcategories__ and __three predefined report scripts__:
   + __Reports__ (Computers by OUs, Installed Features, Installed Roles)  
   __Computers by OUs__: This report displays a list of all computers in a domain and their corresponding Organizational Units. Note: this script needs to be executed on a Domain Controller to return valid results;  
   __Installed Features__: This report displays information about Windows Server features that are available for installation and installed on the target computer(s);   
   __Installed Roles__: This report displays information about Windows Server roles and role services that are available for installation and installed on the target computer(s).
   + The __Management Tasks__ category contains all PowerShell scripts that perform some kind of management task and only return details on whether the specified task was successfully completed or an error occurred.

#### PowerShell Wizard

+ The built-in __PowerShell Script Wizard__ comes with PowerShell __Module Manager__. You can import and edit a script module, which allows you to use a number of rules and cmdlets on your scripts.
+ The __PowerShell module__ feature within SysKit’s PowerShell Script Wizard allows combining of multiple scripts to simplify code management, accessibility, and sharing.
+ Entered script and all referenced modules are validated before the wizard returns and displays the results of the script and modules you have run.
+ Our built-in PowerShell Wizard supports __import__ of:
   + Windows PowerShell scripts with a __.ps1__ extension,
   + PowerShell Script modules with a __.ps1__ and __.psm1__ extensions.
+ Created PowerShell scripts can be __scheduled for execution__. The following schedule options are available:
   + __Manual only__ – the script will be executed manually when the Run button is clicked;
   + __Automatic__ – the script will be executed automatically on a __defined schedule__, which has two types: __Recurrence__ or __After another script__.

#### Manage Scripts

+ This dialog enables easier __management__ of all created or imported PowerShell scripts.
+ It also shows all the information about the scripts’ __execution schedule__, such as: triggers, the last and next run times, and on which computers the scripts are configured to run.

#### Import Wizard

+ This dialog provides options for __importing__ and __configuring__ PowerShell scripts in __SYSpr__ format.
+ It also detects and includes all __referenced PowerShell modules__, if there are any, while importing / exporting a report definition in SYSpr format.

#### Download Scripts

+ You can download and import the predefined PowerShell scripts from Acceleratio’s __repository__.
+ Most of the available PowerShell scripts can run on all types of servers, while others are tied to a specific server role, such as __Domain Controller, IIS,__ or __Hyper-V__.

### Improvements

+ New and improved __design of emails and alerts__ sent by SysKit.
+ With the __Duplicate Monitoring Template__ option, now you can easily create a copy of any Monitoring Template and adjust it according to your preferences.
+ Completely refactored and optimized __AD Integration__ system job. Now it’s even better and faster! Event logging for this system job is also improved.
+ Reorganized and improved __verbose event logging__ and __database log__ options that reveal detailed event entries for troubleshooting. The verbose event logging __warning__ now shows if any of the available options has been enabled.
+ Better SysKit Service account validation in the Configuration Wizard.
+ Search has been optimized through the loaded Performance Counters list in Template Wizard.
+ Loading dialogs, indicating that the application is processing user input, have been added where necessary.
+ The unnecessary condition for SQL permissions in the Configuration Wizard has been removed.
+ The __auto-growth setting__ for the SysKit database was set to a fixed number of megabytes because it can get quite large over time.

### Bug Fixes

+ Users who weren’t members of the Local Administrators security group on SysKit’s app server couldn’t start the application.
+ Deletion of old Performance Counter Alerts was not performed during the upgrade.
+ Application Concurrent Usage summarization was not working in automatic mode because of incorrect UTC time zone handling.
+ Users’ multiple simultaneous remote connections using Remote Desktop Services were not registered correctly by SysKit in some cases.
+ Citrix Gather Mode was incorrectly set for monitored Citrix servers in some cases.
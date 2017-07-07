---
Title: Exclude installation folder from antivirus scanning
Author: Andrea Budisa
Description: This article explains how to exclude installation folder from antivirus scanning on Windows Server 2008 or later.
Date: 29/06/17
---
This folder may have to be excluded from antivirus scanning when you use file-level antivirus software. If this folder is not excluded, you may see unexpected behavior. For example, you may receive “access denied” error messages.

Please configure your antivirus software to exclude the following folder from antivirus scanning:

### 64-bit version

* Drive:\Program Files (x86)\SysKit\SysKit Monitor

If you are using SysKit Monitor Data Collector, please exclude the following folder:

* Drive:\Program Files (x86)\SysKit\SysKit Monitor Data Collector

### 32-bit version

* Drive:\Program Files\SysKit\SysKit Monitor

If you are using SysKit Monitor Data Collector, please exclude the following folder:

* Drive:\Program Files\SysKit\SysKit Monitor Data Collector

> __Please note!__ The placeholder 'Drive' represents the letter of the drive on which you have the application installed. Typically, this drive letter is C.

In case you have a policy that you mustn’t exclude the whole folder, please configure your antivirus software to exclude the following file from antivirus scanning:

`SysKitMonitorService.exe`
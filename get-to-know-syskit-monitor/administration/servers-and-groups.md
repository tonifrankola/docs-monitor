---
title: Servers and Groups
description: This article outlines all the options for the successful administration of servers that are being monitored with SysKit Monitor.
author: Andrea Budisa
date: 25/5/2017
---
If you click on the __Administration__ tab in the left navigation, the
Administration – Computers section will be displayed. 

### Administration – Computers

This category contains the following elements:

Displays all monitored computers in your domain and their characteristics, such as __Status, Type,__ assigned __Computer Groups__ and __Performance Counters__ collection status. After clicking on a computer in the grid view, its details will be shown.

Monitored computers can have __one of five statuses__ in the Administration tab:

+ __Online__ – The computer is active and is currently being monitored by SysKit Monitor.
+ __Offline__ – The computer is offline and is being monitored, but SysKit Monitor is not collecting the data because the computer is unreachable.
+ __Unauthorized__ – The computer is active and being monitored, but SysKit Monitor is not collecting the data because the appropriate permissions are missing.
+ __Unknown__ – SysKit Monitor is determining the computer status.
+ __Disabled__ – The computer is not active and is not being monitored by SysKit Monitor.

The __Type__ column displays the computer type, which is automatically assigned to computers during the adding process. The type can be __Server, Gateway,__ or __Workstation__.

The __Computer Group__ column displays the name of the group to which the computer is assigned. A computer can be assigned to one or more Computer Groups. The main purpose and concept of the Computer Groups will be explained later in this article.

The __Performance Counters__ column displays the performance counters collection status for the computers in your domain. A system job can have __one of four statuses__: Started, Offline or Not Accessible, Unknown, and Disabled. See the [Performance Counters Management](#internal/) article to learn more.

The __details panel__ below the grid view displays additional information for the __selected computer__.

+ The __Identification__ section displays various status monitoring elements, such as the monitoring status within SysKit, the current computer status, the last time the computer was seen online, the last time Event log data was retrieved, the Total System Uptime, and the IP Address.
+ The __Details__ section displays more detailed information on the computer’s specifications, such as the physical memory, the operating system and its version, installed service packs, whether the computer is enabled in Active Directory, and the Organizational Unit to which it belongs.
+ The __Settings__ section displays various configuration options that have been applied, such as session thresholds information, which are used to display the warning and critical session counts on the Sessions Dashboard. It also displays the last time Performance Counters data was collected and information on all Monitoring Templates that have been applied.

### Administration – Computer Groups

This category is very similar to the previously described Computers category since it contains the same ribbon options and grid view columns. It contains more options for managing Computer Groups.

+ __Assign Computer(s) to Group__ – Quickly assign selected computers to the desired Computer Group.
+ __New Group__ – Create a new computer group.
+ __Edit Group__ – Edit the selected computer group and computers’ membership, e.g., add/remove selected computers.
+ __Delete Group__ – Delete the selected computer group.

The __Computer Groups__ category enables the __logical grouping of monitored computers__ so you can more easily manage a large number of computers. This category will help you assign options, such as __Monitoring Templates__, for an __entire group of computers__ instead of an individual computer.

See the [Monitoring Templates](#internal/) article to learn how to simplify performance monitoring for your Windows environments.

#### Administration Ribbon

Use the Administration ribbon page to change computer settings or take actions:

+ __Add__ – allows you to add new computers to monitoring.
+ __Edit__ – enables you to update the operating system and computer type and define session thresholds for the selected computer(s).  
You can __define warning and critical session thresholds__, which will then be displayed on the [Sessions Dashboard](#internal/). Session thresholds help you visualize the current statuses of your computers.  
There are __2 visual color indicators__ for computers’ sessions:
  + __Yellow__ – online computer that has reached an alarming number of users (e.g. 51 users online, the warning threshold is 50)
  + __Red__ – online computer that has reached a critical number of users (e.g. 101 users online, the warning threshold is 100)

  Adjust the values for warning and critical thresholds to match the capacity or other constraints on your computers. You can define the length of time before the __alert notification is to be repeated__ for the session alerts.  
See [Alerts section](#internal/) if you want to enable the option to receive __e-mail notifications__ if monitored computer crosses a warning and/or critical session threshold.

+ __Use In Reports__ – enables using information gathered from the currently not monitored computers in the reports. If the computer is currently disabled, by enabling this option all of the previously gathered data from this computer will be shown in the reports.
+ __Diagnostics__ – enables you to perfrom various diagnostics and to identify issues with your product data. These options will also help our developer and support teams to troubleshoot potential problems more efficiently.
+ __Remote Desktop__ – starts remote desktop session with the selected computer.
+ __Options__ – allows configuration of options for Report and Dashboard data, Alerts, Export and System Jobs.

The __Administration – Computers__ ribbon page also contains options for managing __Computer Groups__, which are listed in the navigation tree view on the left side.

+ __Assign Computer(s) to Group__ – Quickly assign selected computers to the desired Computer Group.
+ __New Group__ – Create a new computer group.

See the [Performance Counters Management](#internal/) article to learn more about managing performance counters.

> __Please note!__ In the trial version the maximum number of monitored computers is __limited to 20__.
---
title: Computer Performance
description: Computer Performance reports are used to measure server performance such as CPU, Memory usage, Disk and Network performance.
author: Andrea Budisa
date: 25/5/2017
---
This report category also includes the [Performance Dashboard](#internal/get-to-know-syskit-monitor/dashboards/performance-dashboard), which is described under Dashboards category.

## Overview

The __Overview__ report gives more detailed information for the selected computer. Values and charts in the Overview report are updated __every 60 seconds__.
The charts display a performance overview for the __last 15 minutes__, while the value next to a chart is in __real time__. The Overview report gives you more detailed information about all Hard Drives and Network Adapters on your computer. Performance Counters available on this report are similar to those in the previously mentioned Dashboard with the addition of __Computer Info__ and __Top 5 processes__ categories.

The __Top 5 processes__ category displays CPU and Memory consumption charts for the top five Windows processes according to CPU usage. This category will quickly show you which processes are consuming the most CPU time on the selected computer. It also displays process performance counters:  
__IO Operations/sec__ and the __total IOs/sec__ (IO Read and Write KB/sec).

Values and charts on the Overview report __change colors__ depending on the defined thresholds for the selected computers, which are configured through the __Monitoring Templates__ category on the Administration tab. When a chart is painted red (or yellow), it means that a threshold has been crossed for the associated performance counter. Red indicates a critical threshold, while yellow indicates a warning threshold.

__Every chart and value in this report is clickable__, which makes it very useful as an initial step in identifying performance bottlenecks and for further detailed analysis. When you click on a chart, the resulting drilldown will capture the Filter values and take you to a __more detailed history report__.

> __Please note!__ This report displays data for a single computer only.
 
Depending on whether the custom perfromance counters and important services are configured for the selected computer, there is one more category that can be visible here: [Monitoring Templates](#internal/).  
Depending on what is configured through the assigned Monitoring Template, this category can contain two subcategories: __Performance Counters__ and __Monitored Services__.

#### Performance Counters

Defined custom performance counters will be shown with __charts and values__, like other (built-in) performance counters. Every custom performance counter configured for monitoring will be displayed with its __category name__ and __instance name__.

You can create __separate__ Monitoring Templates for __Windows Services__, assign them to designated computers or computer groups according to your preferences and define actions for stopped services. Upon configuration, the Monitoring Templates category will appear on the Overview report.

#### Monitored Services

Defined Windows Services will be listed with the following columns:

+ __Name__ – The display name of the service.
+ __Start Mode__ – The startup type of the service.
+ __Logon account__ – The logon account column shows which user account the service is using to log on.
+ __Status__ – The service status column, shows the current status of all monitored services configured to run on the selected computer and is updated every 30 seconds.

If any of monitored services has the service status __`Stopped`__, this means, depending on the defined actions, that SysKit has tried to restart or is in the process of restarting the stopped service(s) on the selected computer. Depending on the options you configure in the __Monitoring Template__ which is assigned to a computer, SysKit can send you __e-mail notifications__ when one or more important services are __stopped__ and can perform __automatic service restarts__. It will also tell you whether it has been successful or not.

See the [Monitoring Templates](#internal/) article to learn more about managing custom performance counters and important services.

## CPU, Memory, Disk and Network

The __CPU__ report in the Computer Performance category displays detailed CPU utilization statistics for the selected Date Range and Computer(s).

The __Memory__ report in the Computer Performance category displays detailed Memory usage statistics for the selected Date Range and Computer(s).

The __Disk__ report in the Computer Performance category displays detailed Disk performance statistics for the selected Date Range, Computer(s), Disk(s), and Disk Counter(s). With these two additional filters, __Disks__ and __Disk Counters__, you can select the desired __Logical Disk__ and __Disk Counter__ for the computer(s) specified in the Computers filter.

#### Disk Counters explanation

+ Used Disk Space – This counter displays the amount of available space and the total usable space on the logical volume in GB.
+ Avg. Disk Queue Length – Average number of both read and write requests that were queued for the disk, value should be between 0 and 2 most of the time, but if you have SAN or RAID controller this can spike above 2.
+ Disk Transfers/sec – Number of read and write IOPS (Input/output Operations per Second), mechanical disk IOPS are from 100-400, SSD from few thousands up to 100 000, modern SAN from few thousands up to million IOPS.
+ Disk Read KB/s – Current disk read bytes per second (throughput), maximum mechanical disk rate is 50-200 MB/s, SSD up to 550 MB/s, modern SAN more than 1000 MB/s, this transfer speed also depends on the RAID level, caching mechanism etc.
+ Disk Write KB/s – Average disk write bytes per second (throughput), maximum mechanical disk rate is 40-180 MB/s, SSD up to 500 MB/s, modern SAN more than 1000 MB/s, this transfer speed also depends on the RAID level, caching mechanism etc.

The __Network__ report in the Computer Performance category displays detailed Network performance statistics for the selected Date Range, Computer(s), Network Adapter(s), and Network Counter(s). With these  two additional filters, __Network Adapters__ and __Network Counters__, you can select the desired __Network Adapter__ and __Network Counter__ for the computer(s) specified in the Computers filter.

#### Network Counters explanation

+ Received Mbps – This counter shows the rate at which bytes are received per second over each network adapter.
+ Sent Mbps – This counter shows the rate at which bytes are sent per second over each network adapter.

__These reports include a few tricks:__

+ You can __quickly zoom in and out__ of a chart’s diagram using the mouse wheel.
+ When you click on the __Drill To Applications__ button, the resulting drilldown will capture the Filter values and take you to a more detailed Application Performance – History report.

A small but very important item to note here is the __tooltip__. The tooltip displays details about the data point the mouse is currently hovering over, such as the computer name, date and time values, and value of the data point.  
Use the __Date Range filter__ to set date boundaries on your performance data. You can select any day, week, or month or a custom date range.

> __Please note!__ You will not be able see any performance data outside 30 days unless you change the Performance Counters [Data Retention](#internal/) settings. The default is set to delete performance counters data older than 30 days.

#### Reports Ribbon

Depending on whether the report type is real-time or history, you will have a different set of options and filters available. Use the reports ribbon to take the following actions:

+ __Export__ – Save the current report to PDF, Excel, HTML, or CSV files.
+ __Subscription Manager__ – Create, edit, and send subscriptions that contain reports and views. Subscriptions can be delivered to email, SharePoint, and FileShare. 
+ __Schedule This Report__ – Schedule the current report or view to email, SharePoint, or FileShare.
+ __Save As View__ – Each report can have different Filters applied – Computers, Disks, Disk Counters, Network Adapters, or Network Counters. To create a View, click on the Save As View button on the ribbon, enter the view name, choose the view type and visibility, and click on Save. Afterwards, you can __adjust the filters__ on the newly created view, and save the changes by clicking the __Save View Changes__ button on the ribbon.
+ __Drill To Applications__ – Easily drill down from the reports to Application Performance – History by clicking the Drill To Applications button on the ribbon.
+ __Refresh__ – Refresh items in the left navigation panel, filters, and the main view.
+ __Options__ – Allows configuration of options for Report and Dashboard data, Alerts, Export and System Jobs.
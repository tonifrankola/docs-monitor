---
title: Quick Start Guide
description: This article provides a quick overview of things that can be done through the SysKit Monitor UI.
author: Andrea Budisa
date: 25/5/2017
---
This guide is intended as a basic guide to help you get started using SysKit Monitor and it simplifies performing common tasks by guiding you through a series of steps describing the user interface.

## Step 1: Add Computers

When you install and open SysKit Monitor for the first time, there will be no data on the reports. The first thing you should do is add servers for monitoring. If you are on the Session Dashboard, a warning message will be displayed that says you do not have any active computers; just click on the __link to add computer(s)__.

Computers can also be added from the __Administration – Computers__ category by selecting the __Add__ button from the upper ribbon.

See [Administration](#internal/get-to-know-syskit-monitor/administration/servers-and-groups) article to learn more about managing computers.

If you want to monitor only a single server only that is a part of a workgroup or Windows domain but __not AD-integrated__, please navigate to the Administration tab and click the arrow below the Add button in the upper ribbon, and then click __Add Computer Manually__.

## Step 2: Active Directory Integration

If you will be monitoring more than one computer, we recommend that you do not skip this step. To successfully perform AD Integration for multiple computers, follow the steps below:

1. Access __Manage__ in the __File__ menu and select __System Jobs__.
2. From the System Jobs dialog, select the __AD integration__ job and in the toolbar click __Run Now__ to execute that job.

## Step 3: Email Settings Configuration

To enable delivery of various SysKit reports by e-mail you must configure the SMTP server. If you will not use report scheduling and email notifications, you can skip this step.  
To perform basic email configuration follow these steps:

1. Access __Manage__ in the __File__ menu and click on __System Jobs__.
2. From the System Jobs menu, double click on __Send e-mails__ option. A new configuration window should appear.
3. From the __Outgoing email settings__ section select option __Enable e-mail sending__ and enter your SMTP server settings.
4. Input information related to server and email accounts. Once you have entered the required fields, test your settings by clicking on __Test email settings__ button.
5. Use __Period__ section to define the day and time when the service will start and to schedule the next incoming emails.

## Step 4: Manage Subscriptions

There are two simple ways to add and remove the report subscriptions. One uses the __Manage Subscriptions__ dialog while the other requires configuration of each report separately. Note that this step requires email sending to be enabled and properly configured.

To manage report subscriptions via the Manage Subscriptions dialog, follow these steps:

1. Access __Manage__ in the __File__ menu and select __Manage Subscriptions__. If you haven’t previously configured email settings, you can do so now by choosing the __Configure Email__ option. To do so, follow Step 3.
2. To add a new report subscription, select the __New Subscription__ option in toolbar. A new configuration window should appear.
3. Define preferences in the __Schedule__ tab that will be used for generating reports. Use a semi-colon to separate multiple receivers of the e-mails. Subject and description can be defined freely by the user. The description field will be presented to the e-mail receiver as the body of the e-mail.
4. In the __Reports__ tab select the reports you wish to add to the subscription by clicking on the __Add Report__ button.
5. Select your preferred report and define filters for it in the __New Scheduled Report__ dialog.

Another way to define your subscription is to access it through the main report dashboard. Navigate to the report you wish to send by email and choose __Schedule This Report > Schedule__ or __Add To Existing__ from the top menu. The rest of the procedure is the same as the steps above.

## Step 5: Get to know your dashboard

The [Sessions Dashboard](#internal/get-to-know-syskit-monitor/dashboards/sessions-dashboard) is shown at the start of the SysKit Monitor application. It enables you to see live data, such as the number of sessions in progress, and the number of currently running sessions, processes, and computer states.

You can also [create your own dashboards](#internal/how-to/dashboards/create-custom-dashboard) by accessing __My Dashboards__ in the Dashboard panel and selecting __New__ from the ribbon.

## Step 6: Date Range filter

For most of the available reports (all except Inventory Reports and some Performance Reports which are real-time), you can use the Date Range filter positioned on the right of the selected report, in the __Actions__ Panel. The selected Date Range represents the time filter for displayed data.

The Date Range filter enables you to select predefined time periods or define your own preferred time period for the selected report.
The selected time period will be preserved through all reports until you change it manually.

## Step 7: Filters

Filters are positioned on the right of the selected report. Depending on the selected report and available data, more or fewer filters will be presented to further eliminate excess data you do not want to be represented in your report.  
Like the Date Range filter, defined filters will be preserved through all reports.

If you find yourself in need of information provided in this Quick Start Guide, you can always access it manually through the SysKit Monitor if you navigate to __File > Help > Quick Start Guide__.
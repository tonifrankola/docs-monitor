---
title: Create SQL Custom Report
description: This article explains how to create a Custom SQL Report.
author: Andrea Budisa
date: 29/6/2017
---
This article explains how to create a **Custom SQL Report**.

Start a new instance of a **Custom Report Wizard** by going to Custom Reports in the left navigation bar and then clicking **Create** button from the ribbon.

### Step 1: Report Name & Type

Enter the report name and select a preferred category for your report. To create SQL report select **SQL** in **Report Type**. Once you do so, you will see a modified version of the Custom Report Wizard. Click **Next >** to proceed.

### Step 2: Enter your SQL

Enter preferred SQL **SELECT** statement. SQL statement you enter will serve as base for your report and will give you the same result as SQL Server Management Studio would.

You can write a simple plain SQL statement using common keywords, with or without parameters. Parameters are words prefixed with special character ‘@‘ (ex. @param1, @param2) and will be used as filters which you can modify outside of the SQL editor in the same way as filters used in standard reports. If you use clean SQL statement, your SQL report will not have any applicable filters.

>_**Please note!**_ *If you are not familiar with SQL or with SysKit Monitor database schema, please contact us and we will create an SQL report for your needs.*

### Step 3: Configure your Parameters

If you used parameters in the previous step, you will be able to initialize them in this step. If you used clean SQL statement you can skip this step.

There are two main options to initialize parameter: as a **Specific Value** or **Select from filter**.

**Specific Value parameter**

If you decide to define specific value, you need to do following:
* Select a preferred parameter from the list of **Detected Parameters**.

* In **Details** group select **Specific Value**.

* Enter **Display Name** if you wish to change the default name.

* In **Data Type** select the type of data for the parameter: **Integer**, **Decimal**, **String** or **Datetime**. 

* Edit **Default Value** to fit your filter criteria.

**Select from filter parameter**

On the other hand, if you choose to select your parameter from a filter, you can do so following these steps:

* Select a preferred parameter from the list of **Detected Parameters**.

* In **Details** group select **Specific from filter**.

* Select a preferred **Filter**.

* Edit **Values** for the selected filter to fit your selection criteria.

There is one more specific option related to parameters, you can use predefined parameters **@StartedOn** and **@EndedOn** to populate a **Date Range** filter. They are used in the same way as custom defined parameters. Only difference is that in third step you can choose to populate them from the Date Range filter. If you do not wish to do so, you can use them as your own custom parameters.

Perform steps described above for each detected parameter and proceed to the next step. Close the Custom Report Wizard by clicking the **Finish** button.

### Get to know your Custom Report

Once your Custom SQL Report has been generated you can edit it using **Edit** button in the ribbon or, if you used parameters, by changing filter values. Alterations in a report layout or filter values can be saved by using **Save Layout Changes** and **Save Filters** option in the ribbon.

If you edit the report layout or filters without saving changes, the next time you access the report it will have initial layout and filter values as if the change didn’t happen.

### Example: SQL statement that filters selected group of servers if servers are logged and updated after a specific date

As explained in the text above, you can write the SQL statement with or without parameters. We will describe both ways in detail.

In this example we will choose servers with ID = 1, 2, 3 as the target group of servers with LastUpdated date greater or equal to February 1st 2013. You can modify this part of SQL to fit your servers and your data.

Create a new custom report, fill in data and proceed to **Step 2: Enter your SQL**.

#### a) Clean SQL statement:

**SELECT** [TerminalServers].* **FROM** [TerminalServers] **where** [TerminalServers].TerminalServerID in (1, 2, 3) and LoggingEnabled = 1 and LastUpdated>= ‘2015-04-04’.

Skip the next step and click **Finish** to exit the Custom Report Wizard.

Newly created report doesn’t contain filters and if you choose to change target group of servers you will have to do so in the SQL Editor of the selected report.

#### b) SQL statement with parameters

**SELECT** [TerminalServers].* **FROM** [TerminalServers] **where** TerminalServerID in @TerminalServerIDs and LoggingEnabled = @LoggingEnabled and LastUpdated >= @LastUpdatedGE.

Click **Next >** to proceed. 

Set values to Detected Parameters. In the previous step we defined three parameters. In this step we will define their meaning and value.

For parameters **@LastUpdatedGE** and **@LoggingEnabled** set specific value as defined:
* **@LastUpdatedGE** set data type to DateTime and set default value to April 1st 2015
* **@LoggingEnabled** set data type to String and set default value to True

Parameter **@TerminalServerIDs** is somewhat different as it should represent collection of target server IDs. As such it will be populated from the filter.
* Select **@TerminalServerIDs** from **Detected Parameters**
* Choose the option **Select from filter**
* Since we want filter by specific servers, select **Servers** from **Filter**
* Select names of target servers in **Values**
* Proceed to the next step. Close the Custom Report Wizard by clicking the **Finish** button. 
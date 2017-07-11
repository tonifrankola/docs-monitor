---
title: Compare Wizard
description: Use Inventory Compare Wizard to compare inventory snapshots taken at different times and keep track of inventory changes.
author: Andrea Budisa
date: 25/5/2017
---
With the Inventory Snapshots __Compare Wizard__, you can compare __snapshots__ taken at different times, easily allowing you to detect and keep track of inventory changes.  
The purpose of the Inventory Snapshots is to display the snapshots for all scans performed over a period of time on your Windows Servers and workstations and to allow the __snapshot comparison__.

Read the section below to learn how to __manage snapshots__ created for your server farm(s).

### Manage Snapshots

You can access the Manage Snapshots dialog by navigating to the __Inventory Reports__, selecting __Snapshots__ from the ribbon, then choosing __Manage Snapshots__.

This form shows all available snapshots or if you haven’t yet deleted a snapshot – __all snapshots ever created__. You can set the __Mark as Good__ option for some of your snapshots so that later you can differentiate good configurations from others.

The following options are available:

+ __Load__ – Load the selected snapshot into the Inventory reports.
+ __Refresh__ – Use this option to refresh items displayed in the dialog.
+ __Delete__ – Use this option to delete the selected snapshot(s).
+ __Compare With Previous__ – Use this option to start the Compare Wizard and compare the selected snapshot with the one taken before it.
+ __Compare Selected__ – Use this option to start the Compare Wizard and compare the two selected snapshots.
+ __Mark As Good__ – Use this option to configure the selected snapshot(s) as good, for future use.

The grid-view in Manage Snapshots displays the following elements:

+ __Created On__ – The date and time at which a snapshot was taken.
+ __Mode__ – The snapshot can be created in two different modes; Automatic, which is performed by the SysKit Service according to the Period options set for this system job, while Manual is performed when this action is triggered by the user.
+ __Differences Detected__ – This option indicates whether differences were detected in the current snapshot when compared to the one taken before it.
+ __Good Configuration__ – Indicates whether the selected snapshot is well configured or not.

See the [Alerts](#internal/get-to-know-syskit-monitor/backstage-screen/configuration/options/#alerts) section if you want to receive e-mail notifications when inventory changes are detected.

### Compare Wizard

The __Compare Wizard__ offers two different compare types: __Inventory Snapshots__ and __Computers__.

The __first__ option enables you to select two inventory snapshots and explore differences between hardware and software data.

> __Tip!__ This option can be useful when you want to compare differences over time.

The __second__ option enables you to compare inventory data on different computers or two selected system environments that are defined through report views. You can define mappings between computers from different environments and determine which inventory items are different.

> __Tip!__ This option can be useful when you want to determine whether different computers have the same configurations or when you want to check if test and production environment are configured correctly.

#### Inventory Snapshots

1. In Step 1, simply select the compare type, which in this case is the __Inventory Snapshots__, as you want to compare two different inventory snapshots and detect any inventory changes.

2. In Step 2, you will need to select __two different snapshots__ you wish to compare. Depending on the __Compare options__ selected on the Inventory Snapshots system job, the Compare Result dialog will display differences in compared data.

3. The Step 3, __automatically starts the Compare Result__ dialog which will display all inventory changes between the two selected snapshots.

The __Compare Results__ dialog contains the following elements:

+ Details about two compared snapshots – the date and time at which snapshots were created.
+ Reports which the comparison is performed for.
+ Detailed grid view with equal, different and missing entries.
+ Show/Hide equal, different or missing nodes and entries – use these buttons to filter data and to make data analysis easier.
+ Save differences between the two selected snapshots to a PDF. With the Export to XLSX option, you can easily export the differences or all data to excel.
+ Compare Options – use these options to configure which reports you want compared. Unchecked options will not be displayed in the Compare Result dialog.

There are __two different levels__ on which data can be compared. Differences can be detected as follows:

__Report (node) level__

+ Different – this is on the report level (nodes).
+ Difference in children – indicates differences in any of the child nodes.

__Report data (entry) level__

+ Missing in source/target – indicates missing entries in source or target snapshot.
+ Different row/cell – indicates differences in any of the rows and cells.

#### Computers

1. In Step 1, simply select the compare type, which in this case is the __Computers__ option, as you want to compare the differences between two computers and detect inventory changes.

2. In Step 2, you will need to choose what kind of computer compare you wish to use. There are two subtype options at your disposal:

   + Compare two computers
   + Compare computers within selected views

   We will proceed with the first option – __Compare two computers__.

3. The Step 3, enables you to select __one or two different snapshots__ to compare inventory data on different computers. Depending on the Compare options selected in the __Inventory Snapshots__ system job, the Compare Result dialog will display differences in compared data.

4. The Step 4, __automatically starts the Compare Result__ dialog which will display all inventory changes, and depending on what is selected at the Snapshot Selection step, it will show one or two different snapshots.

   The __Compare Results__ dialog will contain all the elements previously described in the Inventory Snapshots section, as well as two new panels:

   + __Source Computer__ – Use the left panel to select the Source computer from the snapshot and compare it to the Target computer selected on the same or a different snapshot.
   + __Target Computer__ – Use the right panel to select the Target computer from the snapshot and compare it to the Source computer selected on the same or a different snapshot.

Now we will go back to the __Computer Compare Subtype__ step and proceed with the second option – __Compare computers within selected views__.  
In this step you need to choose the __Source__ and __Target Views__ to compare differences between these two selected system environments.

{:start="3"}
3. The Step 3, enables you to select __one or two different snapshots__ to compare inventory data on different system environments.

4. In Step 4, you will need to __define mappings__ for different computers within the __views__.  
For example, if you know that server A, from farm A and server B from farm B must be similar, you can map the FQDN names so every difference related to the name of the server won’t be displayed on the report.

   > __Please note!__ The current version of SysKit supports only __one-to-one__ server mapping!

5. The Step 5, __automatically starts the Compare Result__ dialog which will display all inventory changes according to previously defined mappings, and depending on what is selected at the Snapshot Selection step, it will show one or two different snapshots.
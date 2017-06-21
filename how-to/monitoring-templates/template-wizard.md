---
title: Template Wizard
description: This article outlines all the steps for loading custom performance counters and the successful performance monitoring of your Windows environments.
author: Andrea Budisa
date: 21/6/2017
---
We’ll break down how you can load custom performance counters into SysKit Monitor using Template Wizard.

1. In the __General__ step, simply enter the Monitoring Template name and description. You can also choose whether you want to include Performance Counters or Windows Services, or both, in this Template.
2. In the __Add Counters__ step, you will need to select the computer from which you wish to load representative Performance Counters. When a representative list of performance counters is loaded from a computer, you must select the performance counters and instances for which you want to collect data. Move the desired performance counters from Available to Selected Performance Counters.
   > __Please note!__ The representative performance counters that are loaded from a computer may vary based on the features of the selected computer that are enabled on that system.

3. In the __Configure Counters__ step, you will need to configure the Threshold, Notification, and Counter settings for the selected performance counter(s) in the previous step.
   + Under __Threshold Settings__, you can define the __warning__ and __critical__ thresholds and the threshold __state change interval__.
   + Under __Notification Settings__, you can select the checkbox in order to __receive an email notification__ when the computer crosses a warning and/or critical threshold. You can also define the length of time before the __alert notification is to be repeated__ for that counter.
   + Under __Counter Settings__, you can define the __Collecting Tolerance__, which means that not every collected value will be saved into the product database. Only new counter values that cross the specified tolerance, when compared to the last saved values, will be registered and saved.

4. In the __Add Services__ step, you can select the services you wish to add to the template. SysKit Monitor collects all the Windows Services that are running on your monitored computers in real time, so you can always choose the important services—from the __list of all available services__—according to your preferences.  
In this step you can also __add__ Windows Services that are __not currently listed__, by typing the __Service Name__ of the designated Windows Service into the __lower textbox__. __Asterisk * wildcard__ is used to represent a number of characters or an empty string, __e.g. MSSQL*__.  
After you __select and move__ the desired services from Available Services to Selected Services, you can proceed with the next step.

5. In the __Configure Services__ step, you can define actions for the selected services in the previous step. Here you can configure the following options:
   + select the checkbox so that SysKit Monitor will try to __restart__ a critical service after it has __stopped__;
   + select the checkbox to __receive an email notification__ when a selected service is stopped;
   + define the length of time before the __alert notification is to be repeated__ for that service.

In the last step, after your Monitoring Template has been configured successfully, please click the __Finish__ button. You can then use the created template and assign it to the appropriate __computers or computer groups__.
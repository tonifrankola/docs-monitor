---
title: Hardware and Software
description: These reports provide an overview of all hard drives, network adapters, processors, programs and printers used in your environment.
author: Andrea Budisa
date: 25/5/2017
---
Inventory Reports within SysKit Monitor are designed to make it as easy as possible for you to get an overview of everything that is deployed across your server environment and compare differences over time. SysKit periodically collects information in the form of __snapshots__ on all the hardware and software installed on your Windows Servers and workstations, as well as which users are the Local Administrators on monitored computers.

__Inventory Snapshot__ consists of:

+ Hardware (Hard Drives, Network Adapters, Processors, Printers)
+ Software (Programs, Available and Installed Windows Security Updates, Services, Certificates)
+ Local Admins report.

With the Inventory Snapshots __Compare Wizard__, you can compare snapshots taken at different times, easily allowing you to detect and keep track of inventory changes.

The purpose of the Inventory Snapshots is to display the snapshots for all scans performed over a period of time on your Windows Servers and workstations and to allow the __snapshot comparison__. The Compare Wizard allows you to compare the collected inventory data, which includes CPU, RAM, available hard disk space, installed programs and Windows updates, local administrators on the servers, etc.

> __Please note!__ In order to see the Inventory Reports it is necessary to configure [Inventory Snapshots](#internal/get-to-know-syskit-monitor/backstage-screen/configuration/options/#inventory-snapshots) system job. The report data will be available after Inventory Snapshots system job execution.
 
## Hardware

The reports within the __Hardware__ subcategory include:

    Hard Drives – Shows disk space usage for every computer in your farm – identify computers low on space.
    Network Adapters – View all network adapters on your system – easily understand where each computer is connected, and get a central overview of all network interface controllers (NICs) installed on your computers.
    Processors – View detailed configuration of each computer – CPU, model, number of processors, and the amount of memory installed.
    Printers – View all printers in your server environment.

## Software

The reports within the __Software__ subcategory include:

    Programs – View a full list of installed programs along with information about install date and location, help location, version and publisher.
    Available Updates – This report helps system administrators who want to see a full list of available updates along with information on whether an update has been downloaded or a reboot is required.
    Installed Updates – This report helps system administrators who want to see a full list of installed programs along with information about the installation date and location, help location, version, and publisher.
    Services – View all services that are running on your local and remote computers.
    Certificates – View a list of the certificates in the personal store on each computer along with information about the validity period, friendly name, thumbprint, intended purposes, etc.

## Local Users and Groups

The __Local Users and Groups__ subcategory contains only one report at the moment:

    Local Users and Groups – This report helps system administrators who want to see a list of all the members of the Local Administrators group for each computer.

The Inventory Reports include two filters: __Snapshots__ and __Computers__. Use the Snapshots filter to select a snapshot from a point in time and for the computer(s) specified in the __Computers__ filter. The Snapshots filter will have the __latest snapshot__ selected and it will be displayed in the reports.

Use the __Reports__ part of the Inventory reports ribbon for the standard actions available for all reports, such as __exporting__ to various formats, __scheduling__ to email, __saving__ as a view, __adding__ to the dashboard, etc.
 
#### Inventory reports Ribbon

Use the __Snapshots__ part of the Inventory reports ribbon to take the following actions:

+ __Take Snapshot__ – Trigger the collection job for Inventory Snapshots.
+ __Compare Wizard__ – Compare whole snapshots or specific computers and explore the differences in hardware and software data.
+ __Manage Snapshots__ – View and manage all your snapshots from one dialog. This includes loading, deleting, comparing, and marking the selected configuration(s) as good.
+ __Configure Snapshots__ – Configure the collection of Inventory Snapshots. Choose when the snapshots will be created, and which data will be collected and compared.

See the article on the [Compare Wizard](#internal/get-to-know-syskit-monitor/reports/inventory-reports/compare-wizard) to learn how to keep track of inventory changes and compare differences over time.
---
title: How to resolve the Offline and Unauthorized computer states
author: Andrea Budisa
description: This article explains how to resolve the offline and unauthorized computer states shown in SysKit Monitor. 
date: 29/06/17
---
### How to resolve the Unauthorized state?

If the computer is in __Unauthorized__ state on the [Administration – Computer](#internal/get-to-know-syskit-monitor/administration/servers-and-groups) category, that means the __Service User__ is not a member of the __Local Administrators Security Group__ on the remote computer where you see the message.

In order to get the data remotely, the service user needs to be a __member of the Local Administrators Security Group__ on the remote computer.

You can add the service user to the local Administrators Security Group [manually](#internal/how-to/service-accounts/add-service-user-manually) or through the [Group Policy](#internal/how-to/service-accounts/add-service-user-group-policy).

### How to resolve the Offline state for workstations?

Our software requires to __Allow Remote RPC traffic__ in order to get the data from the client workstations. After you enable this you will be able to connect and capture data from the __workstations__.

> __Please note__! This is required only in case you need to monitor __workstations__.
 
The easiest way to perform this is via the group policy. We will create either new policy or update existing and the change will propagate to clients. In this example we will create a new policy called __AllowRemoteRPC__.

1. We will assume all the workstations are within the same organization unit, so let’s right click on the desired OU and then select __Create a GPO in this domain, and Link it here…__
2. Name the policy somehow descriptive, e.g. AllowRemoteRPC-forWorkstations.
3. Right click on the newly created policy and click __Edit__.
4. Group policy management editor will open – navigate to Computer Configuration > Preferences > Windows Settings > Registry.
5. Now right click on the Registry > New > Registry Item.
6. In the key path navigate to __SYSTEM\CurrentControlSet\Control\Terminal Server__ and set __Value data__ to __1__ and the __Base__ to __Decimal__.
7. Confirm everything and that’s it, now SysKit Monitor is able to get the data from workstations as well.

What you need to do now is to go back to the SysKit Monitor and add extra workstations you want to monitor.

See [Network Ports](#internal/troubleshooting/network-ports) article to learn more on how to configure firewall settings for data collection.

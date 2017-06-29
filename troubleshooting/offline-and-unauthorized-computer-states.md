---
Title: How to resolve the Offline and Unauthorized computer states
Author: Andrea Budisa
Description: 
Date: 29/06/17
---
### How to resolve the Unauthorized state?

If the computer is in __Unauthorized__ state on the [Administration – Computer](#internal/troubleshooting/offline-and-unauthorized-computer-states/computer-and-computer-groups) category, that means the __Service User__ is not a member of the __Local Administrators Security Group__ on the remote computer where you see the message.

In order to get the data remotely, the service user needs to be a __member of the Local Administrators Security Group__ on the remote computer.

You can add the service user to the local Administrators Security Group [manually](#internal/troubleshooting/offline-and-unauthorized-computer-states/add-service-user-to-local-administrators-group-manually) or through the [Group Policy](#internal/truobleshooting/offline-and-unauthorized-computer-states/add-service-user-to-local-administrators-group-via-group-policy).

### How to resolve the Offline state for workstations?

Our software requires to __Allow Remote RPC traffic__ in order to get the data from the client workstations. After you enable this you will be able to connect and capture data from the __workstations__.

> __Please note__! This is required only in case you need to monitor __workstations__.
 
The easiest way to perform this is via the group policy. We will create either new policy or update existing and the change will propagate to clients. In this example we will create a new policy called __AllowRemoteRPC__.

1. We will assume all the workstations are within the same organization unit, so let’s right click on the desired OU and then select __Create a GPO in this domain, and Link it here…__
1. Name the policy somehow descriptive like AllowRemoteRPC-forWorkstations.
1. Right click on the newly created policy and click __Edit__.
1. Group policy management editor will open – navigate to Computer Configuration > Preferences > Windows Settings > Registry.
1. Now right click on the Registry > New > Registry Item.
1. In the key path navigate to __SYSTEM\CurrentControlSet\Control\Terminal Server__ and set __Value data to decimal 1__.
1. Confirm everything and that’s it, now SysKit is able to get the data from workstations as well.

What you need to do now is to go back to the SysKit Monitor application and add extra workstations you want to monitor.

See [Network Ports](#internal/troubleshooting/offline-and-unauthorized-computer-states/network-ports) article to learn more on how to configure firewall settings for data collection.

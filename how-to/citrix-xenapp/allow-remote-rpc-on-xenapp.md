---
Title: Allow Remote RPC on XenDesktop machines.
Author: Andrea Budisa
Description: 
Date: 29/06/17
---
In order to monitor __XenDesktop__ machines without any agents installed, our software requires to Allow Remote RPC traffic in order to get the data from the client machine. After you enable this you will be able to connect and capture data from the XenDesktop machines completely offloading processing to the SysKit box.

> Please note! This is required only in case you need to monitor XenDesktop machines.
 
The easiest way to perform this is via the group policy. We will create either new policy or update existing and the change will propagate to clients. In this example we will create a new policy called __AllowRemoteRPC__.

1. We will assume all the XenDesktop Machines are within the same organization unit, so let’s right click on the OU XenDesktop and then select “Create a GPO in this domain, and Link it here”.

1. Name the policy somehow descriptive like AllowRemoteRPC-forXenDesktop.

1. Right click on the newly created policy and click __Edit__.
1. Group policy management editor will open – navigate to Computer Configuration > Preferences > Windows Settings > Registry.
1. Now right click on the Registry > New > Registry Item.
1. In the key path navigate to __SYSTEM\CurrentControlSet\Control\Terminal Server__ and set __Value data to decimal 1__.
1. Confirm everything and that’s it, now SysKit Monitor is able to get the data from XenDesktop machines as well.

What you need to do now is to go back to the SysKit application and add extra machines you want to monitor.
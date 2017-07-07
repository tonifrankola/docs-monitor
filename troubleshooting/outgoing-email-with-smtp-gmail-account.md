---
Title: Configuring outgoing email with an smtp.gmail account
Author: Andrea Budisa
Description: This article explains how to configure outgoing email with an smtp.gmail account to use with SysKit Monitor.
Date: 29/06/17
---
Google blocks sign-in attempts from some apps or devices that do not follow modern security standards. Since these apps and devices are easier to break into, blocking them helps keep your account safe. Unfortunately, Google thinks SysKit Monitor is also unsafe.

Therefore, you have to enable __Less Secure Sign-In__ for your Google account in order to enable sending emails in this configuration.

To enable this feature, please follow these steps:

1. Sign in to your Google account (the Google account you use as your Username in the Email options form).
2. Go to: <https://www.google.com/settings/security/lesssecureapps>.
3. Turn on the __“Access for less secure apps”__ option.

After you enable this feature, you should be able to send e-mails without a problem.

Make sure that you have properly configured the __Outgoing email settings__ in the __Send e-mails__ system job within SysKit Monitor:

* The outgoing server should be __smtp.gmail.com__ with port __587__.
* __Use encrypted connection (SSL)__ option should be turned on.
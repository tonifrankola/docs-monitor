---
Title: Configuring outgoing email with an smtp.gmail account
Author: Andrea Budisa
Description:
Date: 29/06/17
---
Google blocks sign-in attempts from some apps or devices that do not follow modern security standards. Since these apps and devices are easier to break into, blocking them helps keep your account safe. Unfortunately, Google thinks SysKit Monitor is also unsafe.

Therefore, you have to enable __Less Secure Sign-In__ for your Google account in order to enable sending emails in this configuration.

To enable this feature, please follow these steps:

1. Sign in to your Google account (the Google account you use as your Username in the Email options form).
1. Go to [https://www.google.com/settings/security/lesssecureapps](https://myaccount.google.com/lesssecureapps?pli=1).
1. Turn On __“Access for less secure apps”__.

After you enable this feature, you should be able to send e-mails without a problem.

Make sure that you have properly configured the __Outgoing email settings__ in SysKit’s Monitor __Send e-mails__ system job:

* The outgoing server should be __smtp.gmail.com__ with port __587__
* __Use encrypted connection (SSL)__ option should be turned on
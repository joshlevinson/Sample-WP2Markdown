---
title: 'Getting Started with Magento'
subject: 'SuiteIntegrations, SuiteMagento'
old_url: 'http://emarsys.dev/old/suite/magento/getting-started/'
---

**Emarsys for Magento is compatible with the following Magento versions:

- Community version 1.7
- Community version 1.8
- Community version 1.9
- Magento Enterprise 1.12
- Magento Enterprise 1.13
- Magento Enterprise 1.14

### Prerequisites

 Before you can install Emarsys for Magento you need an Emarsys API account. Please contact Emarsys Support if you do not already have one. If you have ever used a previous Magento integration from Emarsys, please make sure that this has been uninstalled. You will also need to do the following:

- Create two custom fields in Suite called: - **Magento Customer ID**
- **Magento Subscriber ID**

Please note that these field names are case-sensitive (e.g. ***Magento customer id*** won’t work).

- Contact Emarsys Support to have these custom fields indexed internally in the account database.
- If you are using Smart Insight, ask Emarsys Support for the FTPS credentials. Also, make sure that your Magento hosting provider allows outgoing connections to the address ***exchange.si.emarsys.net*** over the ports ***TCP21*** and ***TCP32000-32500**.*
- Make sure that you can install extensions from the Magento Marketplace in your Magento shop.
- Make sure that the PHP SOAP extension is enabled on your Magento host. Your hosting provider can check this for you.
- Set your Magento Cron to run on 5-minutes basis. You can check the [Magento documentation](http://magento.com/help/documentation) for instructions on how to do this or ask your Magento provider to do it for you.

### Installation

 You can obtain the **Emarsys for Magento **installation package from Emarsys Support (it is also available from the Magento marketplace but that will simply direct you back to Emarsys). Once you own the package, you should install it in your Magento shop as following:

1.  Log in your Magento back-end (admin) and navigate to **System > Magento Connect > Magento Connect Manager**. Here you will be asked to enter your login credentials again.
2. Under **Direct package file upload**, browse to the latest Emarsys for Magento package (a *.tgz* file) provided by Emarsys Support and upload it:
 
[![magento_install_1](/assets/images/2015/07/magento_install_1-300x184.png)](/assets/images/2015/07/magento_install_1.png)1. After successfully uploading the file, return to the Magento admin module and navigate to **System / Cache Management** and flush the **Magento Cache** and the **Cache Storage**. After this you must log out and then log in again.
2. Now that Emarsys for Magento is installed, you will see a new section in the **System / Configuration** menu:
 
[![magento_install_2](/assets/images/2015/07/magento_install_21-273x300.png)](/assets/images/2015/07/magento_install_21.png)1. Click **Suite Settings** to configure your Suite API credentials (not your Emarsys account credentials!). Click **Test connection** to check that you have entered these correctly:
 
[![magento_install_3](/assets/images/2015/07/magento_install_3-300x132.png)](/assets/images/2015/07/magento_install_3.png)Your integration is now installed, and you can move on to the individual feature settings.

**
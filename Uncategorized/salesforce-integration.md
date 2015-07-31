---
title: 'Integrating Salesforce with Suite'
subject: ''
old_url: 'http://emarsys.dev/old/suite/connect-2/salesforce-integration/'
---

Setting up your Suite Salesforce integration is simple and requires no actions in Suite itself.

##### Contents

1. [Prerequisites](#pre)
2. [Installing the App in Salesforce](#setup-sf)
3. [Configuring the integration in Salesforce](#config-sf)
 
<a name="pre"></a>1. Prerequisites
----------------

 To install the Salesforce App you will need the following:

- Your Suite API user credentials; contact Emarsys Support if you are not already a Suite API user
- The URL of the Emarsys App in Salesforce, provided by Emarsys Support
- The Emarsys installation password, provided by Emarsys Support

 Additionally, you will need one of the following Salesforce products:

- Salesforce Enterprise Edition
- Salesforce Unlimited Edition
- Salesforce Developer Edition (for testing purposes only)
- Salesforce Professional Edition (will be supported in a future product version
 
<a name="setup-sf"></a>2. Installing the App in Salesforce
-----------------------------------

 To install the App in Salesforce, proceed as follows:

1. Enter the URL for the Emarsys Salesforce App
2. Log in to your Salesforce account if prompted
3. Enter the Emarsys installation password
4. Follow the installation instructions until you see **Choose security level**
5. Select which users should have access to the App
6. You can now proceed to the configuration steps described below
 
<table style="width: 100%"><tbody><tr><td style="text-align: left;width: 80px;border-color: #fff;background-color: #fff;color: #eb5a19">**Please Note:**</td> <td>The App contains a “Permission Set” which can be applied to individual users. Therefore it is not a problem if you are not sure to whom to give access during installation, as you can grant access later on as well.</td> </tr></tbody></table><a name="config-sf"></a>3. Configuring the Integration in Salesforce
--------------------------------------------

 Before you use the App for the first time, you will need to configure a few settings as follows: In Salesforce, open the **Setup **menu.

1. Go to **Customize/Campaign/Fields**
2. In the **Type** drop-down list, add *emarsys Email* as an option
3. Go to **Customize/Contacts/Page Layouts**
4. Add the related list *EMS Email Responses *to your layout.
5. Click **Edi****t** and add the following fields:

- EMS Email
- Email Category
- Response Type
- Response Date/Time
- Link Category
- Link Title
- Link URL


1. Go to **Customize/Leads/Page Layouts**
2. Add the related list *EMS Email Responses *to your layout
3. Click **Edi****t** and add the following fields:

- EMS Email
- Email Category
- Response Type
- Response Date/Time
- Link Category
- Link Title
- Link URL


 You are now ready to take advantage of all that eMarketing Suite and Salesforce have to offer. See also:

[Salesforce Integration: Use cases and examples](http://emarsys.dev/old/suite/connect/salesforce-use-cases/ "Salesforce Integration: Use cases and examples")
---
title: 'Magento and Smart Insight'
tags: 'SuiteIntegrations, SuiteMagento'
old_url: 'http://emarsys.dev/suite/magento/smart-insight/'
---

If you are using the Smart Insight customer intelligence module, you can easily integrate your Magento shop with it. This part ofÂ  **Emarsys for Magento** can be enabled in the **Smart Insight settings** section (**System** / **Configuration** / **Emarsys Connect** / **Smart Insight**). [![magento_si_1](/assets/images/magento_si_1-300x182.png)](/assets/images/magento_si_1.png) If you choose to enable this feature, you can:

- Make a one-off export from Magento to Smart Insight of all your e-commerce data for the last two years.
- Define the daily schedule to update your Magento e-commerce data in Smart Insight.
- Incluce Magento Bundles in the e-commerce export.

### Setting up a FTPS Connection

 E-commerce data is exported to Smart Insight via an Emarsys FTPS service. Emarsys Support will provide the credentials you need to enter in the Magento form: [![magento_si_2](/assets/images/magento_si_2-300x141.png)](/assets/images/magento_si_2.png) The **Test connection** button can be used to check the FTPS settings credentials. The button should turn green when successful: [![magento_si_3](/assets/images/magento_si_3.png),](/assets/images/magento_si_3.png) or red with a message if it fails:Â  [![magento_si_4](/assets/images/magento_si_4.png)](/assets/images/magento_si_4.png).

### Exporting the Last Two Years of E-commerce Data

 The first thing you should do after enabling the Smart Insight integration is export all your e-commerce data from the last two years. To do this, simply click **Generate Now** and an export will begin at the next multiple of five minutes. The e-commerce data included in the exports includes the standard order information, such as customer, items, quantity, prices, item categories, etc. Please note that orders are only included in the export if they are in the states **processing**, **complete** or **closed**.

### Scheduling the Daily E-commerce Export

 After your initial export, a daily export will then run at the time specified in the **Execute at** field.

### Magento Bundles

 You can also include your Magento Bundles in the export; simply set this field to *Yes*. IfÂ  you do not wish to include Bundles, your export file will contain only the product data: [![magento_si_5](/assets/images/magento_si_5-300x43.png)](/assets/images/magento_si_5.png) If you do include Bundles, then the Bundles will be included as an extra line in addition to the product data: [![magento_si_6](/assets/images/magento_si_6-300x50.png)](/assets/images/magento_si_6.png) You can also define whether to calculate the Bundle price or not. If this field is set to *No*, the price for each item in the Bundle is listed independently and the price for the Bundle is set to zero: [![magento_si_7](/assets/images/magento_si_7-300x47.png)](/assets/images/magento_si_7.png) If this field is set to *Yes*, the Bundle price will display the total for all items in the Bundle and the items themselves will have their price set to zero: [![magento_si_8](/assets/images/magento_si_8-300x47.png)](/assets/images/magento_si_8.png)
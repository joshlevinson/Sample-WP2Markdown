---
title: 'Ecommerce Tracking'
subject: Suite
old_url: 'http://emarsys.dev/old/suite/reporting/ecommerce-tracking/'
---

The Emarsys **Ecommerce Tracking** feature gives you the ability to track end-user activity in your web shop and then analyse the data using Emarsys eMarketing Suite. This allows you to monitor the success of your campaigns in terms of online orders, and end-user behavior with regards to actual and abandoned purchase trends.

How does it work?
-----------------

### Standard Ecommerce Tracking

 [Defcon3] In order to use standard ecommerce tracking you need to contact Emarsys Supportto enable it, and then follow the steps for integrating the tracking feature as described below. Emarsys Support will need a list of users you would like to be able to view the ecommerce reports. These users will be upgraded to the **Administrator ecommerce** user group, and will have full access to Suite features. Once access has been configured, you will be provided with a customer ID and designated an environment to use, for example **https://www1.emarsys.net/u**. You will then need to integrate code snippets into two key areas of your website (**Order Confirmation** page and **Thank You** page) which then enable campaign-level reporting. It works by using code in the email links in conjunction with the code snippets integrated in the website, which then capture information through either cookies or session data generated when the user visits your website from a link in an email. There are two methods to integrate the tracking features into Suite:

- [using JavaScript code](/Suite/ecommerce-tracking-using-javascript.md "Implementing Ecommerce Tracking using JavaScript")
- [using an image pixel](/Suite/ecommerce-tracking-using-an-imagepixel.md "Implementing Ecommerce Tracking using an ImagePixel")

 Both methods require you to integrate code into your website, but have slightly different usage scenarios as the JavaScript method needs the end users to have more relaxed security settings on their browser for it to work. Once ecommerce tracking has been enabled, a new entry is available in the **Analysis** menu called **Ecommerce Tracking**. This section lists successful order events and abandoned shopping cart events from the web shop, both of which can be broken down to show the items in them. These three categories of trackable events are categorized as follows:

- Orders successfully placed
- Number of Abandoned Shopping Carts
- Items successfully purchased

 Both the orders and abandoned cart sections contain the same information per recorded instance: order date, order ID, contacts email, campaign name, and value. Please note: As this data is held separately from the contacts database it can only be reported on, not interacted with or segmented further. For this you will need Advanced Ecommerce Tracking. As most of the configuration necessary for this to work is done on the website by you or your technical team, this facility is available free of charge. However, if you require support for your standard tracking implementation, this is available from Emarsys and will be billed at an hourly rate. For more information please contact Emarsys Support.

### Advanced Ecommerce Tracking

 [Defcon1] If you need your ecommerce analysis to be available for segmentation and further action, you will need to use the Suite API to synchronize the data with your Suite database. If you do not have the resources to integrate the API yourself, please speak to Emarsys Support about possible custom solutions.
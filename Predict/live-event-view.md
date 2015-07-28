---
title: 'Live Event View'
tags: Predict
old_url: 'http://emarsys.dev/predict/user-guide/live-event-view/'
---

Once you have implemented the Web Extend scripts that you want to use, you can easily check to see if the scripts are working correctly by opening the **Live Event View** page in the **Predict** menu in Suite. The **Live Event View** shows the last 10 events on your web shop that have been identified by the scripts. This is refreshed every time you open the page or click the **Refresh** button. To validate your data collection scripts, you just need to go to the web shop and perform the kind of actions that you want to capture from visitors. Then go back to Suite and check that these have been correctly picked up by Web Extend. If not, please contact Emarsys Support so that Emarsys can check your implementation for errors.

##### Example

 To validate the **View** event, click an item on the web shop and check that this item is shown under **view events** with the following information: - Time and date of view
- CustomerID
- Item thumbnail
 
<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">The code under the date and time refers to the Web Extend cookie and can be ignored. The **Cohort** is only interesting if you are using A/B testing.</td> </tr></tbody></table> The **CustomerID** will show ***$custom...*** if you browsed the web shop anonymously, or a real customer ID if you logged in. You should test both scenarios. Click the thumbnail to go to the **Product Information** page, where you can see the item ID, category, price and availability as defined in the Product Catalog. Clicking the item link should take you back to the page where you originally viewed it. You should then repeat this process for all the other events that you want to track: - Clicks
- Add-to-cart events
- Purchases
- Category views
- Searches
- Keywords
 
 Once you have validated all the events you are using, you must wait until Web Extend has collected enough data to enable Predict to make meaningful recommendations. Once your installation of Predict has been activated and is working in a live environment, you can continue to check it using the **Live Validator** page of the **Predict** menu in Suite. ### Validating a multi-domain integration

 If your web shop has multiple domains, you should see the localized feature names appear in Live Event View (**RELATED_UK**, **PERSONAL_UK**, etc.). You should also check that the **addToCart** and **checkOut** commands from your localized sites report the transaction value in the currency of your main site.
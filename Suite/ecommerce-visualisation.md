---
title: 'Ecommerce Tracking Visualization'
subject: Suite
old_url: 'http://emarsys.dev/old/suite/reporting/ecommerce-visualisation/'
---

#### Ecommerce Integration Visualization

 Below is an example of how ecommerce tracking might work for you.

1. The chosen tracking code is embedded in your online shop.
2. The contact clicks on the trackable link embedded in the email they receive.
3. Emarsys eMarketing Suite forwards the contact to your online shop and adds a parameter called the `emst` parameter to the target URL.
4. The web shop detects the `emst` parameter and stores the contact activity using a cookie or session, valid up to (for example) 30 days.
5. After a successful order is placed, the **Thank You** page is retrieved if a cookie or session with the `emst` parameter is detected.
6. If a contact accesses the **Order Confirmation** page but not the **Thank You** page then an `orderID` is not generated and the event is flagged as an abandoned shopping cart event.
 
[![visualisation of Standard eCommerce integration](/assets/images/2014/04/Ecommerce_tracking_04-1.png)](/assets/images/2014/04/Ecommerce_tracking_04-1.png) When the contact reaches the **Order Confirmation** page the data capture starts and they are flagged for an abandoned shopping cart email which is only cancelled if they successfully complete the purchase. If they do not complete the purchase within the time-out period (default is 30 minutes) then an abandoned shopping cart event is logged.
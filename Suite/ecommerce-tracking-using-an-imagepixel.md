---
title: 'Implementing Ecommerce Tracking using an ImagePixel'
tags: Suite
old_url: 'http://emarsys.dev/suite/reporting/ecommerce-tracking-using-an-imagepixel/'
---

Image pixel tracking works by using a small pixel buried in the page with associated code that enables the tracking. As opposed to the JavaScript method this only requires code to be embedded, and no additional script to be hosted on the website.

The tracking pixel URL parameter is then created by the web shop which uses the embedded <img> tag in the **Order Confirmation** and the **Thank You** pages.

 To integrate the image pixel method, proceed as described below. ### Order Confirmation Page

- Add the following code to your **Order Confirmation** page:
 

    <img src="http://www.emarsys.net/upages/ti.php?
      ems_customer=123456789&
      ems_visitor=<customer_number>&
      ems_session=<sessionid>&
      ems_campaign=<emst>&
      ems_action=purchase&
      total=<order_total>&
      tax=<tax_total>&
      shipping=<shipping_total>&
      city=<city>&
      country=<country>&
      code[]=productid_of_product1>&
      category[]=<category_of_product1>&
      productname[]=<name_of_product1>&
      price[]=<price_of_product1>&
      quantity[]=<quantity_of_product1>&
      code[]=<productid_of_productX>&
      category[]=<category_of_productX>&
      productname[]=<name_of_productX>&
      price[]=<price_of_productX>&
      quantity[]=<quantity_of_productX>"
    border="0" alt="" width="1" height="1" style="display:none;">


### Thank You Page

- Add the following code to your **Thank You** page:
 

    <img src="http://www.emarsys.net/upages/ti.php?
      ems_customer=123456789&
      ems_visitor=<customer_number>&
      ems_session=<sessionid>&
      ems_campaign=<emst>&
      ems_action=purchase&
      order=<orderid>&
      total=<order_total>&
      tax=<tax_total>&
      shipping=<shipping_total>&
      city=<city>&
      country=<country>&
      code[]=<productid_of_product1>&
      category[]=<category_of_product1>&
      productname[]=<name_of_product1>&
      price[]=<price_of_product1>&
      quantity[]=<quantity_of_product1>&
      code[]=<productid_of_productX>&
      category[]=<category_of_productX>&
      productname[]=<name_of_productX>&
      price[]=<price_of_productX>&
      quantity[]=<quantity_of_productX>"
    width="1" height="1" border="0" alt="" style="display:none;">


 <table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">You must replace ***www.emarsys.net*** with the appropriate Suite environment and 123456789 with your Emarsys account ID.</td> </tr></tbody></table> The image pixel code will now be able to gather data from contacts in the same way that the JavaScript code does, and will feed back to the Suite for reporting purposes. In the same way as when integrating the JavaScript code, the image pixel code can be amended to include or exclude data for the reporting section in Suite.
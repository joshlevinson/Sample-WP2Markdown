---
title: 'Implementing Ecommerce Tracking using JavaScript'
subject: Suite
old_url: 'http://emarsys.dev/suite/reporting/ecommerce-tracking-using-javascript/'
---

The JavaScript method uses three elements:

- an Emarsys script which is hosted on your website
- a JavaScript code snippet which is inserted into all your website pages
- special JavaScript code snippets which are inserted into your target pages

 Some end users may have JavaScript or cookies disabled due to security reasons, in which case JavaScript based tracking will not work. If you find this is a problem, you should use the image pixel implementation instead to enable ecommerce tracking.

<table border="0" cellpadding="1" class="wikitable" title="JavaScript Integration Overview"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">With the JavaScript method the functions need to run in the correct order for it to work, i.e. `emsTracking` has to run before `emsSubmitOrder`. If you download the script then these instances will already be set to run in the correct order.</td></tr></tbody></table>Implementing the Javascript
---------------------------

 To integrate the JavaScript method, proceed as follows:

- Download the script from `http://www.emarsys.net/u/emstrack.js`.
- Store it in a public folder on your web server, e.g. `http://www.yourdomainhere.com/js/emstrack.js`.
- Embed this script in the  section of every webpage:
 

    <script language="Javascript" type="text/javascript" src="http://www.yourdomainhere.com/js/emstrack.js"></script>

- Place this HTML snippet on every page:
 

    <script type="text/javascript" language="JavaScript">
    // <!--
      emsSetEnv('www1'); 
      emsTracking(112734771,'yourdomainhere.com');
    // --> 
    </script>

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">- This code snippet must be loaded and executed before any `emsSubmitOrder()` calls.
- Replace ***www1*** with your Suite environment variable (Emarsys Support can help you with this).
- Replace ***112734771*** with your Suite customer ID.
- Replace ***yourdomainhere.com*** with the address of your website.
 
</td></tr></tbody></table>### Order Confirmation Page

- Add the following code to the **Order Confirmation** page of your website:
 

    <form style="display:none;" name="emsform">
      <input type="hidden" name="total" value="totalprice_without_comma_only_with_dot">
      <input type="hidden" name="tax" value=" totaltax_without_comma_only_with_dot ">
      <input type="hidden" name="shipping" value="shippingcosts_without_comma_only_with_dot">
      <input type="hidden" name="city" value="city_of_the_client">
      <input type="hidden" name="country" value="country_of_the_client">
      <!-- Repeat the following line for each ordered product in the cart -->
      <input type="hidden" name="ems_items[]" value="id_of_ordered_product1;category_of_ordered_product1;name_of_ordered_product1;price_of_ordered_product1_without_comma_only_with_dots;quantity_of_ordered_product1_without_comma_only_with_dots">
    </form>
    <script type="text/javascript" language="JavaScript">
      // <!--
      emsSubmitOrder();
      // -->
    </script>

### Thank You Page

- Add the following code to your **Thank You** page:
 

    <form style="display:none;" name="emsform">  
      <input type="hidden" name="tax" value="[totaltax]">
      <input type="hidden" name="shipping" value="[shippingcosts]">
      <input type="hidden" name="city" value="[customer_city]">
      <input type="hidden" name="country" value="[customer_country]">
      <input type="hidden" name="order" value="[order]">
      <input type="hidden" name="total" value="[total]">
      <!-- Repeat the following line of each product in cart -->
      <input type="hidden" name="ems_items[]" value="[sku/code];[category];[product name];[price];[quantity]">
    </form>
    <script type="text/javascript" language="JavaScript">
    // <!--
      emsSubmitOrder();
    // --> 
    </script>


<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">The square brackets in the above code are to indicate where the content is entered and should not be included, nor should you use commas to separate large numbers. For example: value="[total]" should just be value="2999.00" and not value="[2,999.00]". The inserted JavaScript code will now interact with the downloaded script to populate the content from your web shop. When integrating the code, values can be removed if they are not required for the reporting. Optional entries are: [sku/code], [category], [product name], [price], [quantity].</td></tr></tbody></table>
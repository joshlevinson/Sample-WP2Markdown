---
title: 'Importing the Product Catalog'
subject: 'Gettingstarted, WebExtend'
old_url: 'http://emarsys.dev/old/web-extend/implementation/catalog-import/'
---

Once you have [prepared your product catalog](/Gettingstarted/prepare-catalog.md) and are sure that it is correctly formatted, you can import it on the **Product Catalog** page of the **Predict** menu in your Suite account. After that, to make sure that Suite is always kept up to date with changes to your products, a new (and complete) product catalogue should be exported every day.

### <span class="mw-headline" id="Manually_Importing_the_Product_Catalogue">Manually Importing the Product Catalog<a name="bs-ue-jumpmark-1efe589607ffa593a6bbc3876667af60"></a></span>

 In your Suite account, open the **Predict** menu, **Product Catalog** tab. [![Product_catalogue_settings](/assets/images/2014/04/Product_catalogue_settings-300x173.png)](/assets/images/2014/04/Product_catalogue_settings.png)

<div style="text-align: center;">**Figure:** The **Product Catalog** tab in Suite. Note that the Merchant ID is displayed below the menu on the left.</div> In the **Catalog Upload** field, browse for the catalog. Before you upload it you should validate it, which will tell you whether the syntax of your .CSV file is correct. In case of validation errors please check your syntax again and contact Emarsys Support if problems persist. Then click **Submit** to import the file.

### <span class="mw-headline" id="Scheduling_Automated_Product_Catalogue_Imports">Scheduling Automated Product Catalog Imports<a name="bs-ue-jumpmark-0a18db5162bb2906f7e500168fdc23e1"></a></span>

 After the catalog has been successfully imported, you should set up an automated export on your side to a designated destination, and then enter and save that URL in the **Catalog URL** field. Suite will fetch the catalog every day and log these imports in the **Catalog List** table below. Imports are scheduled for shortly after midnight UTC, but alternative schedules are possible on request.
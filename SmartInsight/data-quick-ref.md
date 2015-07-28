---
title: 'Data Exchange Quick Reference Guide'
tags: SmartInsight
old_url: 'http://emarsys.dev/resources/data-transfer/data-quick-ref/'
---

Importing Ecommerce Data
------------------------

 The guidelines below cover the import of ecommerce data from web shops and other databases for use in eMarketing Suite. The guidelines apply to all Suite features and related modules, unless explicitly stated otherwise.

### File Types

 Ecommerce data falls into two categories:

- **products **These are the products that you offer for sale on your web shop, and make up your product catalogue.
- **sales items **These are individual items in an order, comprising order information such as order ID, customer ID, etc., and the product ID of the item purchased.

### File Names

 All files containing ecommerce data must start with the correct prefix according to their type. These are:

- products
- sales_items

 You can then continue with the file name using the following characters:

- Letters of the English alphabet (a-z, A-Z)
- Numbers (0-9)
- The separator characters '_' (underscore) and '-' (dash)

 When naming your import files, it is good practice to include a date suffix, e.g. <tt>products-2013-05-07.csv</tt>. Due to the way the files are sorted in the import folder, this will ensure that the files are easy to find. Once a file has been successfully imported, the name is automatically modified and a timestamp added as a prefix. It will also be removed from the upload folder and placed in a folder called 'Finished'.

#### Examples

<table class="wikitable"><thead><tr><th style="text-align: left;">december-products-shoes.csv</th> <td>This file will *not* be imported</td> </tr><tr><th style="text-align: left;">products-01-12-13-shoes.csv</th> <td>This file *will* be imported</td> </tr><tr><th style="text-align: left;">2013-12-05_00h13m57s_products-01-12-13-shoes.csv</th> <td>This file *has been successfully* imported</td> </tr></thead></table><table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">Files that do not match these naming conventions are silently ignored. That is, you will not receive any notification that they have not been imported.</td></tr></tbody></table>### Smart Insight Uploads

 Every customer has a designated upload folder for Smart Insight uploads. This folder - in the form of an FTPS account - is made available to the customer as part of the Smart Insight integration process. Files uploaded to this directory are processed automatically by the system as long as they follow the correct naming convention described above.

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">Smart Insight *detects duplicates* in the **product** catalogue: newer values overwrite old values.</td> </tr></tbody></table><table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">Smart Insight *does not detect* duplicates in the **sales_item** catalogue: Duplicates will appear as two identical entries in the reports.</td></tr></tbody></table>The Data Files
--------------

### Generating a Product Catalogue for Import into Suite

 In order to ensure that Emarsys solutions have access to the most recent data, you should import your entire product catalogue every day. The product catalogue must be uploaded as a UTF-8 Unicode encoded, .CSV (comma separated values) file. The first line is the header. It is a simple comma-separated list describing what the columns are. Subsequent lines contain fields in the order defined in the header.

#### Required Fields

 Below is an example of the fields required for the product catalog. These fields must all be present and must be in the order described below.

- **item** (string) - the unique ID used in your system to identify an item. This is the ID that all data-collection and rendering scripts will refer to.
- **title** (string) - the name of the product.
- **category** (list of hierarchy levels) - describes the category that a given item belongs to.
 
<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">- Depending on the Emarsys solution you use, your product catalogue can have other mandatory or custom fields.
- The order of the first three fields is important for Emarsys Smart Insight implementations.
 
</td></tr></tbody></table>#### Categories and Hierarchies

- Emarsys solutions support multiple *categories*- Use the pipe character (|) to separate categories.

- Categories can consist of *hierarchy levels*: - Hierarchy levels are separated by the greater-than character (>)
- The most generic level is always the first one. For example, in a bookstore, a specific book would have the levels`"book > literature > fiction"`
- Using multiple categories, the example would look as follows:`"book > literature > fiction | book > literature > british"`

#### Categories in Smart Insight

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">By default, only the first three categories are displayed by Smart Insight</td> </tr></tbody></table><table cellpadding="1" class="wikitable" style="width: 100%; border: 0px solid #999;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">**Product category visualization in the Affinity and Purchases screen:**- Assuming a product has three categories, for a product purchase all three categories will show in the bar chart (three separate rows)
- Customers can select a hierarchy level to use as a label on the bar chart.
 
</td> </tr></tbody></table><table cellpadding="1" class="wikitable" style="width: 100%; border: 0px solid #999;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">**Filters:**- Smart insight will take the first three hierarchy levels from each category.
- These three levels will be grouped under three filters - The first filter will use the left value in the hierarchy (e.g. "type")
- The second filter will use the middle value in the hierarchy (e.g. "brand")
- The third filter will use the right value in the hierarchy (e.g. "gender")
 
</td></tr></tbody></table>#### Sample Data

 Below is an example of how a product catalogue file might look, including some custom fields for Emarsys Predict:


    item, title, category, link, image, available, price, c_predict_1, c_predict_2, c_predict_3
    
    122,"The Ancestor's Tale", book > popular > science > predict_attribute1 > predict_attribute_2 | office > print > read > predict_attribute1 > predict_attribute_2 | gifts > men > novel > predict_attribute1 > predict_attribute_2, http://mystore.com/konyv?id=122, http://mystore.com/images/122.jpg, false, 29, "D. Dawkins", blue, 5 star
    
    233, The Lucifer Effect, book > psychology > mental > predict_attribute1 > predict_attribute_2 | book > psychology > mental > predict_attribute1 > predict_attribute_2 | book > psychology > mental > predict_attribute1 > predict_attribute_2, http://mystore.com/konyv?id=233, http://mystore.com/images/233.jpg, true, 23, "Ph. Zimbardo", red, 3 star

### Generating a Sales Item Catalogue for Import into Suite

 The **sales_item** catalogue contains the specific items purchased in every order, including all order information as well. After the initial import of the historical data, updates should be performed automatically on a daily basis. The sales_items import should only comprise the delta (i.e. only the orders which occurred that day). The sales item catalogue must be uploaded as a UTF-8 Unicode encoded, .CSV (comma separated values) file. The first line is the header. It is a simple comma separated list describing what the columns are. Subsequent lines contain fields in the order defined in the header.

#### Required Fields

 The following fields are necessary for reporting:

- **order** - the order ID of the order that this item was purchased in.
- **date** - the date of the purchase
- **customer** - the ID of the customer who made the purchase. This must be an external key pointing to a field in the Suite contacts table.
- **item** - the ID of the product that was purchased.
- **c_sales_amount** - the total amount of this sales item (i.e. unit price * quantity).
- **quantity** - the number of items bought.
 
<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px solid #999;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">It is possible to add custom fields to the sales_items table as long as the field name starts with prefix "c_"</td></tr></tbody></table>#### Sample Data

 Below is an example of how a sales_item file might look:


    order,date,customer,item,quantity,c_sales_amount
    123,2011-01-01,987654,JNS-456,1,145
    124,2012-12-24,654321,JCK-712,1,123.99
    125,2013-06-04,753861,SCR-111,1,250
    125,2013-06-04,753861,JNS-465,2,290

### Additional Fields

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px solid #999;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">For more information on using fields in Suite, see the document *Suite Field IDs and Values*.</td></tr></tbody></table>
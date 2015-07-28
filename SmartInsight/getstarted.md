---
title: 'Getting Started with Smart Insight'
tags: 'GettingStarted_SmartInsight, SmartInsight'
old_url: 'http://emarsys.dev/smart-insight/getstarted/'
---

Introduction
------------

 Smart Insight is an integrated solution for marketers that utilizes customer data from various touch points in order to provide actionable intelligence focused on customer engagement. Smart Insight addresses the following primary requirements of data-driven marketing:

- The need to collect, physically store and analyze continuously-rising data volumes
- The need to convert data into actionable intelligence
- The need to use this intelligence to engage with contacts according to where they are in the customer lifecycle
 
[![Overview of the Smart Insight data flow](/assets/images/Smart_Insight_EUG_Page_03_Image_0002.png)](/assets/images/Smart_Insight_EUG_Page_03_Image_0002.png)Product Benefits
----------------

 Smart Insight enables the storing of large volumes of data in a Big Data model, which provides real-time, clear, transparent and actionable intelligence. Smart Insight is delivered with built-in analysis algorithms focused on customer lifecycle marketing, which display their results on pre-configured screens. To populate these screens, Smart Insight uses data from external transactional databases in combination with automatically tracked website behavior and campaign response data from Emarsys eMarketing Suite. The "out-of-the-box" installation immediately delivers the following benefits, which are described in more detail below.

### Analysis and Segmentation Screens

#### Customer Lifecycle Module

 The Customer Lifecycle module lets you track your goals to identify where action is needed to improve results. Customer Lifecycle analysis is based on engagement, Recency, Frequency and Monetary (eRFM) scoring, whereas Lead Lifecycle analysis based on recency and frequency of engagement.

#### Product Affinity Module

 The Product Affinity module displays your product categories and shows how many of your contacts have expressed an interest in them. You can use this information to segment your contacts and target them with more relevant product information. These default screens have been designed to cater to the eMarketing needs of ecommerce organizations. The addition of further, customizable screens and data sets beyond the standard setup is also possible; please contact Emarsys Support for details.

### Data Analysis

#### Smart Insight Profiler

 Emarsys collects your historical purchase data (default is last 2 years of data) and runs it through clustering algorithms, and makes eRFM parameter recommendations for you. These parameters will in turn be used to segment contacts automatically on the Customer Lifecycle screen.

### Web Extend

 This is an online behavior data collection script, which captures valuable information from your website and uses this for engagement scoring (contact behavior) and affinity scoring (product clustering).

#### Data Retention

 Every three months, the Smart Insight database is purged of all eCommerce data older than two years. If you want to access data over a longer period than this, you can specify a different timeframe during the setup process â&#128;&#147; but please note that additional costs may be incurred.

<table cellpadding="1" class="wikitable" style="width: 100%;border: 0px solid #999"><tbody><tr><td scope="col" style="text-align: left;border: 0px solid #999;vertical-align: top" width="60px">[![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999;vertical-align: top;color: #555555">The age of the data is defined by the value in the order date field rather than import date. This is a mandatory field for all eCommerce data imports.</td></tr></tbody></table>Getting Started with Smart Insight
----------------------------------

 This section describes the screens available with Smart Insight, their information and controls.

### Setup

 Every Smart Insight implementation starts with the Setup. This involves two important steps which will lay the foundation for your future customer engagement strategy.

- Data migration All the relevant data from your web shop (sales items and product catalogue), your Suite account and any other external sources is imported into Smart Insight in a one-off, manual import. After the initial import of the historical data, updates should be performed automatically on a daily basis. The product catalogue import is a complete import of all the data and the sales items import should only comprise the delta (i.e. only the orders happened that day).
- Configuration In cooperation withÂ Emarsys Support and the Emarsys Customer Intelligence Consultants, you decide which parameters to use to ensure that the Smart Insight screens and dashboard fit your business model. This includes laying down the framework for your customer lifecycle (e.g. deciding after how many days a lead becomes â&#128;&#152;coldâ&#128;&#153;) as well as operational aspects such as setting up the automated import mechanism. The configuration is largely determined by the recommendations made by the Smart Insight profiler report.
 
<table cellpadding="1" class="wikitable" style="width: 100%;border: 0px"><tbody><tr><td scope="col" style="text-align: left;border: 0px solid #999;vertical-align: top" width="60px">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999;vertical-align: top;color: #555555">In order for the data that you import from different sources to match and give you actionable intelligence on your customers, you must make sure that the unique identifier that you use for your web shop customers matches the external key used in Suite. This is best done by making use of the Suite **externalID** field.</td></tr></tbody></table> Smart Insight has a standard deployment which includes two modules, the **Customer Lifecycle Module** and the **Product Affinity Module** (described in more detail below). Should you feel that the standard screens do not fully match your business case, you can contactÂ Emarsys Support to discuss the possibility of designing further, custom screens. Please note that additional costs may be incurred for additional custom development.

### Layout and Controls

 The available Smart Insight screens are all accessed via the left navigation menu and comprise two main elements:

#### Main Section

 This is the main part of the interface where the data is displayed in graphical form. In some screens there is a hierarchy of data, either going from top to bottom or from left to right. This means that if you make a selection in one chart, the neighboring charts will update their content accordingly. For example, on the **Customer Lifecycle** screen, if you select a subsection of the **Customers per lifecycle status** graph, the **Customers by buying status** graph will show the breakdown for only those contacts.

#### Filters

 This is the panel on the right. All screens beside the Customer Lifecycle Dashboard allow you to use these filters to refine the displayed contacts and save your selection as a segment. The total number of contacts displayed at any one time is shown in a counter at the top. This total gives you an indication of the size of the available segment. Note: To use this segment as the source for a Suite email campaign, you must use it to create a Suite segment (in the **Contacts** menu, **Segments**, **Segment Details**). Below this are the filters which you can use to fine-tune your segments or views. Up to six filters can be defined for each screen during Setup. If more are required, please contact Emarsys Support. Every selection you make will automatically refresh the reports. In addition to the checkboxes for selecting values, the filters also show more controls if you hover your mouse cursor over them. [![Smart Insight EUG Page 07 Image 0005.png](/assets/images/Smart_Insight_EUG_Page_07_Image_0005.png)](/assets/images/Smart_Insight_EUG_Page_07_Image_0005.png)

<table class="wikitable"><tbody><tr><td>[![Smart Insight EUG Page 07 Image 0002.png](/assets/images/Smart_Insight_EUG_Page_07_Image_0002.png)](/assets/images/Smart_Insight_EUG_Page_07_Image_0002.png)</td> <td>Opens a text box so that you can search for a specific value.</td> </tr><tr><td>[![Smart Insight EUG Page 07 Image 0003.png](/assets/images/Smart_Insight_EUG_Page_07_Image_0003.png)](/assets/images/Smart_Insight_EUG_Page_07_Image_0003.png)</td> <td>Displays more or fewer values for the field (this is configured during Setup).</td> </tr><tr><td>[![Smart Insight EUG Page 07 Image 0004.png](/assets/images/Smart_Insight_EUG_Page_07_Image_0004.png)](/assets/images/Smart_Insight_EUG_Page_07_Image_0004.png)</td> <td>Here you can decide whether the field values are single-choice or multiple-choice, and also whether the selected values are included or excluded from the segment.</td></tr></tbody></table> In addition to this, the following controls are located in a panel at the bottom of the page, which enable a range of further actions:

<table class="wikitable"><tbody><tr><td>[![Smart Insight EUG Page 08 Image 0006.png](/assets/images/Smart_Insight_EUG_Page_08_Image_0006.png)](/assets/images/Smart_Insight_EUG_Page_08_Image_0006.png)</td> <td>This displays the name of the current view (default is Original view). If you customize a screen and want to save that view for future reference, click this control. Here you can save the view as well as select other views. You can also rename or delete views by clicking Manage Custom Views.</td> </tr></tbody><thead><tr><td>[![Smart Insight EUG Page 08 Image 0002.png](/assets/images/Smart_Insight_EUG_Page_08_Image_0002.png)](/assets/images/Smart_Insight_EUG_Page_08_Image_0002.png)</td> <td>Save the selected contacts as a Smart Insight segment. This segment will then be accessible in the Suite segment page and can be used as a starting point for a creating a new Suite segment. This button does not appear in the Dashboard. <table border="0" cellpadding="1" class="wikitable" style="width: 100%;border-width: 0px;border-style: solid"><thead><tr><th style="text-align: left;border-color: #fff;background-color: #fff;color: #eb5a19">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left;border-color: #fff;background-color: #fff;color: #555555">When you save a Smart Insight segment it will overwrite any existing segment with the same name. All Suite segments based on it will henceforth take the new values as their source.</td> </tr></tbody></table></td> </tr></thead><tbody><tr><td><div class="floatnone">[![Smart Insight EUG Page 08 Image 0003.png](/assets/images/Smart_Insight_EUG_Page_08_Image_0003.png)](/assets/images/Smart_Insight_EUG_Page_08_Image_0003.png)</div></td> <td>Export the data in one of the supported file formats.</td> </tr><tr><td>[![Smart Insight EUG Page 08 Image 0004.png](/assets/images/Smart_Insight_EUG_Page_08_Image_0004.png)](/assets/images/Smart_Insight_EUG_Page_08_Image_0004.png)</td> <td>Revert all visualization or filter selections and return to initial reporting mode.</td> </tr><tr><td>[![Smart Insight EUG Page 08 Image 0005.png](/assets/images/Smart_Insight_EUG_Page_08_Image_0005.png)](/assets/images/Smart_Insight_EUG_Page_08_Image_0005.png)</td> <td>Pause/Resume the screen refresh. Every selection you make refreshes the screen, so pause this feature if you want to make multiple selections or apply complex filters.</td> </tr><tr><td>[![Smart Insight EUG Page 08 Image 0007.png](/assets/images/Smart_Insight_EUG_Page_08_Image_0007.png)](/assets/images/Smart_Insight_EUG_Page_08_Image_0007.png)</td> <td>Manually refresh the screen. However, the data is updated once a day, so you will probably not need to use this button very often.</td></tr></tbody></table>The Customer Lifecycle Module
-----------------------------

 This module consists of three screens:

- Dashboard
- Customer Lifecycle
- Lead Lifecycle

 These three screens display your contact database in terms of the eRFM scoring that was defined during setup, and based on the recommendations resulting from the **Smart Insight Profiler** analysis.

### The Dashboard

 The Smart Insight Dashboard is where you can see an overview of your customer lifecycle eMarketing goals, and how you are currently performing against them. The goals are defined in terms of moving contacts from one lifecycle stage to another.

<table border="0" cellpadding="1" class="wikitable" style="width: 100%;border-width: 0px;border-style: solid"><thead><tr><th style="text-align: left;border-color: #fff;background-color: #fff;color: #eb5a19">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left;border-color: #fff;background-color: #fff;color: #555555">The **Dashboard** is used for reporting and not for segmentation. This means you cannot save the contacts that are displayed and use them to create a Suite segment.</td></tr></tbody></table> On the **Dashboard** you get an overview of your three main customer lifecycle marketing goals:

- Lead Conversion
- Active Buyers revenue growth
- Win-back rate of Active Buyers
 
[![The Smart Insight Dashboard](/assets/images/Smart_Insight_EUG_Page_09_Image_0002.png)](/assets/images/Smart_Insight_EUG_Page_09_Image_0002.png)#### Goal Tracking

##### Number of Orders

 The goal tracking graphs show the number of orders made by contacts associated with each goal, which displays the last six months' worth of results. The current month is colour-coded so that you can get a visual indication of the status

- *Red* indicates performance is worse than the previous month
- *Green* indicates that performance is better than the previous month

 In addition to this, the current month displays content in two colours: the darker colour shows you the current data so far, and the lighter one is the end-of-month projection, assuming the monthly average daily rate is maintained.

##### Revenue

 For each goal you can also see the associated revenue: total monthly revenue from first-time orders for leads and/or total monthly revenue from win-back orders, and average monthly revenue from active customers.

<table cellpadding="1" class="wikitable" style="width: 100%;border: 0px solid #999"><tbody><tr><td scope="col" style="text-align: left;border: 0px solid #999;vertical-align: top" width="60px">[![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999;vertical-align: top;color: #555555">The main use case for the Dashboard is to compare the activity on your web shop month by month and use that to judge the effectiveness of your current marketing campaigns.</td></tr></tbody></table>### Customer Lifecycle Screen

 The **Customer Lifecycle** screen gives a breakdown of contact distribution in terms of lifecycle stage and spending value. This data is not displayed over a defined time period, but is a snapshot of the current database status (i.e. accurate to the most recent import). The three shades of colour group the contacts according to their engagement scores for each status (see below for information on how the eRFM scoring works). [![The Customer Lifecycle screen](/assets/images/Smart_Insight_EUG_Page_11_Image_0002.png)](/assets/images/Smart_Insight_EUG_Page_11_Image_0002.png)

#### Customer per Lifecycle Status

 This section shows how your contact base is distributed across the various customer lifecycle stages, with a numeric breakdown associated with each.

#### Customers by Buying Status

 This section shows how the spending power is distributed across all or the selected lifecycle stages.

#### Measure-Value Type

 As well as the standard filters, you can display your customer lifecycle statistics according to the following metrics:

- **Total spent** (over the last two years, by all the contacts in this lifecycle stage)
- **Average spent** (over the last two years, per contact in each lifecycle stage)
- **Number of contacts** (todayâ&#128;&#153;s figure for this lifecycle stage)
 
<table cellpadding="1" class="wikitable" style="width: 100%;border: 0px solid #999"><tbody><tr><td scope="col" style="text-align: left;border: 0px solid #999;vertical-align: top" width="60px">[![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999;vertical-align: top;color: #555555">- You can use this screen to analyze the experience your web shop offers customers. For example, high numbers of defecting first-time buyers might indicate problems in your shipping or billing processes that put customers off making a second purchase.
- You can also segment your contact by source and see which acquisition channels are performing better and which need investment.
 
</td></tr></tbody></table>### Lead Lifecycle Screen

 The **Lead Lifecycle** screen gives a breakdown of leads, i.e. contacts in your database who have never made a purchase. [![The Lead Lifecycle screen](/assets/images/Smart_Insight_EUG_Page_12_Image_0003.png)](/assets/images/Smart_Insight_EUG_Page_12_Image_0003.png)

#### Leads by Lifecycle Status

 This section shows how your leads are distributed across the various lead lifecycle stages, with the total for each of them.

#### Leads by Lead Source

 This section indicates the source from which the leads originated, from manual and automatic imports through to leads generated by individual registration forms.

<table cellpadding="1" class="wikitable" style="width: 100%;border: 0px solid #999"><tbody><tr><td scope="col" style="text-align: left;border: 0px solid #999;vertical-align: top" width="60px">[![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999;vertical-align: top;color: #555555">This screen gives you detailed insights into the way your web shop attracts new customers, and how successful your welcome campaigns are.</td></tr></tbody></table>The Product Affinity Module
---------------------------

 This module consists of two screens:

- Purchases
- Affinity

 These two provide ready-made segments of your contacts according to the products they bought or are likely to be interested in a product category based on their website behavior

### Purchases Screen

 The **Purchases screen** gives a breakdown of purchase behaviour in terms of products and product categories. [![The Purchases screen](/assets/images/Smart_Insight_EUG_Page_14_Image_0002.png)](/assets/images/Smart_Insight_EUG_Page_14_Image_0002.png)

#### Purchases by Product Category

 This section shows the total number of contacts who have purchased items in each product category over the last two years.

#### Purchases by product name

 This section shows the total number of contacts who have purchased each product. If a product category has been selected, only those products are shown, otherwise all products will be displayed.

<table cellpadding="1" class="wikitable" style="width: 100%;border: 0px solid #999"><tbody><tr><td scope="col" style="text-align: left;border: 0px solid #999;vertical-align: top" width="60px">[![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999;vertical-align: top;color: #555555">You can use this screen to make your emails more relevant, for example by saving a segment of contacts who have already bought a product, and excluding it from promotional campaign for that product. You can also schedule reminder campaigns for products which require refills or maintenance.</td></tr></tbody></table>### Affinity Screen

 The **Affinity Screen** gives a breakdown of the top product categories that your contacts are interested in based on their website behaviour. Smart Insightâ&#128;&#153;s machine learning algorithms score all categories per contact and the displays the top 3 categories per customer. [![The Affinity screen](/assets/images/Smart_Insight_EUG_Page_15_Image_0003.png)](/assets/images/Smart_Insight_EUG_Page_15_Image_0003.png) The **Affinity screen** is based on the data that is automatically captured from the website, using the Emarsys **Web Extend** collection script.

#### Last Website Visit Date

 This graph displays the last time that your contacts visited your web shop. In this way you can see how many of your contacts are regular visitors, as well as compare behavior by lifecycle stage.

#### Affinity to Product Categories

 On this chart you can see which product categories are the most popular, according to the Smart Insight analysis.

<table cellpadding="1" class="wikitable" style="width: 100%;border: 0px solid #999"><tbody><tr><td scope="col" style="text-align: left;border: 0px solid #999;vertical-align: top" width="60px">[![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999;vertical-align: top;color: #555555">You can use this screen to filter product categories by customer lifecycle and see which are more popular with regular buyers and which with new customers. You can also segment contacts by their affinity to a category and use that segment for targeted campaigns such as stock clearance or special offers.</td></tr></tbody></table>Working with Tables, Charts and Graphs
--------------------------------------

 Smart Insight uses interactive elements for data visualisation in the form of line graphs and bar charts. It is possible, and sometimes necessary, to make a selection on these graphs to fine-tune the segmentation, populate other graphs or just to exclude specific data sets when generating reports.

### Filtering the contacts

 In each screen Smart Insight displays all the contacts which fulfil the criteria appropriate to that screen - with the exception of the Dashboard. The total number is displayed in the box in the top right, above the filters. You can then fine-tune the selection by using the checkboxes and other controls. The available filters will depend on the screen in question.

### Save Segment from Selected Contacts

 The **Save Segment** button allows you to save the selected contacts as a Smart Insight segment. These can then be selected in the Suite **Segment Details** page and used as the source for a standard Suite segment. [![Use Smart Insight segments](/assets/images/Smart_Insight_EUG_Page_17_Image_0002.png)](/assets/images/Smart_Insight_EUG_Page_17_Image_0002.png)

### Rollover Tool Tips

 Many of the Smart Insight screens and graphs have interactive controls which display when the mouse cursor is held over them.

#### Sorting contacts

 Clicking the axes of any of the graphs or charts will display icons for sorting the contacts. [![Sorting contacts controls](/assets/images/Smart_Insight_EUG_Page_17_Image_0003.png)](/assets/images/Smart_Insight_EUG_Page_17_Image_0003.png) The available options (depending on the graph or chart in question) are:

- Sort Ascending
- Sort Descending
- Sort A-Z

#### Keeping and Excluding Results

 When you have results displayed in a bar chart, it can be that one column (e.g. Leads) is much larger than the others, making it difficult to view the smaller ones. You can exclude this column by hovering the mouse over it and selecting **Exclude**. Alternatively, you can hover over another column and select **Keep Only** to exclude all other columns. This pop-up also shows you exactly what criteria lie behind the graph. In addition, you can drill down to see the detailed analysis of a graph by clicking the **Show Data** icon. To return to the full display, click the **Revert All** icon at the bottom of the screen. [![Viewing the Details of a Lifecycle Stage](/assets/images/Smart_Insight_EUG_Page_18_Image_0003.png)](/assets/images/Smart_Insight_EUG_Page_18_Image_0003.png)

#### Zooming In and Out

 You can also use the following controls to zoom in and out of each visualisation:

<table class="wikitable"><tbody><tr><td>[![Smart Insight EUG Page 18 Image 0004.png](/assets/images/Smart_Insight_EUG_Page_18_Image_0004.png)](/assets/images/Smart_Insight_EUG_Page_18_Image_0004.png)</td> <td>Zoom in</td> </tr><tr><td>[![Smart Insight EUG Page 18 Image 0005.png](/assets/images/Smart_Insight_EUG_Page_18_Image_0005.png)](/assets/images/Smart_Insight_EUG_Page_18_Image_0005.png)</td> <td>Zoom out</td> </tr><tr><td>[![Smart Insight EUG Page 18 Image 0006.png](/assets/images/Smart_Insight_EUG_Page_18_Image_0006.png)](/assets/images/Smart_Insight_EUG_Page_18_Image_0006.png)</td> <td>Drag to select zoom</td> </tr><tr><td>[![Smart Insight EUG Page 18 Image 0007.png](/assets/images/Smart_Insight_EUG_Page_18_Image_0007.png)](/assets/images/Smart_Insight_EUG_Page_18_Image_0007.png)</td> <td>Restore zoom to 100%</td></tr></tbody></table>### Selecting Data in Visualizations

 If you do not want to select all the results in a particular screen (for example if you want to save a subset as a smaller segment), you can refine your visualisation in various ways:

- Click a bar or chart to select an individual entry. This may then affect the results in other graphs and charts.
- Click the label on the x-axis to select the entire column.
- Click and drag to select multiple entries.
- Hold CTRL key and click or drag to select multiple entries (either add to or remove from the selection).

The Smart Insight Scoring Model
-------------------------------

 Smart Insight uses the eRFM scoring model to build the out-of-the-box screens. This model is a method used for analysing customer behaviour and then defining segments based on this behaviour. It is commonly used in database marketing and direct marketing, both online and offline.

### eRFM Scoring

 The eRFM model categorises contacts by four aspects of their behaviour and allows Smart Insight to decide whether an individual is, for example, a cold lead, active buyer or defecting gold customer. The categorisation is done by matching the contactâ&#128;&#153;s behaviour to the parameters defined during setup, and is based on the analysis provided by the Smart Insight profiler. The graphic below illustrates how these parameters might look in a typical Smart Insight account. [![An example of an eRFM scoring model](/assets/images/Smart_Insight_EUG_Page_19_Image_0002.png)](/assets/images/Smart_Insight_EUG_Page_19_Image_0002.png)

### Customer Lifecycle Terminology

 Smart Insight has two categories of contacts:

- **Leads:** Contacts that have never made a purchase. For these contacts, only date of registration and engagement are analysed.
- **Customers:** Contacts that have made a purchase

 Within these two categories the lifecycle stages are identified based on activity, and can be broken down as follows (the numbers below are just for example, and can be defined during Setup):

#### Leads

<table class="wikitable"><thead><tr><th>New Lead</th> <td>Registration was within the last 90 days, no response yet (beyond opt-in)</td> </tr><tr><th>Active Lead</th> <td>At least one response in the last 90 days</td> </tr><tr><th>Cold Lead</th> <td>No response for more than 90 days</td> </tr><tr><th>Inactive Lead</th> <td>No response for more than 180 days</td></tr></thead></table>#### Customers

<table class="wikitable"><thead><tr><th>1<sup>st</sup> time buyer</th> <td>Only one purchase ever, made in the last 90 days</td> </tr><tr><th>Active buyer</th> <td>Made a purchase in the last 90 days and has made more than one purchase in total</td> </tr><tr><th>Defecting buyer</th> <td>Has not made a purchase in the last 90 days but has made at least one purchase in the past</td> </tr><tr><th>Inactive buyer</th> <td>Has not made a purchase in the last 365 days but has made at least one purchase in the past</td></tr></thead></table>#### Buying Status

 The **Buying Status** categorizes customers based on their spending levels using the last two yearsâ&#128;&#153; worth of historical data. The actual amounts for each threshold are defined during Smart Insight Setup.

<table class="wikitable"><thead><tr><th>Low spender</th> <td>e.g. up to â&#130;¬50</td> </tr><tr><th>Normal</th> <td>e.g. up to â&#130;¬200</td> </tr><tr><th>Silver</th> <td>e.g. up to â&#130;¬500</td> </tr><tr><th>Gold</th> <td>e.g. up to â&#130;¬1000</td> </tr><tr><th>Platinum</th> <td>e.g. more than â&#130;¬1,000</td></tr></thead></table>### Preparing your Reports

 During Smart Insight setup you will be presented with Smart Insight Profiler reports and recommendations based on an analysis of your data. You will then define, with Emarsys Support, the parameters, scale and terminology that will determine the scope of your reports. The following variables must be defined:

- eRFM parameters For example, a cut-off point for Recency could be <45 days instead of <30, for Monetary could be > â&#130;¬5,000 instead of > â&#130;¬1,000, etc.
- Terminology Which terms to use, e.g. *Small spender* instead of *Low spender*, etc.
- Number and types of filters per screen Up to six filters can be defined per screen in the standard configuration, and any field from the defined fields or tables can be used.

 In addition to this, some further customisation options are available, but which will incur development costs; if you feel these are necessary please consult Emarsys Support.

Smart Insight Data Migration
----------------------------

 As part of the standard, "out-of-the-box" installation, two types of data sets must first be imported to the Smart Insight data warehouse:

- All the contacts in your Suite database. You only have to decide which Suite fields you want available as filters in Smart Insight and Emarsys will do the rest.
- External transactional data This is typically the **products** and **sales_items** tables from your web shop.
- Web Extend Here you will need to implement our behaviour collection script in your web pages.

 After the initial, manual import, Smart Insight is updated once a day with new data from all sources. The Suite response data (as well as any relevant contact updates) is synced automatically via the Suite API. Data from other sources must be placed by you in a defined FTPS server, where it will be collected once a day.

<table cellpadding="1" class="wikitable" style="width: 100%;border: 0px"><tbody><tr><td scope="col" style="text-align: left;border: 0px solid #999;vertical-align: top" width="60px">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999;vertical-align: top;color: #555555">In order for the data to be matched to the right person, you must make sure that the unique identifier that you use for your web shop customers matches the external key used in Suite. This is best done by making use of the Suite **externalID** field.</td></tr></tbody></table>### Uploading Web Shop Database Tables

 During Setup every customer is given access to an FTPS account where they can upload the CSV files containing the data to be imported to Suite. These are typically the **Products** table and the **Sales_items** table as defined below. Once Smart Insight is fully implemented, files added to this directory are processed automatically.

<table cellpadding="1" class="wikitable" style="width: 100%;border: 0px"><tbody><tr><td scope="col" style="text-align: left;border: 0px solid #999;vertical-align: top" width="60px">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999;vertical-align: top;color: #555555">Files that don't follow the conventions in this document (below and in the appendix) are silently ignored. This means that you will not receive any notification that the import has failed. It is therefore extremely important that you follow the rules and conventions described below.</td></tr></tbody></table> In the Smart Insight standard installation, data from your web shop database is broken down into three tables: Customers table, Products table and Sales_items table, which are uploaded as follows:

- Customers table This is synchronised with the Suite contact database via the Suite API and requires no action by you.
- Products table This is your entire product catalogue and should be uploaded daily by you to the FTPS as a CSV file.
- Sales_items table This is a delta file (i.e. containing only new data) of recent purchases, added daily by you to the FTPS as a CSV file.

 For both the **products** table and the **sales_items** table, the data import is automatically processed from the FTPS account and the files are recognised via the following naming convention:

- products*.csv
- sales_items*.csv

 See below for more information on the naming of import files.

### Required Fields for Reporting

 For Smart Insight to be able to create actionable reports based on order data, you must add custom fields in the import that you can use for filtering. The following fields are mandatory and are considered the bare minimum of what should be passed to Smart Insight to ensure meaningful reporting.

#### Products

 In order to ensure that Smart Insight has access to the latest data, you should be importing your entire product catalogue every day. This is the **products** file.

<table class="wikitable"><thead><tr><th>item</th> <td>The unique identifier of the product</td> </tr><tr><th>title</th> <td>The name of the product</td> </tr><tr><th>category</th> <td>The product category, expressed within your category hierarchy (see below)</td></tr></thead></table>  

<table cellpadding="1" class="wikitable" style="width: 100%;border: 0px"><tbody><tr><td scope="col" style="text-align: left;border: 0px solid #999;vertical-align: top" width="60px">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999;vertical-align: top;color: #555555">When Smart Insights detects duplicates in product files, the newer values overwrite the old values.</td> </tr></tbody></table><table cellpadding="1" class="wikitable" style="width: 100%;border: 0px solid #999"><tbody><tr><td scope="col" style="text-align: left;border: 0px solid #999;vertical-align: top" width="60px">[![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999;vertical-align: top;color: #555555">Smart Insight supports a structure category hierarchy with up to three levels. Levels should be separated by a greater than character (>) and the most generic category should be the first one. Example: pets > dogs > dog food If you enter simply 'dog food' as the category, Smart Insight will look for this as a top-level category and the import will fail.</td></tr></tbody></table>#### Sales_items

 Each day you should upload also only the "delta" of your orders, i.e. the orders that happened that day. **sales_item** data contains the specific items purchased in every order, including all order information as well. The following fields are necessary for reporting:

<table class="wikitable"><thead><tr><th>order</th> <td>The unique identifier of the order that this item was purchase in</td> </tr><tr><th>date</th> <td>The date of the purchase</td> </tr><tr><th>customer</th> <td>The identifier of the customer who made the purchase. This must be an external key pointing to a field in the Suite contacts table.</td> </tr><tr><th>item</th> <td>The identifier of the product that was purchased</td> </tr><tr><th>c_sales_amount</th> <td>The total amount of this sales item (i.e. unit price * quantity)</td> </tr><tr><th>quantity (optional)</th> <td>The number of items bought</td> </tr><tr><th>unit price (optional)</th> <td>The unit price of the item purchased</td></tr></thead></table>  

<table cellpadding="1" class="wikitable" style="width: 100%;border: 0px"><tbody><tr><td scope="col" style="text-align: left;border: 0px solid #999;vertical-align: top" width="60px">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999;vertical-align: top;color: #555555">Duplicate entries in a sales_items file are not detected; they will appear as two identical entries in the Smart Insight reports.</td> </tr></tbody></table><table cellpadding="1" class="wikitable" style="width: 100%;border: 0px solid #999"><tbody><tr><td scope="col" style="text-align: left;border: 0px solid #999;vertical-align: top" width="60px">[![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999;vertical-align: top;color: #555555">It is possible to add extra optional fields to the sales items table as long as the field name starts with "c_"</td> </tr></tbody></table><table cellpadding="1" class="wikitable" style="width: 100%;border: 1px solid #fff"><tbody><tr><td scope="col" style="text-align: left;border: 0px solid #999;vertical-align: top" width="60px">[![Icon FurtherReading.png](/assets/images/Icon_FurtherReading.png)](/assets/images/Icon_FurtherReading.png)</td> <td scope="col" style="border: 0px solid #999;vertical-align: top;color: #555555">For more information on working with the products table or sales_items table, as well as general tips on working with .CSV files, please see the [Data Exchange Quick Reference Guide](/SmartInsight/data-quick-ref.md "Data Exchange Quick Reference Guide").</td></tr></tbody></table>Smart Insight Tips and Tricks
-----------------------------

### Some Field Basics

#### Contact Fields

 Before setting up Smart Insight you will have liaised with Emarsys Support to identify which contact fields should be imported into Smart Insight and which ignored. As your business evolves, you can always check to see if you have the most appropriate fields by asking yourself the following questions:

- What data do you want to see in your reports?
- Which fields do you want to be able to use in order to filter or segment?
- Do these fields contain any data?

#### Linking the unique identifier

 Contacts in the Suite Contact Database must be matched correctly with their corresponding orders using a unique identifier. This identifier appears in the Suite contacts table as **externalID**, and must be included and populated in order for the association to work.

#### Mandatory Fields

 During the initial configuration of Smart Insight fields it is possible to define certain fields as mandatory, meaning that they have to contain data in order for the import to be processed correctly. If a mandatory field is left blank, then the data import will fail.

#### Product Category

 The Smart Insight template supports up to three product categories for each item, which can be used to filter the reports. For this to work correctly a main category always has to be defined per item during Setup, as this will decide which category is displayed in the **Purchases** screen.

#### Using the appropriate currency

 At the moment there is no multi-currency support, so all data must use the same currency for all monetary values. The currency is specified during Setup, and cannot be changed.

#### Handling Order Duplication Issues

 In order that your daily delta imports do not cause duplication of data, you must ensure that every import has valid and unique order IDs. If this is not the case, Smart Insight will perform on very basic duplication handling:

- If an import contains duplicated order IDs, the second order will simply be ignored.
- If an order ID is missing, any subsequent order items will be assumed to belong to the previous order and will be associated with it.

#### Handling Erroneous Contact Data

 The benefits that Smart Insight brings are heavily dependent on the quality of the data you import. If you do not take care to ensure that your CSV files follow the guidelines described above, the following errors might occur.

- Multiple contacts with the same unique identifier Make sure that whatever field you use really is unique to that contact. If you are exporting or importing contact data into Suite you should try to use the same field as external ID to prevent duplication of data.
- Invalid Date Information in a Date Field Smart Insight expects all date fields to contain dates, or no dates at all - any malformed date entries will cause errors.
- Invalid Choice Field Entries If a multiple-choice field contains more entries than the field has values, this will cause the data import to fail.
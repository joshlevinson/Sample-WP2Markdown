---
title: 'Suite Version 8.2'
tags: Roadmap
old_url: 'http://emarsys.dev/development/suite-version-8-2/'
---

##### February, 2015

 Version 8.2 was a minor release which focused on three areas of the Suite platform: [column width="eight" place="first" ]

##### Improvements to the core Suite functionality

- [A new wizard for configuring auto-imports](#auto-import)
- [Trend reporting for on-event campaigns](#on-import)
- [PDF export for trend reporting](#pdf-export)
- [BCC field for transactional emails](#bcc)
- [More notifications](#nc)

 [/column] [column width="eight" place="second" ]

##### Improvements to Smart Insight

- [Predictive revenue figures on the Customer Lifecycle dashboard](#clc)
- [A new Revenue Impact screen](#revenue-impact)
- [Enhanced filter criteria for creating Smart Insight segments](#si-segments)
- [Refined lead conversion classification](#lead-conversion)
- [Miscellaneous enhancements](#misc-si)

##### Improvements to Predict

- [New Predict Web Recommender widget: Category](#category-widget)
- [Export of the purchase data collected by Predict](#purchase-data)
- [A new Site Traffic tab for the Predict Statistics screen](#traffic)

 [/column]

Improvements to the Core Suite Functionality
--------------------------------------------

#### <a name="auto-import"></a>1. Auto-Import Wizard

 You can now easily and independently set up automated data synchronization between Suite and your database/CRM with our new, intuitive auto-import setup wizard. The **Auto-import** feature can be found in the **Contacts** menu:

<div class="row">[![auto-import-list](/assets/images/auto-import-list-1024x381.png)](/assets/images/auto-import-list.png)</div> This opens an overview page with a list of your existing auto-imports.

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">It may be that some older auto-imports, for example those involving on-import campaigns or without duplication handling, are not displayed. This is because they are using functionality that is currently not supported by our new import wizard. To edit these auto-imports, please contact Emarsys Support.</td></tr></tbody></table> To configure a new auto-import, simply follow the instructions on the intuitive new wizard. Click here for the[ user documentation](/Suite/auto-imports.md "Auto-Imports") including a comprehensive [FAQ](/Suite/import-faq.md "Data Import FAQ").

<div class="row">[![](/assets/images/auto-import.png)](/assets/images/auto-import.png)</div>#### <a name="on-import"></a>2. Trend reporting for on-event campaigns

 This involves two important changes to the campaign reporting:

- New reporting pages have been provided for on-event campaigns. Now you can view the results of an on-event campaign over time, instead of simply the total aggregated responses since the first launch (though these are still available via the **View Full Report** link). [Click here for details...](/Suite/trend-reporting.md "Suite: Trend Reporting")
- The **Trends** page now includes on-event campaigns, giving you a better overall analysis of your marketing strategies on an account level.

#### <a name="pdf-export"></a>3. PDF export for the Trend Reporting page

 You can now publish your results from the **Trend Reporting** page to .PDF as well as to .CSV.

#### <a name="bcc"></a>4. BCC field for transactional emails

 You can send blind copies of all transactional emails, for example for archive or reference purposes. This feature is restricted to three email addresses, which must all belong to the main sender domain configured for your account (for example, if your main sender domain is *reply.emarsys.com*, then any email address ending *@emarsys.com* will be accepted). You add the BCC email addresses on the **Campaign Settings** page of the Suite CMS. BCC emails are not counted for analysis or billing.

#### <a name="nc"></a>5. New messages for the Notification Center

 There are also a number of new alerts for the Notification Center:

- Auto-import status and error alerts
- Notifications on successful batch email campaign launch
- Alerts when an unusually high proportion of a launch list were discarded, which can often indicate that the target segment does not fully match the dynamic content of the email.

Improvements to Smart Insight
-----------------------------

 A number of new, smart metrics have been added to Smart Insight, giving you an even better understanding of the value of your key segments, as well as trends in customer behavior. These will help you to focus your attention on those parts of your customer lifecycle where you can make the most difference.

#### <a name="clc"></a>1. The Customer Lifecycle Dashboard - Predictive Revenue

 Each of the customer lifecycle stages have been enhanced with a new expanding section for predictive revenue. The figures in this section are calculated by analyzing the past behavior of your contacts to predict their future behavior, providing you with key metrics regarding predictive revenue. They are updated on a daily basis and are tailored to optimize retention automation.

<div class="row">[![predictive-revenue-collapsed](/assets/images/predictive-revenue-collapsed-1024x207.png)](/assets/images/predictive-revenue-collapsed.png)</div> There are four new metrics, split into two categories.

<div class="row">[![predictive-revenue-expanded_new](/assets/images/predictive-revenue-expanded_new.png)](/assets/images/predictive-revenue-expanded_new.png)</div>##### Overview of the last 30 days

 These metrics show you the overall impact on your business of the conversions from this group.

- **Revenue from current purchases** This is the total spent in all conversions from this group in the last 30 days.
- **Predicted future revenue increase** This is the additional revenue you can expect from the contacts who converted to a more valuable segment.

##### Average contact value

 These metrics give you an insight into the average value to your business of the individual contacts in this segment.

- **Average historical spend** This is how much each contact in this segment has already spent with you
- **Predicted average future spend** This is how much you can expect them to spend in the future, averaged out to reflect the fact that some with convert and some will not.
- **Average lifetime value** This is the sum of the two above metrics.

#### <a name="revenue-impact"></a>2. The Impact screens

 A new menu entry has been added to Smart Insight: **Impact**. Here we will add a series of screens which break your revenue down according to different criteria. The first of these screen focuses on retention marketing.

##### Retention Revenue

<div class="row">[![](/assets/images/revenue-retention.png)](/assets/images/revenue-retention.png)</div> Here you can see the contribution that each of your customer lifecycle segments makes to your bottom line, and measure the success of the different marketing strategies you use to engage with them. This new page provides real value because it shows the monetary value of each segment and lets you measure and compare your marketing ROI in real terms across your entire customer base. On this page you can also:

1. Hover over the graphs to see the actual figures for that month
2. Filter by contact attributes
3. Drill down to look at product categories or even individual products

<div class="row">[![](/assets/images/revenue-impact-controls1-300x218.png)](/assets/images/revenue-impact-controls1.png)</div> You can easily switch the visualization from a daily to a monthly view, or simply use the interactive time-range selector underneath to define your own view.

#### <a name="si-segments"></a>3. Smart Insight segments

 In the Suite **Segments** page (**Contacts** menu, **Segments**) the filter criteria for creating Smart Insight segments have been extended with two new options in the **Purchases** section:

<div class="row">[![si-segments](/assets/images/si-segments-240x300.png)](/assets/images/si-segments.png)</div> These two criteria refer only to the selected purchases. For example, you can now filter for contacts who have spent a certain amount or made a certain number of purchases *within a specific product category* or *with a specific brand*.

#### <a name="lead-conversion"></a>4. Re-classifying Lead Conversion

 Historically, we have always treated all new customers who make a first purchase as converted leads, no matter how soon after registration this purchase occurred. From now on, if a lead registers with a web shop and makes a purchase that same day, we treat them as direct first-time buyers and leave them out of the Leads segment altogether. This is because such a time frame is too short for your lead conversion strategy to have had any effect on these contacts, and including them skews your lead conversion statistics and makes them less reliable.

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">This new classification may lead to a dramatic fall in your lead conversion rate. However, the new rate will be a genuine reflection of the effect of your lead conversion campaigns and you will be able to measure the success of new strategies more accurately.</td></tr></tbody></table>#### <a name="misc-si"></a>5. Miscellaneous Improvements

 There have also been a number of minor improvements, giving greater flexibility in the way to categorize and score your contacts.

- **Purchase filters in the Customer Lifecycle screen** Additional filters based on product catalogue or sales items attribute fields can now be loaded to this screen on request.
- **Custom Fields as Contact Sources in the Lead Lifecycle screen.** If you want to track your lead generation sources using a dedicated custom field, this can now be implemented in the **Lead Lifecycle** screen on request.
- **More choice when selecting which product categories to display** If you are using a hierarchy of nested product categories, Smart Insight always used to take the highest level (e.g.: *Shoes*) when showing a category in the reports. Now you can request to use any of the lower levels (e.g.: Shoes/*Casual* or Shoes/*Formal*), giving you greater accuracy and flexibility.
- **Better documentation** You can now access the Smart Insight End-user Guide directly via a link in the interface (only available to AltTab customers at present).

Improvements to Predict
-----------------------

#### <a name="category-widget"></a>1. Web Recommender CATEGORY Widget

 A new Web Recommender widget has been introduced called CATEGORY, which displays personalized recommendations restricted to items within a specific category. For example, restricting the recommendations to the *T-shirts* category means that only content matching a contact's interests from this particular category will be displayed. This enables you to go one step beyond the general product recommendations and gives you the freedom to target individual customers with individual items, while staying within the broader objectives of your campaign.

#### <a name="purchase-data"></a>2. Export of purchase data

 In the Predict **Overview** page you can now extract all the purchase data collected by Predict over the last 7, 15 or 30 days, and export it. In this way you can directly compare these figures with those from your web shop and catch any errors in the integration, for example mismatched fields in the product category.

#### <a name="traffic"></a>3. Site traffic

 A new tab has been added to the Predict **Statistics** screen: **Site Traffic**.

<div class="row">[![predict-site-traffic](/assets/images/predict-site-traffic.png)](/assets/images/predict-site-traffic.png)</div> This shows you how many page views, orders, order lines (items) and how much revenue has been tracked by Predict on your web shop over the last given time period. This will help new Predict customers to follow the early stages of their integration easily from within Suite and to identify areas for optimization.
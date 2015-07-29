---
title: 'Suite Link Tracking for External Analytics'
subject: 'Suite, SuiteReporting'
old_url: 'http://emarsys.dev/suite/reporting/external-analytics/'
---

Introduction
------------

 eMarketing Suite can send tracking variables to external web analytics platforms, such as Google Analytics, to track contact behavior coming from email campaigns. This is done by adding extra variables, such as email name, email date, link category, etc. to the links in your email campaign. When a contact visits a web page via such a link, the analytics tool used by the web page can then track their behavior and match it to them via whichever identifiers (variables) have been used. In this way you can see exactly how much interest, traffic or revenue an email campaign has generated on your web shop, and segment the contacts according to their behavior. Depending on the analytics platform you use, this data can be returned to Suite automatically (if a deep integration with Emarsys exists), manually via an import, or using the Suite API. This feature is called **External Analytics** in Suite and can be activated for you by Emarsys Support. Emarsys Support can also provide you with a list of applications which integrate with Suite and help you with advice on implementing the Suite API.

How External Analytics Works
----------------------------

 A web analytics platform categorizes the information that it logs according to variables that you define during setup. The platform then sorts the data according to the selected variables, and can combine variables together to provide a really fine-tuned breakdown of contact activity. The Suite External Analytics feature works by matching the variables used by the analytics platform with Suite variables, and adding them to the URL of the links in the email. In this way the variables of the analytics are populated automatically with Suite data, for example campaign name, date, link name, etc. This can be done on an account level for all email campaigns, or on a per-campaign basis.

<div class="center"><div class="floatnone">[![Visualisation of how Web Analytics works with Suite](/assets/images/SuiteLinkTracking_Page_04_Image_0003.png)](/assets/images/SuiteLinkTracking_Page_04_Image_0003.png)</div></div>### Example of a tracking link

 A link without external tracking might look like this: `www.example.com/pagename.html` The same link using Google Analytics for tracking the email campaign and link used to access the web page could look like this: `www.example.com/pagename.html?utm_campaign=$cname$&utm_term=$clinkname$`

<table cellpadding="1" class="wikitable" style="width: 100%; border: 1px solid #fff;"><tbody><tr><td scope="col" style="text-align: left; border: 1px solid #fff;" width="60px">[![](/assets/images/Icon_FurtherReading.png)](/assets/images/Icon_FurtherReading.png)</td> <td scope="col" style="border: 1px solid #fff;">A full list of the Suite variables can be found in the Appendix of this document.</td></tr></tbody></table>Using External Analytics in Suite
---------------------------------

### Enabling the feature

 If you want to take advantage of this feature, you must ask Emarsys Support to enable it. Before you do this, you should familiarize yourself with the variables and separators used in your web analytics platform, as well as decide on the ones you want to use in Suite. You can choose between using the same variables for all your email campaigns, or change them on a per-campaign basis. If you want to use one set of variables for all email campaigns, simply provide Emarsys Support with the variable pairs which will map your web analytics tool fields with your Suite fields. If you choose to use different variables for individual campaigns, you will see a new text field in the **Email Settings** page. Here you enter the variable pairs manually and they will be added to the trackable link for that email.

<div class="center"><div class="floatnone">[![Where to enter the tracking parameters for individual email campaigns](/assets/images/SuiteLinkTracking_Page_05_Image_0002.png)](/assets/images/SuiteLinkTracking_Page_05_Image_0002.png)</div></div>### Matching the variables

 Web analytics platforms have a fixed number of variables that they use to filter content, and these are usually fewer in number than those available in Suite. When defining the variables for the analytics platform, you can therefore combine several Suite variables per analytics variable to ensure that the resulting data is filtered according to your needs. For example, if your analytics platform offers only one campaign ID variable (such as `utm_campaign` for Google), you can get around this limitation by combining several Suite variables and matching them all to this one. In this way you can create more complex filters, such as sorting responses from the same recurring campaign which occurred on different days. As well as matching standard Suite variables, a full list of which can be found in the Appendix, you can also choose to define a fixed value for the analytics variable. This is done by omitting the $ before and after the value.

#### Example of matching complex variables

 If you have a number of regular daily newsletters, you might want to be able to sort the responses in Google Analytics per newsletter by day, or compile all responses for all newsletters together. In this case you might do the following:

- match the Suite variables `$cname$`, `$cmonth$` and `$cday$` to `utm_campaign`
- match the static value `newsletter` to `utm_source`

 The resulting URL would like something like: `www.example.com/pagename.html?utm_campaign=$cname$$cmonth$$cday$&utm_source=newsletter` Furthermore, for a newsletter called *welcomecampaign*, sent on March 23<sup>rd</sup>, the value for `utm_campaign` in Google would be: `welcomecampaign0323`. ***Colorcoding still missing***

- - - - - -

Know Your Analytics Platform
----------------------------

 Different analytics platforms use different syntax to build up statistics on website activity, so it is important that you understand what options are available to you from your chosen platform. They typically use their own naming conventions for variables, and different syntax. For example, some platforms use "&" to separate variables, others use "." to separate them. Below is a selection of the variables available in **Google Analytics**.

<table class="wikitable"><thead><tr><th>Google Analytics Variable</th> <th>Description</th> </tr></thead><tbody><tr><td>`utm_campaign`</td> <td>keyword analysis to identify a specific promotion</td> </tr><tr><td>`utm_medium`</td> <td>identify mechanism/type of message</td> </tr><tr><td>`utm_source`</td> <td>identify a search engine, newsletter name or other source</td> </tr><tr><td>`utm_content`</td> <td>version of content, can be used for A/B testing</td> </tr><tr><td>`utm_term`</td> <td>key/search term used</td></tr></tbody></table> Different analytics packages also use different variables to describe the same data; below is an example of how the `campaign_ID` variable can vary from platform to platform.

<table class="wikitable"><thead><tr><th>Web Analytics Platform</th> <th>Campaign Variable Syntax</th> </tr></thead><tbody><tr><td>Coremetrics</td> <td>`cm_mmc`</td> </tr><tr><td>Google Analytics</td> <td>`utm_campaign`</td> </tr><tr><td>Omniture</td> <td>`id`</td> </tr><tr><td>Webtrends</td> <td>`mc_`</td> </tr><tr><td>Webtrekk</td> <td>`mid`</td></tr></tbody></table>### Mandatory variables

 To ensure that the analytics platform collects the data correctly you also need to know what the mandatory variables for that platform are. For example, `utm_source` and `utm_medium` variables are required in order for Google Analytics to work, but for Coremetrics you would only need `cm:` to capture data successfully.

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Omitting the mandatory variables will result in <span style="text-decoration: underline;">no</span> data being sent to the analytics platform.</td></tr></tbody></table>### A comparison of the different syntax used

 Below are some examples of how various analytics platforms would have their URL composed when capturing specific campaign data. To help illustrate this, each platform will aim to capture the same information so you can see the difference in the final URL. This information has been colour coded as follows:

<table class="wikitable"><thead><tr><th>Information</th> <th>Suite variables or fixed values</th> </tr></thead><tbody><tr><td><span style="color: #eb5a19;">campaign name/ID</span></td> <td><span style="color: #eb5a19;">`$cname$$cyear$cmonth$cday$`</span></td> </tr><tr><td><span style="color: #76923c;">source or origin of the click</span></td> <td><span style="color: #76923c;">`newsletter`</span></td> </tr><tr><td><span style="color: #193c96;">communication channel used</span></td> <td><span style="color: #193c96;">`email`</span></td> </tr><tr><td><span style="color: #948a54;">link name/URL used</span></td> <td><span style="color: #948a54;">`$clinkname$`</span></td></tr></tbody></table> Each platform generally uses different labelling and syntax to separate variables; for more in-depth information please consult the relevant documentation for that platform.

#### Google Analytics

 This is what a blank Google Analytics syntax would look like that you would use to capture the content: `www.example.com/pagename.html<span style="color: #eb5a19;">?utm_campaign=</span><span style="color: #76923c;">&utm_source=</span><span style="color: #193c96;">&utm_medium=</span><span style="color: #948a54;">&utm_term=</span>` The finalized code used in the URL would look like this: `www.example.com/pagename.html<span style="color: #eb5a19;">?utm_campaign=$cname$$cyear$cmonth$cday$</span><span style="color: #76923c;">&utm_source=newsletter</span><span style="color: #193c96;">&utm_medium=email</span><span style="color: #948a54;">&utm_term=$clinkname$</span>`

#### Coremetrics

 Coremetrics offers just one variable `cm_mmc` which can contain up to four parameters, each of which can be matched to a variable from Suite. This is therefore what a blank Coremetrics syntax would look like that you would use to capture the content: `www.example.com/pagename.html?cm_mmc=` Following the Coremetrics syntax where the parameters are separated by '`-_-`' the finalised code used in the URL would look like this: `www.example.com/pagename.html?cm_mmc=<span style="color: #eb5a19;">$cname$</span>-_-<span style="color: #76923c;">newsletter</span>-_-<span style="color: #193c96;">email</span>-_-<span style="color: #948a54;">$clinkname$</span>`

#### <span class="mw-headline" id="b3210c89be5c381ac38bf10deb806f9b">Webtrends<a name="bs-ue-jumpmark-2048a36985c94f6b5124c5f0ba69ab90"></a></span>

 This is what a blank Webtrends syntax would look like that you would use to capture the content (there is no Webtrends variable for the channel used): `www.example.com/pagename.html<span style="color: #eb5a19;">?WT.mc_n</span>=<span style="color: #76923c;">&WT.mc_t=</span><span style="color: #948a54;">&WT.ti=</span>` The finalized code used in the URL would look like this: `www.example.com/pagename.html<span style="color: #eb5a19;">?WT.mc_n=$cname$$cyear$cmonth$cday$</span><span style="color: #76923c;">&WT.mc_t=newsletter</span><span style="color: #948a54;">&WT.ti=$clinkname$</span>`

#### Webtrekk & Omniture

 Both of these analytics platforms use custom defined variables, so for this example there is no standard syntax example to showcase as both would involve a bespoke set up. For both of these products there would be an input parameter name and parameter value specified during setup that would then enable the analytics packages to work with Suite.

Important Data Privacy Note
---------------------------

 According to compliance regulations please note that Web Analytics Platforms handle your data outside of Suite which can lead to legal liability if the analytics platform is hosted outside of your country. You need to make sure that the servers where Web Analytics Platform is hosted are compliant with any national laws applying to your organisation as emarsys cannot, and will not, accept any liability for your actions if you use a platform with incompatible data protection and associated laws applying to data handling and security.

Appendix
--------

### The Suite Variables

 The Suite variables are mostly self-explanatory, with many of them allowing you to fine tune the time variables for campaigns, through to link information and category. To add flexibility there is the variable `$pers_N$` where `N` stands for the field ID from Suite. Below is a list of the standard variables available for use in Suite, although it is important to note that the `$pers_N$` variable is a generic custom designation and is what any manual variables would be based on. `N` can be swapped for any field ID in Suite to enable you to integrate your contacts database content with your web analytics platform.

<table class="wikitable"><thead><tr><th>Suite Variable</th> <th>Definition</th> </tr></thead><tbody><tr><td>`$cname$`</td> <td>campaign name</td> </tr><tr><td>`$ascii_cname$`</td> <td>campaign name (ASCII)</td> </tr><tr><td>`$cdate$`</td> <td>campaign date</td> </tr><tr><td>`$cyear$`</td> <td>campaign year</td> </tr><tr><td>`$cmonth$`</td> <td>campaign month</td> </tr><tr><td>`$cday$`</td> <td>campaign day</td> </tr><tr><td>`$chour$`</td> <td>campaign hour</td> </tr><tr><td>`$clinkcat$`</td> <td>link category</td> </tr><tr><td>`$clinkname$`</td> <td>link name</td> </tr><tr><td>`$clinktitle$`</td> <td>link title</td> </tr><tr><td>`$pers_N$`</td> <td>user’s element N</td> </tr><tr><td>`$campaign_category$`</td> <td>campaign category</td> </tr><tr><td>`$addcamptracking$`</td> <td>extra tracking variables that are enabled for you if you want to use individual tracking links for different campaigns.</td> </tr></tbody></table><table cellpadding="1" class="wikitable" style="width: 100%; border: 1px solid #fff;"><tbody><tr><td scope="col" style="text-align: left; vertical-align: middle; border: 1px solid #fff;" width="60px">[![](/assets/images/Icon_FurtherReading.png)](/assets/images/Icon_FurtherReading.png)</td> <td scope="col" style="border: 1px solid #fff;">See the document *Suite Field IDs and Values* for more information on the fields available for use as Suite variables.</td></tr></tbody></table>
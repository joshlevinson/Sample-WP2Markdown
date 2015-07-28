---
title: 'SuiteKit - the Audiences page'
tags: SuiteKit
old_url: 'http://emarsys.dev/suite/suitekit/suitekit-the-audiences-page/'
---

Audiences**Campaigns**
----------------------

 menu ->** Social Ads** -> **Audiences** Here you can see all the audiences you have created, with their current status and number of Facebook users. To create a new audience, click the button below the list. On this page you can:

1. [View, edit and delete audiences](#edit)
2. [Create a new blank audience](#new-blank)
3. [Create a new custom audience from an existing segment](#new-custom)
4. [Create a new lookalike audience](#new-lookalike)
5. [Filter your audiences further with Facebook's own data](#fb-data)
 
<a name="edit"></a>### 1. Viewing, editing and deleting audiences

 All the audiences that you have created in Suite are shown in the list, alongside any other custom audiences created by you in Facebook and linked to your Facebook Ads account. Along with their name and creation date, they are shown with the following information.

##### Source

This is what the audience is based on and can be one of:

- **Custom Audience** - either a blank audience or one based on an existing segment
- ** Lookalike: *source audience name*** - a lookalike audience sharing the characteristics of the custom audience it is based on
- **Tracking Pixel** - These are any kind of audience that have been created outside Suite using a pixel (e.g. to create an audience of all visitors to your website)

##### Status

This shows whether or not the audience can be used for Facebook Ads campaigns. Values include:

- **Too few people** - Facebook requires an audience to have at least 20 contacts before it will begin to bid for your Ads campaigns
- **Pending** - in the case of a Lookalike Audience, this means that Facebook has not yet finished creating it
- **Ready** - the audience can now be used for an Ads campaign
- **Unknown error** - in the rare case that this should happen, please contact Emarsys Support

##### FB matched contacts

This is the number of contacts that Facebook has identified (e.g. because their email addresses match those of the corresponding Suite contacts).

 To delete an audience, click the **X **icon next to it. <a name="new-blank"></a>

### 2. Creating a new blank audience

 To create blank audience, select the appropriate option for **Create New Audience** and proceed as follows:

1. Give the blank audience a suitable name

<div class="row">[![create-blank-audience](/assets/images/create-blank-audience.png)](/assets/images/create-blank-audience.png)</div>1. [Filter the audience further with Facebook's own data](#fb-data), if required (see below)
2. In the Automation Center, place the **Add to audience** node at the point where you want your contacts to join the audience. This could be after a recurring daily filter, or a concrete action such as an email response or a data change.

<div class="row">[![social-ads-nodes](/assets/images/social-ads-nodes.png)](/assets/images/social-ads-nodes.png)</div>1. Double-click the node to open the properties and select the blank audience you just created.

<div class="row">[![social-ac-select-audience](/assets/images/social-ac-select-audience.png)](/assets/images/social-ac-select-audience.png)</div>1. Place the **Remove from audience** node at the point where you want your contacts to leave the audience. This will typically be after a **Wait** node of a few days, or again after a concrete action by the customer such as a purchase.

 Once you activate the program, it will begin to add contacts to the audience according to your specifications, and as soon as Facebook has identified 20 user profiles from contacts it will begin to target these people with the [Social Ads campaign](/Suite/about-campaigns.md "Social Ads – About Campaigns") that you have launched to target this audience.<a name="new-custom"></a>

### 3. Creating a new custom audience from an existing segment

 To create a blank audience, select the appropriate option for **Create New Audience** and proceed as follows:

1. Select the Suite or Smart Insight segment that you want as the source.

<div class="row">[![create-custom-audience](/assets/images/create-custom-audience.png)](/assets/images/create-custom-audience.png)</div>1. Name the audience (the source segment is selected by default)
2. Decide whether you want to keep the audience synchronized with the source segment (this will happen every 15 minutes) or keep is static.
3. [Filter the audience further with Facebook's own data](#fb-data), if required (see below)

 Once you have saved your audience, it will be available for selection in the **Campaigns** page.<a name="new-lookalike"></a>

### 4. Creating a new lookalike audience

 To create lookalike audience, select the appropriate option for **Create New Audience** and proceed as follows:

1. Give the lookalike audience a name
2. Select the existing audience that you want to base the new one on
3. Select the country (this refers to the Facebook profile, not your contact properties) **Note:** Facebook will only create a lookalike audience based on a single country.  To target prospects in more than one country, you will have to create multiple lookalike audiences based on the same source audience.
4. Select the optimization settings Here you decide whether you want to spend your ads budget on fewer, but potentially more valuable, prospects (**Similarity**) , or simply cover a greater number (**Reach**).

<div class="row">[![create-lookalike-audience](/assets/images/create-lookalike-audience.png)](/assets/images/create-lookalike-audience.png)<a name="fb-data"></a></div>### 5. Filter your audiences further with Facebook's own data

 When you create a blank or a custom audience from a segment, you can also choose to filter this audience further using Facebook's own data. If you select this option, you can restrict the contacts that Facebook puts in the audience according to:

- **Location** - you can filter by **one of**: country, region or city. Within each option, multiple selection is possible.
- **Languages**
- **Gender**
- **Age**
- **Interests** - these are the interests that Facebook users have included in their profiles. You can drill down through the hierarchy of categories offered by Facebook, and next to each category is the total number of Facebook users worldwide who share that interest.

<div class="row">[![facebook-interests](/assets/images/facebook-interests.png)](/assets/images/facebook-interests.png)</div>
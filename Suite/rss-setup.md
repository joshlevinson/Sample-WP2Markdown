---
title: 'Setting up RSS Feeds'
subject: Suite
old_url: 'http://emarsys.dev/suite/content/rss-intro/rss-setup/'
---

Below you can find all the information you need to set up and activate RSS feeds to populate recurring emails campaigns with content. This section is aimed at technical support staff rather than Suite end users.

### How Does It Work?

 The RSS feature uses a Suite template-based recurring email and works by populating sections of that campaign with selected content. This is initially set up for you in conjunction with Emarsys Support. After deciding on the template which provides the framework for the look and feel of the content, you then specify how often and at what time the campaign should run. The RSS scheduler is configured to run the process automatically, pulling the content from the external source and sending it out at the intervals specified without the need for any further action.

<div class="center"><div class="floatnone">[![Visualization of RSS in Suite.png](/assets/images/Visualization_of_RSS_in_Suite.png)](/assets/images/Visualization_of_RSS_in_Suite.png)</div></div><div style="text-align: center;">**Visualization of RSS functionality in Suite**</div> This feature uses a parent/child email campaign relationship. The parent email is a template which defines how the content will be displayed and stores the email properties (language, reply mail address, etc.). It uses XSL to interpret the XML content of the RSS feed to create the output. The child email is created once the XML content has arrived via the RSS feed, and together with the launch list and schedule this becomes the actual email that is sent. A new child email campaign is created for every scheduled launch.

### Setting up RSS in Suite

 In order to get RSS set up there are a few simple steps to perform, after which the RSS campaign is ready to use and will run automatically until deactivated:

1. Contact Emarsys Support with an RSS template creation request, providing a screenshot of a current template - or a design proposal for a new template.
2. Provide them with the URL for the RSS feed you want to use and let us know if you would also like the subject line to be configured to auto-populate
3. Emarsys will then create the template for you in Suite, making sure that the format is correct and matches your requirements
4. Emarsys sets up the recurring URL for the defined groups (and subject line if desired)
5. You create the parent email campaign in Suite using the template with the RSS feeds, and specify the delay between child campaign creation and final launch
6. Emarsys configures the XSL definitions for you using the template and RSS information
7. Emarsys then defines the frequency and time for the email launch schedule, and runs a full test.

 Once the campaign has been tested and is ready to send, Emarsys will inform you that it is live.

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">- The delay time enables you to review your content before sending using a defined pre-fetch time limit. For example, you can create the child email one hour before the scheduled launch time, giving you the chance to review and edit the content if needed. This lead time can be particularly useful for customers who have websites with content that changes rapidly (e.g. a news website) and want to review the message before sending. The minimum delay is 5 minutes, our recommendation is at least 30 minutes.
- Should any changes be required to the parent email template after the RSS has been set up then you would need to contact Emarsys Support, who can advise further.
 
</td> </tr></tbody></table>[![Components_of_an_RSS_Campaign.png](/assets/images/Components_of_an_RSS_Campaign.png)](/assets/images/Components_of_an_RSS_Campaign.png "Components_of_an_RSS_Campaign.png")<div style="text-align: center;">**Illustrated components of a configured RSS campaign**</div>### RSS Code Example

 When an RSS-based email is created the underlying code of the message generated looks like the following example, once it has drawn on all the elements of the configured email campaign. [![RSS Code Example.png](/assets/images/RSS_Code_Example.png)](/assets/images/RSS_Code_Example.png)

<div style="text-align: center;">**Example of RSS code**</div>### Including Link Categories in the Content

 To enhance link reporting, you can assign names and categories to the links created in the RSS content. You can define any name you like, but the link categories must already exist in your Suite account (in the **Administration menu**, **Link Categories**). For each link included in your RSS, instead of having one link parameter to define the categories you will now need include three, for example:

#### XML:

- <http://www.yourURL.com/Interesting_Topic_URL:>
- <link_name:> (e.g. ***Daily fashion deal***)
- <link_category:> (e.g. ***Hero deal***)

#### XSL:

- <link><xsl:value-of select="link" /></link>
- <link_name><xsl:value-of select="link_name" /></link_name>
- <link_category><xsl:value-of select="link_category" /></link_category>

### Automating Subject Lines for RSS Campaigns

 Subject lines can be automated for RSS campaigns, but this requires configuration changes to be made before it will work.

1. Emarsys Support needs to arrange for configuration changes to enable the subject line automation
2. You need to edit the parent campaign as follows:
 
<dl><dd>- Make sure there is one section in the pre-header group that is empty
- Delete any existing subject line
- Enter the following as the new subject line: ***$#channel:title#$***

</dd></dl>Once you have completed these steps, the campaign should start automatically applying subject lines to your RSS-based campaigns.

### Using Tags

 Content is delivered by the RSS feed contained in a hierarchical structure using tags (in much the same way that HTML uses tags). Below you can see the available tags and the hierarchy in which they are used:


    <channel>
      <title>
      <link>
      <description>
      <language>
      <copyright>
      <managingEditor>
      <webmaster>
      <pubDate>
      <lastBuildDate>
      <rating>
      <docs>
      <fromname>
      <item> within this you can have:
         <link_name>
         <link_category>
         <title>
         <link>
         <description>
         <author>
         <category>
         <comments>
         <enclosure>
         <guid>
         <pubDate>
         <source>
         <image_url>
           <image> within this you can have:
           <title>
           <url> <b><span style="color: #ff6600;">*</span></b>
           <link>
           <width>
           <height>
           <textinput> within this you can have:
             <title>
             <description>
             <name>
             <link>


<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Content you put in the **<image>/<url>** tag will have the same effect as content you put directly in the **<image_url>** tag.</td></tr></tbody></table>### Technical Information at a Glance

<table border="1" cellpadding="0" cellspacing="0" class="wikitable" style="border: 1px solid #ebebeb;"><tbody><tr><td>Encoding</td> <td>UTF8</td> </tr><tr><td>Syndication</td> <td>RSS 2.0 or Atom 1.0</td> </tr><tr><td>Template from User</td> <td>CSS template or Screenshot</td> </tr><tr><td>Content</td> <td>Content only (no layout or formatting)</td> </tr><tr><td>Content Looping</td> <td>Enabled automatically</td></tr></tbody></table> For more information on how to work with RSS feeds in Suite, please see the [RSS User Guide](/Suite/rss-campaigns.md).
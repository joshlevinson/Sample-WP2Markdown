---
title: 'Suite CMS End-user Guide'
tags: Suite
old_url: 'http://emarsys.dev/ebene2-2/suite-cms-end-user-guide-2/'
---

Introduction
------------

 eMarketing Suite offers an advanced and intuitive content management system (CMS) which, when used in conjunction with email templates, offers a quick and reliable way to create complex and sophisticated email campaigns with little effort. The templates are built to customer specifications by the Emarsys Web Development team and can easily be filled with content, either manually or automatically via RSS feed, and launched. This document gives an overview of the functionality available in the Suite CMS and Email Campaign Manager. For more information on Suite templates, please speak to Emarsys Support. For information on creating emails using your own HTML code, please refer to the *Suite Online Help*. Learn more about the Suite CMS:

- [The E-Mail Campaign Manager](/Suite/campaign-manager.md)
- [Campaign Settings](/Suite/campaign-settings.md)
- [E-Mail Settings](/Suite/email-settings.md)
- [Creating Content](/Suite/section-editor.md)
- [Testing the E-Mail](/Suite/testing-emails.md)
- [Launching the E-Mail](/Suite/launching-emails.md)

The Suite Email Campaign Manager
--------------------------------

 Email campaigns are created in Suite using the Email Campaign Manager, which is accessed via the **Campaigns** menu. The **Overview** page lists all the email campaigns created in your account. The filter options above the list enable you to sort the list according to your specifications. You can also search for individual email campaigns using the **Search** function on the left of the screen. For more information on the information and controls on this page, please refer to the *Suite Online Help*.

### Creating an Email

 You can create a new email either using a blank template, or by copying an existing campaign.

- If you copy an existing campaign, you will copy everything from the content to the settings and scheduling options.
- If you create a new email from a blank template you will first be asked to choose the template.

 After creating the email, you enter the Suite content management system, which is comprised of the Toolbar, Section Editor and Live Preview pane.

<div class="center"><div class="floatnone">[![The Suite Campaign Editor](/assets/images/Suite_CMS_EUG_Page_04_Image_0002.png)](/assets/images/Suite_CMS_EUG_Page_04_Image_0002.png)</div></div>#### Toolbar (1)

 Here you save your work, and can find all the controls you need to configure the high-level settings of your email campaign, including testing utilities and scheduling.

#### Section Editor (2)

 Here you can see all the section groups in your email template, and is where you add and modify the actual content of your email.

#### Live Preview (3)

 This pane displays the content you add to your email and refreshes dynamically, helping you to visualize the final layout of the email as you work. The section that you select in the section editor is highlighted in the preview; you can also scroll up and down in the preview to select a section and this will then open in the section editor.

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">The Live Preview is a not a fully-generated email preview, and features such as personalization or conditional text will not be visible. You should always generate a full preview to check the final content of the email before sending; see below for details.</td></tr></tbody></table>#### Saving your work

 When you save your changes, Suite displays a validation message which lists all the settings which still need to be defined before the email campaign can be launched.

Campaign Settings
-----------------

 The campaign settings define the top-level characteristics of the email campaign, and are accessible via the **Settings** button.

### Language

 This setting defines the language used for any additional features, such as tell-a-friend or unsubscribe, as well as forms and database fields used for personalization.

### Template

 You can change the template of an email after creation. Suite will try to reassign all sections to an appropriate section group automatically, but if no such group exists in the new template you will have to open each unassigned section separately (they are located at the top of the section editor above the first group) and assign it to the correct group, otherwise the content will not be correctly displayed.

### Email category

 Assigning a category is helpful when you want to segment your contacts by their responses to similar campaigns (e.g. 'Holiday Specials'). It is also useful to assign a unique category to recurring emails for the same reason, since the behavior targeting filters will only check the most recent launch if an email is selected. By selecting a category instead, you can be sure to filter for all responses to all launches of a recurring campaign.

### Additional tracking parameters

 If you are using an external tracking tool, you can enter the parameters required by that tool in this field. They will then be appended to all the trackable links in this email campaign. For example, if you are using Google Analytics, you might enter: `utm_source=emarsys&utm_medium=email&utm_campaign=$ascii_cname$$cyear$$cmonth$$cday$+$chour$&utm_content=$clinkcat$$clinkname$_$clinktitle$`

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px solid #999;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">This field is only visible if you have asked Emarsys Support to enable it. You can also ask for these parameters to be defined on an account level, in which case they will be added automatically to every link in every email.</td> </tr></tbody></table><table cellpadding="1" class="wikitable" style="width: 100%; border: 1px solid #fff;"><tbody><tr><td scope="col" style="text-align: left; border: 1px solid #fff;" width="60px">[![Icon FurtherReading.png](/assets/images/Icon_FurtherReading.png)](/assets/images/Icon_FurtherReading.png)</td> <td scope="col" style="border: 1px solid #fff;">For more information please refer to the document *Suite Link Tracking for External Analytics*.</td></tr></tbody></table>### Recipient source

 Here you define how the email will be triggered and to whom it will be sent.

Email Settings
--------------

 In the Section Editor, you can define the preferences for the actual content of the email. If you are using the A/B testing feature, these settings will apply only to the open version. In this way you can test different subject lines, headers, etc.

### Sender Information

 The content you enter here is what your contacts will first see when they receive your email, and should be selected with care as it can have a major impact on deliverability. In particular the **From (email address)** is important, as most ISPs will not forward emails without a reply address.

<table cellpadding="1" class="wikitable" style="width: 100%; border: 1px solid #fff;"><tbody><tr><td scope="col" style="text-align: left; border: 1px solid #fff;" width="60px">[![Icon FurtherReading.png](/assets/images/Icon_FurtherReading.png)](/assets/images/Icon_FurtherReading.png)</td> <td scope="col" style="border: 1px solid #fff;">For more information on best practices for optimizing your email deliverability, please see the Deliverability Policy and Guidelines documentation in the Appendix of the *Suite Online Help*.</td></tr></tbody></table>### Additional features

 Here you can add the following features to your email:

- Change profile form
- Contact or Feedback form
- Social Network sharing
- Tell-a-friend form
- Unsubscribe link
- Table of contents

 The texts used for the subscribe and unsubscribe pages, as well as the design for the tell-a-friend form, can be defined in the **Forms, Settings** page.

Creating Content
----------------

 The Sections pane shows all the available section groups in your chosen template, and lists the groups in the order in which they would appear in the email. The order of these groups cannot be changed; however, the order of sections within a group can be changed by dragging and dropping the sections. The section list has the following controls:

<table border="0" class="wikitable"><tbody><tr><td>[![Suite CMS End-user Guide - English Page 07 Image 0002.png](/assets/images/Suite_CMS_End-user_Guide_-_English_Page_07_Image_0002.png)](/assets/images/Suite_CMS_End-user_Guide_-_English_Page_07_Image_0002.png)</td> <td>Add a section to the group.</td> </tr><tr><td>[![Suite CMS End-user Guide - English Page 07 Image 0003.png](/assets/images/Suite_CMS_End-user_Guide_-_English_Page_07_Image_0003.png)](/assets/images/Suite_CMS_End-user_Guide_-_English_Page_07_Image_0003.png) / [![Suite CMS End-user Guide - English Page 07 Image 0004.png](/assets/images/Suite_CMS_End-user_Guide_-_English_Page_07_Image_0004.png)](/assets/images/Suite_CMS_End-user_Guide_-_English_Page_07_Image_0004.png)</td> <td>If your template is enabled for Mobile Sense, these icons indicate whether or not this section will display on both mobile and desktop clients or will be hidden for mobile clients and display only on desktop.</td> </tr><tr><td>[![Suite CMS End-user Guide - English Page 07 Image 0007.png](/assets/images/Suite_CMS_End-user_Guide_-_English_Page_07_Image_0007.png)](/assets/images/Suite_CMS_End-user_Guide_-_English_Page_07_Image_0007.png)</td> <td>Copy the section.</td> </tr><tr><td>[![Suite CMS End-user Guide - English Page 07 Image 0008.png](/assets/images/Suite_CMS_End-user_Guide_-_English_Page_07_Image_0008.png)](/assets/images/Suite_CMS_End-user_Guide_-_English_Page_07_Image_0008.png)</td> <td>Delete the section.</td> </tr><tr><td>[![Suite CMS End-user Guide - English Page 07 Image 0009.png](/assets/images/Suite_CMS_End-user_Guide_-_English_Page_07_Image_0009.png)](/assets/images/Suite_CMS_End-user_Guide_-_English_Page_07_Image_0009.png)</td> <td>Click and hold this icon to drag a section within a group.</td></tr></tbody></table> To open a section for editing, click anywhere on the section title bar.

### The Section Editor

 Section content can be edited in two modes: Standard and Advanced. Standard Mode is a fast and efficient way of adding content, since the formatting and layout are taken care of by the template. If you want to deviate from the template design, you can switch to Advanced Mode and use the HTML editor to work directly in the HTML code.

#### Working in Standard Mode

 A section consists of four main elements: header, body text, image and link. Each one can be opened via the menu on the left.

- **Header & Body**These are plain text fields which have a toolbar with limited formatting options. You can also switch between WYSIWYG and the HTML source code.
 
<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">The HTML editor accepts only a limited set of HTML tags and will strip unsupported tags out when switching back to WYSIWYG mode. These tags should satisfy all but the most advanced editing requirements and a full list can be found in the *Suite Online Help*.</td></tr></tbody></table>- **Image** You can upload images from your Media Database or link to externally-hosted images by entering a URL. If your template is enabled for Mobile Sense, you can also define another image to display on mobile devices (otherwise the main image will be resized and displayed).
 
<table cellpadding="1" class="wikitable" style="width: 100%; border: 1px solid #fff;"><tbody><tr><td scope="col" style="text-align: left; border: 1px solid #fff;" width="60px">[![Icon FurtherReading.png](/assets/images/Icon_FurtherReading.png)](/assets/images/Icon_FurtherReading.png)</td> <td scope="col" style="border: 1px solid #fff;">For more information on Mobile Sense, please refer to the *Mobile Sense End-user Guide*.</td></tr></tbody></table>- **Links**Here you enter the link for the section, and define whether the section header and image are also linked.

 In addition to these elements, there are other features available in the section editor.

- **Registration form**Here you can add a link to a form in the section.
- **Advanced options**Here you can move the section to another group, and also switch to edit the section in Advanced Mode.
- Section targeting If you want the section to appear only to contacts in a particular segment, use this option. The option Enable this section for network sharing should be used when you want to control which content is shared on a network. If this is activated, only this section, and no other sections in the group, can be shared on a network. If section targeting is enabled, this icon will appear in the sections list:[![Suite CMS End-user Guide - English Page 08 Image 0003.png](/assets/images/Suite_CMS_End-user_Guide_-_English_Page_08_Image_0003.png)](/assets/images/Suite_CMS_End-user_Guide_-_English_Page_08_Image_0003.png)
- **Social networks**Here you enable a section to be shared and also select which network icons to add to the section.

Testing the Email
-----------------

 Before you launch your email campaign, you should test it to ensure that all the content is being displayed correctly. There are three testing utilities available:

- **Show Full Preview**Whereas the Live Preview shows the content of the email without any personalisation or conditional content, this generates a full version of the actual email that will be sent and uses the Suite dummy contact to populate some (though not all) of the personalization fields with values. The Full Preview also shows how the email will look in the text and mobile versions (when enabled).
- **Inbox Preview**Here you can see what your campaign will look like in the most popular email and webmail clients. In order to run a proper inbox preview test, the email must be ready to launch.
- **Send Testmail**You can send a testmail either to an email address that you enter manually, or to a Suite list or segment. If you enter the email address manually you will send an HTML and test version of the email, but without any personalisation. If you send a full campaign email to a list or segment, the email will be personalised for each recipient according to their contact properties.
 
<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">The A/B testing feature is described below in the **Launching the Email** section.</td></tr></tbody></table>Launching the Email
-------------------

 Once you have finished and tested your email you can proceed to the scheduling stage. Here you define when the email will be launched, how many recipients to send it to (full or part launch), as well as selecting the versions to send if you are using the A/B Testing feature. There are two scheduling modes in Suite: Simple and Advanced.

### Simple Scheduling

 If you are launching an ad-hoc email, which is not based on an event or part of an Automation Center program, and are not using any advanced features such as A/B Testing, Suite will automatically select the Simple Scheduling mode. This shows you the total number of contacts in the contact list or segment, as well as how many of them have no opt-in.

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">If you are sending to a segment, the figure here will only be accurate according to the last time the filter was run to create the segment. The filter will be run again immediately prior to launch and so the final launch list may not have the same total.If you have not yet run the filter, or changed some of the conditions since you last applied it, there will be no figures available. In this case an **Update** link will be available for you to refresh the segment.</td></tr></tbody></table> Simple Scheduling lets you launch an email campaign (or schedule one for launch) very quickly, because you do not need to generate the launch list first or check the personalization. If you do want to generate the launch list (and get a more representative total for your recipients), or see what percentage of recipients will see your personalizations, you can switch to Advanced Scheduling.

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px solid #999;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">Although you cannot check the personalization in Simple Scheduling mode, you can still define alternative text for the personalization variables in the Content Creation page.</td></tr></tbody></table>### Advanced Scheduling

 If your email has A/B versions or you are using personalization variables in the From (name) field (or if you are using certain other on-demand features), Suite will automatically select Advanced Scheduling for your campaign. In this mode you can see not only the recipients in your contact list or segment, and which of these have no opt-in, but also which are considered invalid, i.e. have previously been bounced. You can also generate the launch list again, which will refresh the recipient source. If your launch list is very large, this may take several minutes.

#### Launch type

 Select **Final mailing** to send the email to all recipients, or select **Send test email** to use the A/B Testing feature.

#### Select version to send

 If you are using the A/B Testing feature, here you define the percentage of the launch list for each version. The test versions you must select manually: the final version will be selected automatically based on the response criteria you choose.

#### Set schedule

 Here you select when the email campaign will be launched. If you schedule the campaign in the future, you can also define a specific time zone (e.g. the time zone of the target country). In this case, the launch takes place at the specified local time of that time zone, and this launch time is displayed with that time zone’s GMT offset. When scheduling a launch in the future, you can instruct the system to update the launch list (i.e. recipient source) before launching using the **Generate new launch list before launching email campaign** checkbox. This option is activated by default.

#### Send email

 When you have completed your preparations and are ready to launch the email, you need to check the personalization variables. The **Check Personalization** pop-up shows you how many recipients (as a %) have a value for each variable, and allows to you define alternative text for those without, as well as omit recipients without a value for this field from the email completely. Click the **Start Launch** button to finish, and your campaign is now done.
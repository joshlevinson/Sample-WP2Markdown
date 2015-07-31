---
title: 'Campaign Settings'
subject: Suite
old_url: 'http://emarsys.dev/old/suite/campaigns/campaign-settings-5/'
---

The campaign settings define the top-level characteristics of the email campaign, and are accessible via the **Settings** button.

### Language

 This setting defines the language used for any additional features, such as tell-a-friend or unsubscribe, as well as forms and database fields used for personalization. ### Template

 You can change the template of an email after creation. Suite will try to reassign all sections to an appropriate section group automatically, but if no such group exists in the new template you will have to open each unassigned section separately (they are located at the top of the section editor above the first group) and assign it to the correct group, otherwise the content will not be correctly displayed. ### Email category

 Assigning a category is helpful when you want to segment your contacts by their responses to similar campaigns (e.g. 'Holiday Specials'). It is also useful to assign a unique category to recurring emails for the same reason, since the behavior targeting filters will only check the most recent launch if an email is selected. By selecting a category instead, you can be sure to filter for all responses to all launches of a recurring campaign. ### Additional tracking parameters

 If you are using an external tracking tool, you can enter the parameters required by that tool in this field. They will then be appended to all the trackable links in this email campaign. For example, if you are using Google Analytics, you might enter: `utm_source=emarsys&utm_medium=email&utm_campaign=$ascii_cname$$cyear$$cmonth$$cday$+$chour$&utm_content=$clinkcat$$clinkname$_$clinktitle$` <table cellpadding="1" class="wikitable" style="width: 100%; border: 0px solid #999;"><tbody><tr><td scope="col" style="text-align: left; border: 1px solid #fff; vertical-align: top;" width="60px">![Icon AdditionalInfo.png](/assets/images/2014/04/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">This field is only visible if you have asked Emarsys Support to enable it. You can also ask for these parameters to be defined on an account level, in which case they will be added automatically to every link in every email.</td> </tr></tbody></table><table cellpadding="1" class="wikitable" style="width: 100%; border: 1px solid #fff;"><tbody><tr><td scope="col" style="text-align: left; border: 1px solid #fff; vertical-align: top;" width="60px">![Icon FurtherReading.png](/assets/images/2014/04/Icon_FurtherReading.png)</td> <td scope="col" style="border: 1px solid #fff;">For more information please refer to the document *Suite Link Tracking for External Analytics*.</td></tr></tbody></table>### Recipient source

 Here you define how the email will be triggered and to whom it will be sent.
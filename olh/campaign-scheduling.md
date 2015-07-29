---
title: 'Campaigns - Scheduling and Launching the Email'
subject: 'olh, SuiteCampaigns'
old_url: 'http://emarsys.dev/suite/online-help/campaign-scheduling/'
---

**Campaigns menu -> **Email Campaigns** ->** CMS** ->** Scheduling ** In the **Scheduling** pop-up, you manage the launches of your email campaigns.There are two interfaces available for this pop-up, which are displayed according to the nature of the email campaign you are sending.

<div> <table><tbody><tr><td>**Simple Scheduling**

 </td> <td>This is a fast and easy way to launch campaigns and is available if none of the advanced features are used (such as A/B Testing or personalization of the subject line).</td> </tr><tr><td>**Advanced Scheduling**

 </td> <td>This contains all the available functionality but takes longer to launch a campaign, since you must first generate the launch list and later check the personalization variables.</td></tr></tbody></table></div>#### Simple Scheduling

 When this feature is enabled, only the launch time and actual launch controls are available, meaning you can launch an email immediately. The **Launch Details** table will display the estimated launch list and look only for contacts with no opt-in. If you are sending to a segment, this table will show the number of contacts returned by that segment the last time it was refreshed. If the segment has since been modified and not refreshed, no figures will be displayed. You can refresh the segment manually via the **Update** link. If you want to take advantage of any of the features that have been removed, such as A/B testing or partial launches, you must switch back to **Advanced Scheduling**. Please note that once you have switched and used one of these features, you will not be able to switch back to **Simple Scheduling**. **Please note**: Even though the **Check Personalization** button is not available in Simple Scheduling, you can still define alternative text for personalization variables in the **Content Creation** page, via the **Alternative Text** button. However, you will not be able to see how many contacts have values for the fields you have chosen to use.

#### Advanced Scheduling

 The descriptions below refer to features available in Advanced Scheduling mode.

#### Generate/update launch list

 In the **Launch Details** section, click **Generate Launch List**. You can view the following information on your recipient source:

- **Original target** - Tells you how many contacts the recipient source contains.
- **Opt-in false** - Tells you how many of the contacts do not have an opt-in.
- **Invalid** - Tells you how many of the contacts have invalid email addresses.
- **Opt-in false and invalid** - Tells you how many contacts neither have opt-in nor a valid email address.
- **Excluded** - Tells you how many contacts have been removed from the launch list by the [Exclude on send](/olh/email-settings.md "Campaigns – Email Settings") feature.
- **Estimated** **recipients** - The total of contacts the email campaign will be sent to.

 Click the number for **Presumed** **Launch** to go to the appropriate list of contacts. Click the number of invalid email addresses to go to [Bounce Management](/olh/bounce-management-settings.md "Admin – Bounce Management Overview"), where the corresponding contacts are listed. Re-click **Generate** **Launch** **List** to have the system update the selected recipient source and create another launch list. The table to the right contains more information on the email campaign, such as the launch type, starting time, planned mailing volume and mail format.

#### Define launch type

 In the **Launch** **type** section, you can either launch the final email campaign or start a test run. By using the testmail function you can check how your emails will affect a definable amount of recipients. This way you can still make changes before the email is sent to all recipients. Emarsys eMarketing Suite memorizes the addresses of the recipients the test mail has been sent to and will not send twice to the same contact.

#### Launch versions

 If you have created versions, you can select one from **Select version to send** and send it to all or a percentage of the launch list. As soon as you have sent at least two versions as test launches (to a percentage of your launch list) you can have Emarsys eMarketing Suite decide which version should be sent to the rest of your launch list. Choose between the following options: Send the version with:

- the best mail open rate
- the best unique click rate (i.e. all clicks by one person are counted once) or
- the best total click rate (i.e. all clicks by one person are counted individually)

 If the [Ecommerce tracking](/Suite/ecommerce-tracking.md "Ecommerce Tracking") feature has been activated for your account, you are presented with two more options. You can select either the version that turned out to have the best paragraph (i.e. the most units sold) or the best turnover. This way you do not have to check the email analysis every time you have made a test launch. **Please note**: A minimum time period must have passed between the last test launch and the final email campaign launch. This can be defined per account; the default is one hour.

#### Set schedule

 You can define at which time to launch the email campaign, either immediately or on a certain day at a particular time. **Note**: If you try to schedule a launch for a date/time in the past, you are notified and prompted to enter a date/time in the future. You can also assign a specific time zone (e.g. the time zone of the target country). In this case, the launch takes place at the specified local time of that time zone, and this launch time is displayed with that time zone’s GMT offset. When scheduling a launch in the future, you can instruct the system to update the launch list (i.e. recipient source) before launching. This option is activated by default. **Please note**: If you schedule an email to launch over more than one day, be careful if you are using the [Frequency Cap](/olh/frequency-cap.md "Admin – Frequency Cap Overview"), since all the contacts on the launch list will be counted as having received the email on every day that a launch takes place.

#### Check personalization

 In the **Send Email** section, click **Check personalization** to review the availability of the personalization variables used in the email campaign (such as: title, first name, last name). The system checks whether the contacts in the selected recipient source have the corresponding entries in their individual profiles. The results are presented in the **Check personalization** window. If the availability of a variable is below 100%, you can decide to insert an alternative or to exclude all recipients who do not have a corresponding entry; for the latter, activate **Omit recipients**.

#### Launch email

 To send your email campaign as defined, click **Launch email**. **Please note**: We strongly recommend running through the steps above before launching.

#### Pause and resume launches

 While an email campaign is being launched (i.e. some emails have already left the servers), you can stop the launch by clicking **Pause**. To continue sending, click **Resume**.

#### Unscheduling planned launches

 Even after you have scheduled a launch and clicked **Launch Email**, you can still change your mind; for this, go back to the Launch Details section on top of the page and click **Unschedule**. **Please note**: This applies to future launches; email campaigns which are in the middle of being launched cannot be rescheduled.

#### Schedule event-driven emails

 Event-driven emails do not have a recipient source as such; the launch takes place if/only after the event has occurred. To schedule such an email, make the following settings:

- Activate **Exactly on event** if the email is to be launched as soon as an event has taken place (e.g. as soon as someone has registered for your newsletter). With this option activated, you can either have the email launched only once (on the specified date), or set it to be launched repeatedly (same date every year).
- If you want the email to be launched a few days earlier or later, make the corresponding settings below.

 For emails of the type on **abandon shopping cart**, you can schedule the launch a number of hours after the cart has been abandoned, or at a fixed time a couple of days later. **Please note**: Since these emails are to be sent at some time in the future, no availability values exist. However, you can still enter an alternative text, in case the values for the personal variables are missing. Click **Activate Email**. This has the program wait for someone to trigger the event, and then send the mail according to your settings. To stop the launch, click **Deactivate**; the email will no longer be sent.

**
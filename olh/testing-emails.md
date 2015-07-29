---
title: 'Campaigns - Testing the Email'
subject: 'olh, SuiteCampaigns'
old_url: 'http://emarsys.dev/suite/online-help/testing-emails/'
---

**Campaigns menu -> **Email Campaigns** ->** CMS** Once you have created the content you can now start to do some testing to ensure that it will be displayed as intended, and finally schedule the campaign once it is ready. Suite offers the following testing utilities:

#### A/B Split Testing

 You can test the content, layout or subject line of your emails by creating different versions and sending them to small percentages of the launch list. You can then decide for yourself which version is the more effective, or schedule the final launch to pick a version automatically, based on the best click rate, open rate or other eCommerce conversion criteria. When you create a version the original email is always the master version; this cannot be deleted. There is no limit to the number of versions you can create but you cannot send tests to more than 90% of the launch list.

- If you are using template-based emails, the version number is displayed next to the campaign name at the top. You can create, edit and delete versions by clicking the Version icon on the toolbar.
- If you are using your own HTML code, click the plus sign icon in the top right corner to activate the A/B testing feature.
 
**Please note**: This feature is not available for on-event and recurring emails. To test these mails you should use the A/B Splitter node in the [Automation Center](/olh/ac-overview.md "Campaigns – Automation Center – Overview").

#### Full Email Preview

 Since the email preview in the content editor is a live preview, it is a generated locally. This means it has no access to the contact database. Therefore dynamic content such as personalization variables or conditional text will not display, and some template elements may also be incompletely rendered. In order to see how the final email will really, look, it is necessary to generate a full preview. Here you can see the HTML, text and mobile versions of the final result.

#### Inbox Preview

 On this page, you can test an email campaign to see how it will be displayed in the inboxes of the most popular email and webmail clients. If tests have already been run for an email campaign, the thumbnails of the most recent test are displayed. You can display the thumbnails from previous tests by selecting the test in the drop-down box. If no test has been run, you see a series of dummy thumbnails. For more details, see: [Inbox Preview](/olh/inbox-preview.md "Campaigns – Inbox Preview").

#### Send Testmail

 Prior to launching an email campaign, we recommend sending a test email. These test emails are not recorded as part of the launch and no contact responses (opens, clicks etc.) are displayed in the [Email Analysis](/olh/analysis-emails-overview.md "Analysis – Emails – Overview"). Scheduling, launch list or A/B version tests are not affected by test emails. To send a testmail, proceed as follows:

1. Select a **Mail** **type** using the dropdown, choosing from:

- **Full** **Campaign** **Email** - this must be sent to an existing Suite contact list or segment and shows full personalization and conditional text (including section targeting).
- **Text and HTML Emails** - this will send one copy of each type of email to an address that you must enter manually. There will be no personalization of content.

1. Enter a **Subject** **line**.
2. Choose the **Recipient** **source** using the dropdown.
3. Click **Send** to send the test.
 
**Please note**: A test email cannot be sent to more than 50 recipients, so if the selected contact list or segment contains more than 50 recipients, the test email is sent only to the first 50.

**
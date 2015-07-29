---
title: 'Analysis - Results Summary'
subject: 'olh, SuiteFeatures'
old_url: 'http://emarsys.dev/suite/online-help/analysis-results-summary/'
---

**Analysis menu ->** Emails** ->** Results Summary** Here you can get a detailed breakdown of how the email campaign is performing with the Open Rate and Click Rate shown as a bar chart. The Click Rate is split into two colors to highlight unique vs. repeated clicks. This screen gives a complete overview of delivered messages, rejections, click origin and format.

#### Emails Planned

 This section indicates the total number of emails that were set to leave Emarsys eMarketing Suite as part of the email campaign but could not be sent. There are various possible reasons for this:

- **No content available for these recipients** - the contacts in the selected Recipient Source do not fit any of the filters of the individualization of a section.
- **Email address empty** - no email address entered
- **Blocked by program** - recipients who do not want mail and signed up to the Robinson List will have their details imported daily to an internal blacklist to ensure they do not get content. This also applies to specific addresses like abuse@... or spamcop@... that are known to be blacklisted by recipient organizations, which is a system-wide policy.
- **Blocked by Internal Blacklist** - manual list of contacts that do not want to receive further content and is controlled by you. All entries added here will only apply to your account.
- **Other** - An email address with umlauts or syntax errors (e.g. john@domain.co.m instead of john@domain.com)

#### Emails Sent

 This is the total number of messages that went to the mail server after the **Emails Planned** section removed any erroneous messages, and lists any messages that were not successfully delivered. Emarsys eMarketing Suite is able to categorize why a message was not delivered under the **Bounces** section where you can click on each type to find out why the message could not be delivered.

#### Emails Delivered

 This section breaks down the message delivery into different categories where you can see if messages are opened, and allows you to track clicks where clickable links have been accessed.

- **Opens** - this only applies to HTML formatted email messages, and is the total number of emails opened by the recipients.
- **No Opening Indication** - No information on the message which can be due to either: - message has not been opened yet
- email client set to disable images
- email client cannot display images
- email could have been bounced
- **Unique Clicks** - breakdown of how many individual contacts use the link (one click per contact counted)
- **Total Clicks** - total clicks for when a contact clicks the link more than once
- **Not Clicked** - Total of messages that have not been tracked because the contact hasn't clicked a trackable link, there are no trackable links, or the message has been bounced. This total includes the** No Opening Indication value**.

#### Social Networks

 Summary of Social Network activities on here, for more detail click on the [Social Network Tracking](/olh/analysis-social-network-tracking.md "Analysis – Social Network Tracking") section.

#### Email Formats

 Breakdown of what format was used for the content sent, using either HTML, text or both which is based on the individual profile of the contact and what they entered in the **Preferred Mail Format** field. Both only applies to contacts that selected auto detect and they get content in multipart emails which means it's a mix of both text and HTML.

#### Additional Activity

 Breakdown of how many recipients actually performed the action e.g. click a save button in a profile change, or used the unsubscribe feature. These clicks are graphed on the [Individual Link Tracking](/olh/analysis-individual-link-tracking.md "Analysis – Individual Link Tracking") page.

**
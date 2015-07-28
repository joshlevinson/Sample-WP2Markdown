---
title: 'Admin - Frequency Cap Overview'
tags: 'olh, SuiteAdmin'
old_url: 'http://emarsys.dev/suite/online-help/frequency-cap/'
---

**Admin menu ->** Frequency Cap** The frequency cap is the maximum number of emails that a contact can receive within the specified time period. if this limit is reached, the contact will receive no more emails and will be displayed in [Email Analysis - Overview](/olh/analysis-emails-overview.md "Analysis â&#128;&#147; Emails â&#128;&#147; Overview") as **Excluded by frequency cap**. When the frequency cap is activated, all emails will check their launch lists for contacts who have reached their limit and remove them. Event-triggered (transactional) emails do not add to the frequency count of contacts. That is, contacts can receive these emails without affecting their ability to receive other mails. All other emails, including on-import emails, will increase the frequency count by one each time. On the **Frequency Cap Overview** page, you make the following general settings:

#### Deactivate frequency cap for your account

 By default, the frequency cap is activated. To deactivate the feature for your account, remove the tick for **Activate frequency cap**. **Note**: For individual emails, you can deactivate the via the setting **Ignore frequency cap** on the [Email Settings](/olh/email-settings.md "Campaigns â&#128;&#147; Email Settings") page.

#### Set frequency cap threshold value

 You can define how many emails recipients may receive within a certain time period. The time period you can also specify. **Attention**: The frequency cap works by checking the launch lists of email campaigns each day. It does not differentiate between A/B testing versions, nor does it recognize when an email is sent over two days. This means that if an email campaign launch is spread over more than one day, either due to versions being so scheduled or due to it being launched close to midnight, the frequency cap will think that each contact in the launch list received the campaign each day. This can lead to contacts reaching their maximum limit erroneously.

**
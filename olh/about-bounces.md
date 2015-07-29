---
title: 'Admin - About Bounces'
subject: 'olh, SuiteAdmin'
old_url: 'http://emarsys.dev/suite/online-help/about-bounces/'
---

Bounces are emails which indicate that a campaign could not be delivered to certain contacts.

#### <span class="f_Subheading1">Bounce types</span>

 There are three types of bounces:

- **Soft Bounces**

Emails could not be delivered because of temporary problems, such as:

- the mail box of the recipient is full
- the denoted domain cannot be reached temporarily or the host is unknown


Reasons for soft bounces can be mistyped addresses as well as temporary server breakdowns.

- **Hard Bounces**

Emails could not be delivered because of permanent problems, the common reason being a non-existing email address ("contact unknown").

- **Block Bounces**

Emails could not be delivered because they were blocked by spam filters. Reasons for this could be:

- A content with suspicious words; emails that contain bawdy words (in the text body or the subject or sender field) are usually rejected.
- The HTML format in the sent email differs significantly from the HTML standard.
- A recipient activated a spam filter and has put the sender on its personal spam list.
- The sender is blacklisted, which means that the contact has informed their internet provider that they consider the email received to be spam.
- Emails are rejected by the recipient's server firewall (especially company servers).


#### Status

 Email addresses are either active or inactive. After an email address produced a certain number of bounces, the system assigns the status inactive and no further emails are sent to the address as long as it is not changed. The threshold value for soft bounces can be defined on the [Settings ](/olh/bounce-management-settings.md "Admin – Bounce Management – General Settings")tab. In the Bounce list, Inactive email addresses are marked with an **X**, while those addresses which have been bounced, but not yet deactivated, are marked with a **?**.
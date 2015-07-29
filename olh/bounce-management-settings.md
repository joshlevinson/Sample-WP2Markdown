---
title: 'Admin - Bounce Management - General Settings'
subject: 'olh, SuiteAdmin'
old_url: 'http://emarsys.dev/suite/online-help/bounce-management-settings/'
---

**Admin** ->** Bounce Management** ->** General Settings**#### Soft Bounces

 On the **General Settings** page, you define the threshold value which determines after how many soft bounces an email address is to be set to invalid. The following rules apply: - If an email was sent successfully to an email address which had produced bounces before, the counter is set back to zero.
- Email addresses which were inactive before you increased the counter (e.g. from "after two" to "after three"), remain inactive.
- If you have adjusted the counter the other way round (e.g. from "after three" to "after two"), email addresses which were bounced twice in a row are marked as invalid. For our example, email addresses which had been bounced twice in a row before the counter was lowered become invalid immediately after the change.

#### **Reset Soft Bounces**

 If an email address is flagged as invalid because it has reached the limit for soft bounces, you can override this by resetting the bounce status after a defined delay using the drop-down menu. **Important**: This can have a significant effect on your Deliverability and reputation, and is been limited to twice per email address. After this, the status will permanently be set to invalid. Click **Save** to store your settings.
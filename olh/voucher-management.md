---
title: 'Admin - Voucher Management Overview'
tags: 'olh, SuiteAdmin'
old_url: 'http://emarsys.dev/suite/online-help/voucher-management/'
---

**Admin menu ->** Voucher Management Overview** Via Voucher Management, you can attach vouchers to your emails. For that you must use a voucher pool, which is a list of randomly created codes. You can create such a list yourself (e.g. as a column in MS Excel), or you can have Emarsys create them for you. The lists must have the TXT or CSV format. You can create as many voucher pools as you like.

#### Using voucher codes in emails

 To include vouchers in an email, you must use the **Personalize** function when [creating the content](/Uncategorized/content.md "Creating and Editing Content") of the email; this inserts the field (i.e. the voucher pool name) via **Section Editor**. In the actual email, the placeholder for the voucher pool name is replaced with a voucher code taken from the code pool. The **Overview** page lists all existing voucher pools with their names. For each pool, you can see how many voucher codes are left.

#### Create pools

1. To create a new pool, click **Add** **New** **Pool**.
2. Enter a name for the pool.
3. In the **Voucher** **Pool** **Settings** dialog box, browse for a code list and click **Upload**.
4. For reminders, you can specify the following:

- To have a reminder sent when the number of codes in the pool has gone down to the specified value.
- An email address to which the reminder is to be sent.
- A default text for the reminder.

1. Click **Save**; the new pool is added to the list on the **Overview** page.

#### Edit pools

 To modify a pool, click [![edit-icon](/assets/images/edit-icon.png)](/assets/images/edit-icon.png). This opens the **Voucher Pool Settings** dialog box (see Create pools above), where you can make your changes.

**
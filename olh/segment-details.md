---
title: 'Contacts - Segments - Segment Details'
subject: 'olh, SuiteContacts'
old_url: 'http://emarsys.dev/suite/online-help/segment-details/'
---

**Contacts menu ->** Segments** ->** Details** On the **Segment Details** page you define the filter conditions of a segment and apply filters.

#### Define segments

1. When you create a segment, the system automatically assigns a **Name**, which you can keep or change. Names must be unique in the system.
2. You can add a **Description**.
3. Specify a **Source**; this can be all contacts in the system, a specific contact list or segment.
4. Proceed with defining the filter conditions:

- Expand the **Contact Criteria **section to define conditions based on contact properties.
- Expand the **Behavior Criteria** section to define conditions based on contact behavior.
- If you are a Smart Insight customer, you can also define conditions based on customer lifecycle activities.


1. If required, define **Advanced Filter Options**.
2. Click **Save**.

#### Define source list for filtering

 You can decide to run a filter on all contacts in the database, on an existing Suite contact list, or on a segment. If you decide on a segment, it is refreshed dynamically when the filter is re-run. If you decide on a contact list, the filter remains static. Go to **Contact Criteria** and click [![ico_plus](/assets/images/ico_plus.jpg)](/assets/images/ico_plus.jpg) to expand the section. From the drop-down box on the left select the field (custom or system) on which the filter is based. In the middle box you select the filter operator, and on the right you select the value. Which operators are available, depends on the field, as does the value (e.g. single selection or text field). This is an example for a filter based on contact criteria: Field = Salutation', 'Operator = Equal' and 'Value = Mr.'

#### Use behavior criteria

 Behavior targeting allows you to define filter conditions according to contact behavior. You can, for example, filter your database for contacts that have received more than three email campaigns in the last month, but have not made any clicks; or you can view which clicks in which categories were made most frequently. Go to **Behavior Criteria** and click [![ico_plus](/assets/images/ico_plus.jpg)](/assets/images/ico_plus.jpg) to expand the section. You can define filter conditions based on the following behavior criteria:

- Emails sent or not
- Emails received or not
- Received emails opened or not
- Links in opened emails clicked or not
- Links in link categories clicked or not

 Depending on the criteria you choose, you can further refine your filter

- by selecting the email (all, single or category)
- by defining a time frame
- by defining the number of actions (volume restriction)
 
**Attention**: The contact behavior here depends on the notifications returned by the target email client. This may not always exactly reflect the behavior of the recipient. Therefore the following points should be considered when filtering for contact behavior:

- An email which is opened without images does not return an open indication.
- Emails which are read in the mail client preview window do also not return an open indication, unless the client is set to display images.
- A contact may click a link several times to open it. Depending on the click speed and browser settings, each click could be counted separately even though the link was opened only once.

 The filters are defined in the same way as for the contact criteria, and multiple conditions are by default linked with an AND operator; you can modify this via the **Advanced Filter Options**.

#### Use Smart insight criteria

 If you are using the Emarsys customer intelligence module, Smart Insight, you can also add filter criteria based on ERFM activity and web behavior.

#### Combine filter conditions

 You can define more than one condition for a filter. Click [![ico_plus](/assets/images/ico_plus.jpg)](/assets/images/ico_plus.jpg) to display another set of conditions/operators. In standard mode, all conditions are grouped with an AND operator, that is, contacts must satisfy all filter conditions to be included in the result. If you want to define a more complex filter, for example with nested conditions, click **Advanced** **Filter** **Options**. To remove a filter condition, click [![ico_minus](/assets/images/ico_minus.jpg)](/assets/images/ico_minus.jpg) to its right.

#### Apply advanced filter options

 If you click **Advanced Filter Options**, all filter conditions are automatically grouped together with an** AND/OR** operator. You can create groups within groups (nested conditions) by clicking [![ico_plus](/assets/images/ico_plus.jpg)](/assets/images/ico_plus.jpg) to the right of the filter condition. Here you can also define an **EITHER/OR** filter, that is, where a contact must satisfy only one of the filter conditions in order to be included in the result.

#### Apply filter and view results

 Once you have defined your filter click **Apply Filter** to run it. Note that applying the filter will automatically save it. In the **Filter Results** section you see the following:

- **Last applied** - The last time the filter was run.
- **Duration** - The time it took to run the filter.
- **Total contacts in the database.**
- **Total contacts** - The number of contacts who fulfil the filter criteria.
- **Contacts with opt-in** - The number of contacts with opt-in status, i.e. ready to receive an email campaign.

 Click **Display Contacts** to show all contacts who have been returned by the filter. You can save this result as [contact list](/olh/contact-lists-overview.md "Contacts – Contact Lists – Overview"). Note that contacts with no opt-in are also included in the displayed list.

**
---
title: 'Contacts - Data Export - Data Changes'
tags: 'olh, SuiteContacts'
old_url: 'http://emarsys.dev/suite/online-help/export-data-changes/'
---

**Contacts menu ->** Data Export** ->** Data Changes** Contact data changes performed in Emarsys eMarketing Suite (via registrations forms, contact profiles and duplication handling) are recorded and can be exported. This way, you can synchronize Emarsys eMarketing Suite with another database. **Attention**: Data changes which result from an import are not exported. This was implemented to prevent configurations from using both automatic import and automatic export of data changes result in an endless loop in which data is constantly overwritten. On the **Data Changes** page, you make settings for the export of data changes and schedule an automatic export.

#### Define settings for a manual export of data changes

 On the **Manual Export** tab, you define the following:

1. In the **Export includes** section you specify if you want to export changes to all contacts in the database or those applied to a segment; you can also specify a single contact list.
2. Specify a source, i.e. how/where the changes were made.
3. For **Additional options**, decide to export changes to existing contacts, new registrations or both.
4. Set a time range; only changes which occurred within the range are exported.

 For the other settings on this page, see: [Define settings for a manual export of contact lists](/olh/export-contact-list.md "Contacts â&#128;&#147; Data Export â&#128;&#147; Contact List").

#### Schedule automatic export of data changes

 On the **Export Scheduler** tab, you define settings for the automatic export. For this, you must use a so-called export rule. Existing export rules can be edited, deleted, activated and deactivated. To create a new export rule, click **New Rule**; the **Edit Rule** page opens. Here you define the following settings:

1. **Name of Schedule** - assign a name to the rule.
2. **Export includes** - decide if you want to export all contacts in the database, a specific segment or a contact list.
3. **Schedule** - decide if you want to export on a monthly, weekly or daily basis, and define an export time. Set a date for **Next export on**; the intervals for the automatic export are calculated from that day onwards.
4. For the other settings, see the manual export above.
5. Click **Save**; the export will be performed as scheduled.

**
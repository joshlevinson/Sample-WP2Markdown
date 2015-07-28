---
title: 'Contacts - Data Export - Contact List'
tags: 'olh, SuiteContacts'
old_url: 'http://emarsys.dev/suite/online-help/export-contact-list/'
---

**Contacts menu ->** Data Export** ->** Contact List** On the **Contact list** page, you make settings for the export of contact lists, export lists and schedule an automatic export.

#### Define settings for a manual export of contact lists

 On the **Manual Export** tab, you define the following:

1. In the **Export includes** section you specify if you want to export all contacts in the database, a specific segment or a contact list.
2. In the section below, you specify by which channel you want to export:

- For **Email**, you must enter a valid email address; you can specify a subject line or use the default entry. **Note**: The download link which is sent via email is password-protected; for the download you must enter your Emarsys eMarketing Suite user credentials.
- For **FTP**, you must enter the corresponding access data (i.e. a host address, user name and password; the directory is optional).
- For **Local Delivery**, the content is exported to a WebDAV folder that was configured during your account setup, and requires no further action by you. **Note**: This feature is manually configured during setup and will not be visible by default.


1. Select a **Display Language**; this language is used for the field names (e.g. first name, last name).
2. Select a **Field Separator**.

**Note**: The German and English versions of programs like Microsoft Excel might use different characters for separating fields in .CSV files. With this option, you can adapt the .CSV export to suit the version you use.

1. The **Add field names to the first row of export file** option is activated by default. It writes the field names to the top row of the exported file.
2. Now you select the fields you want to export in the left box. You can select more than one field by pressing the CTRL key on your keyboard and selecting fields with the mouse. Move your selection to the right box by clicking [![r-arrows](/assets/images/r-arrows.png)](/assets/images/r-arrows.png). You can remove an entry by clicking [![l-arrows](/assets/images/l-arrows.png)](/assets/images/l-arrows.png).
3. If you have made all required settings, click **Export Now**.

 During the export, the system assigns an internal ID to each record. In fact, this ID has been generated at the time a record was created (via online registration, manual entry or import). It remains invisible until an export is started. The internal ID is unique and will later on allow you to re-import the same file to Emarsys eMarketing Suite. Example: You exported a list with invalid email addresses and corrected them in Microsoft Excel. In order to re-import the records, you only need to provide the internal IDs and the updated email addresses. Emarsys eMarketing Suite will update the records in the database accordingly.

#### Schedule automatic export

 On the **Export Scheduler** tab, you define settings for the automatic export. For this, you must use a so-called export rule. Existing export rules can be edited, deleted, activated and deactivated. To create a new export rule, click **New Rule**; the **Edit Rule** page opens. Here you define the following settings:

1. **Name of Schedule** - assign a name to the rule.
2. **Export includes** - decide if you want to export all contacts in the database, a specific segment or a contact list.
3. **Schedule** - decide if you want to export on a monthly, weekly or daily basis, and define an export time. Set a date for **Next export on**; the intervals for the automatic export are calculated from that day onwards.
4. For the other settings, see **Define settings for manual export** above.
5. Click **Save**; the export will be performed as scheduled.

**
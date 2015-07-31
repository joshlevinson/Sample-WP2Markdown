---
title: 'Manually Importing Contacts'
subject: SuiteContacts
old_url: 'http://emarsys.dev/old/suite/contacts/manual-import/'
---

The Data Import Page**Contacts**
================================

 menu ->** Data Import ** Data imports are an easy way to add contacts to your Suite database. You can import new contacts, as well as update the data fields of existing contacts. Before you start with an import, you might want to read the following:

- [Auto-imports](/SuiteContacts/auto-imports.md "Auto-Imports")
- [Data Import FAQ](/SuiteContacts/import-faq.md "Data Import FAQ")
- [CSV guidelines](/DataManagement%20@zh-hans/csv-files.md "CSV Guidelines")

 On this page you can:

1. [View the status of currently active imports](#current-imports)1. [Check the settings of active imports](#check-settings)
2. [Abort an import that is already running or queued for processing](#abort-import)
2. [Manually import a file](#manual-import)
3. [View the history of past imports](#import-history)1. [Open the contact list, if one was created](#check-list)
2. [Check the import settings](#check-settings2)

### <a name="current-imports"></a>

### 1. Current Import Status

 This table shows you which imports are currently running, or scheduled to run soon.

<table border="0" cellpadding="1" class="wikitable" style="width: 100%;border-width: 0px;border-style: solid"><thead><tr><th style="text-align: left;border-color: #fff;background-color: #fff;color: #eb5a19">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left;border-color: #fff;background-color: #fff;color: #555555">In order to ensure that duplication handling is managed consistently, only one import can run at a time. Imports are queued and processed on a first come, first served basis.</td></tr></tbody></table> The table displays the total number of contacts in the import file, as well as how many of these are new and how many already exist in your database. depending on your duplication handling settings, it will also show you how many imported contacts have been merged with existing ones and how many have been flagged as potential duplicates, but which require further processing in the **Duplication Handling** page. You can also see an estimation of the remaining time, and the contact list created by the import. <a name="check-settings"></a>

##### Import settings

 Click the **?** icon in the table to see the settings for that import <a name="abort-import"></a>

##### Aborting an import

 To cancel a running import, click the **X** icon in the table. This will stop the import immediately, but all data imported up to that point, either new contacts or changes to existing contact data fields, will remain in the database. <a name="manual-import"></a>

### 2. Manually Importing Contacts

 To start a manual import, proceed as follows:

1. Click **Import** to open the import wizard.
2. On the **Upload Files** page, select the .CSV file you want to import. You will now see the column names and the first few entries of the import file.


<div class="row">[![manual-import-1](/assets/images/2015/02/manual-import-1.png)](/assets/images/2015/02/manual-import-1.png)</div>1. In the **Settings**, select: 1. The **Unique Identifier** field which will be used for duplication handling
2. The **Opt-in** status of the contacts in the file (all with opt-in, all without opt-in, or the opt-in status is contained in a field in the import file)
3. The **Language** of the contacts to be imported (if required for segmentation)
2. Show the **Advanced Settings** if you want to: 1. Change the field delimiter
2. Change the text delimiter
3. Change the language of the file (this will affect how Suite recognizes the field names in the import file and matches them to fields in the database)
4. Change the date format used in the file
3. In the **Field Matching** section, make sure that the field name in the drop-down matched the field that you are importing.
4. Click **Do not import** to omit any fields from this import.
5. When you are satisfied that the import settings are correct and the fields matched, click **Next Step**.
6. On the **Match Values** page, you must map a value for each of the multiple- and single-choice fields in the import file. When you are finished, click **Next Step**.
7. If you want to save the imported contacts as a contact list, you can enter a name for this list on the final page of the wizard. If you do not want to save the imported contacts as a list, leave this field empty.
8. Click **Start Import** to close the wizard and start (or queue) the import.
 
<a name="import-history"></a>### 3. Import History

 This table shows you all the imports ever made for your account, along with the date and time of the import, the number of contacts imported, merged and flagged as potential duplicates, the status and the contact list, if relevant. You can also:

- <a name="check-list"></a>Click the [![](/assets/images/2015/02/view_details_icon.png)](/assets/images/2015/02/view_details_icon.png) icon to open the contact list
- <a name="check-settings2"></a>Click the **?** icon to check the setting for that import
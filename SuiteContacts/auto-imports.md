---
title: Auto-Imports
subject: SuiteContacts
old_url: 'http://emarsys.dev/old/suite/contacts/auto-imports/'
---

The Auto-Imports Page**Contacts**
=================================

 menu ->** Auto-Imports ** Auto-imports are a great way to ensure that you keep an external contact database synchronized with Suite. You simply define the fields that you want to import, the source where you will place the import file, and Suite takes care of the rest. You can place your source files either on a [WebDAV](http://en.wikipedia.org/wiki/WebDAV) folder provided to you by Emarsys Support, or on your own [SFTP](http://en.wikipedia.org/wiki/SSH_File_Transfer_Protocol) or [FTPS](http://en.wikipedia.org/wiki/FTPS) server. Suite checks the WebDAV for new files every minute, the SFTP or FTPS servers every hour. All contacts imported via the auto-import are saved in Suite as a contact list with the following naming convention:

**auto-import-name YYYY-MM-DD HH:MM**

 In order to configure an auto-import, you will need a sample file. This is used to match the fields and values and to check that the text and field delimiters are correct. A sample file need only contain one or two actual contacts but these must have:

- All the fields that will be included in the actual import files, <span style="text-decoration: underline">in the same order</span> as the import files
- <span style="text-decoration: underline">All</span> the possible values for <span style="text-decoration: underline">all</span> the multiple- and single-choice fields in the import files

 Before you start with an import, you might want to read the following:

- [Manually importing contacts](/SuiteContacts/manual-import.md "Manually Importing Contacts")
- [Import FAQ](/SuiteContacts/import-faq.md "Data Import FAQ")
- [CSV guidelines](/DataManagement%20@zh-hans/csv-files.md "CSV Guidelines")

 On this page you can:

1. [View, edit and delete existing existing auto-import configurations](#edit-auto-import)
2. [Enable and disable existing auto-imports](#enable)
3. [Configure a new auto-import](#new-auto-import)

### 1. The Auto-imports list

 All the auto-imports that you have configured are displayed in the list at the top of the page.

<div class="row">[![auto-import-list](/assets/images/2015/02/auto-import-list1.png)](/assets/images/2015/02/auto-import-list1.png)</div><a name="edit-auto-import"></a>##### Editing auto-imports

 To edit an auto-import, click the [![edit-icon](/assets/images/2015/02/edit-icon.png)](/assets/images/2015/02/edit-icon.png)icon. This will open the first page of the Auto-import wizard (see below for details). If you want to edit any of the field or value matches, you must upload another sample file. <a name="enable"></a>

##### Enabling and disabling auto-imports

 You can also use the controls in the **Status** column to enable and disable auto-imports directly in the list.<a name="new-auto-import"></a>

### 2. Configuring a new Auto-Import

 To configure a new auto-import, proceed as follows:

1. Click **Create New Auto-Import** to open the auto-import wizard.
2. Select the **File Source**: WebDAV, SFTP or FTPS. If you select SFTP or FTPS, you must provide the path for this server as well as the user name and password. Suite will verify these credentials on completing the wizard.
3. Define the naming convention for the source files. This is a crucial step because you many configure many auto-imports in your account, and Suite must know exactly which naming convention applies to which import configuration. Please note that files names are <span style="text-decoration: underline">case sensitive</span>.
4. Define the naming convention and password for the compression file, if one is used.
5. Upload your sample file.
6. From this point on you must simply match the fields and their values as for [manual imports](/SuiteContacts/manual-import.md "Manually Importing Contacts").
7. Give the auto-import a name and save the wizard.
 
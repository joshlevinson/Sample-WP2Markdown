---
title: 'Data Import FAQ'
subject: SuiteContacts
old_url: 'http://emarsys.dev/old/suite/contacts/import-faq/'
---

Data Import FAQ##### Configuring your auto-import

- [What is the difference between using a WebDAV folder or an SFTP/FTPS server for auto-imports?](#configure1)
- [What sort of naming convention should I use for auto-imports?](#configure2)
- [Why do I need a sample file for auto-imports?](#configure3)
- [Are any of the dummy contacts in my sample file actually imported?](#configure4)
- [What encoding should I use for import files?](#configure5)
- [What file types are supported?](#configure6)
- [What difference does the Contact Language field make in the import configuration?](#configure7)
- [What does the source file language refer to?](#configure8)

##### General

- [Why are the import files deleted from my SFTP or FTPS servers?](#general1)
- [Why can't I edit all of the auto-imports in the list?](#general2)
- [Can I add imported contacts to an existing contact list?](#general3)

##### Errors

- [I received an error that my source connection could not be accessed. What can I do to resolve this issue?](#errors1)
- [What if I enter the wrong source credentials while configuring the auto-import?](#errors2)
- [What happens if I select the wrong text or field delimiter?](#errors3)
- [What should I do if I see auto-import errors in the Notification Center?](#errors4)
 
<a name="configure1"></a>
===============================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left;">What is the difference between using a WebDAV folder or an SFTP/FTPS server for auto-imports?</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">- A [WebDAV](http://en.wikipedia.org/wiki/WebDAV) is an SSL-secured source hosted and maintained by Emarsys. This is convenient for many clients because Emarsys Support will set it up for you (free of charge) and all you need to do is use a suitable client application such as [Bitkinex ](http://www.bitkinex.com/)or [Cyberduck ](https://cyberduck.io/?l=en)to access the folder, or program automatic updates directly from your CRM. Suite checks the WebDAV of each account every minute and processes any new files it finds there. Processed files are saved back on the WebDAV with the following naming convention: - **filename.csv.done** - for successful imports
- **filename.csv.error** - for unsuccessful imports. A notification with details of the error will be sent to the Notification Center.
- **filename.csv.ignore** - for files whose names do not match the naming convention defined for any of the enabled auto-imports.

Note: if you use a compression file, the import file will be extracted to the WebDAV and renamed as above, and the compression file deleted.

- [SFTP](http://en.wikipedia.org/wiki/SSH_File_Transfer_Protocol) or [FTPS](http://en.wikipedia.org/wiki/FTPS) servers are the most secure transfer protocols available and should be used if you have the technical resources available. Suite checks these external sources once every hour and successfully imported files are deleted from the source.<a name="configure2"></a>
 
</td> </tr></tbody><thead><tr><th style="text-align: left;">What sort of naming convention should I use for auto-imports?</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">We recommend including both static and dynamic parts in the file names. The static part should be clear and easily understandable, ideally relating to some aspect of your customer lifecycle strategy, while the dynamic part (e.g. a timestamp) will differentiate individual files. The dynamic part is represented by a wildcard asterisk ***** in the naming convention field.

##### Examples

- If you will only ever need one auto-import configuration, you can use a simple naming convention such as ***.csv**. This will mean that *every* .CSV file placed on the source folder will be processed.
- If you use more than one auto-import, then we recommend to match the static part to the auto-import name, and keep the dynamic part for a timestamp. In this way you could define the naming convention for the **converted leads** auto-import as: **converted-leads-*.csv**, and then name each individual file as: **converted-leads-2015-02-12.csv**

Important: File names are <span style="text-decoration: underline;">case sensitive</span>.<a name="configure3"></a>

 </td> </tr></tbody><thead><tr><th style="text-align: left;">Why do I need a sample file for auto-imports?</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">A sample file is necessary so that Suite knows which fields to expect in the import files, and how to map them and their values to existing fields in the Suite database. If you make any changes to the import files, however minor, you should upload a new sample file based on the new import file.

A sample file must contain all the expected fields, in the correct order and with all the possible values for any multiple- and single-choice fields.<a name="configure4"></a>

 </td> </tr></tbody><thead><tr><th style="text-align: left;">Are any of the dummy contacts in my sample file actually imported?</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">No. Suite is only interested in the file settings and the fields and values.<a name="configure5"></a>

 </td> </tr></tbody><thead><tr><th style="text-align: left;">What encoding should I use for import files?</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">For most Suite accounts, only UTF-8 encoding is supported. The only exceptions are the accounts on the environment www.emarsys.net, which supports only Latin1. Please note that Suite does <span style="text-decoration: underline;">not</span> verify the encoding used; if you use any other encoding, the contact data you import may be corrupted and unusable.<a name="configure6"></a>

 </td> </tr></tbody><thead><tr><th style="text-align: left;">What file types are supported?</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">The import file itself must be a .CSV file. However, you can compress this file. The following compressions formats are supported: .ZIP, .RAR, .ARG, .GZIP, .TAR, .TGZ, .BZIP2, .7Z. If you do want to use a compressed file format, make sure you include the naming convention for the compression file and any password required to open it.<a name="configure7"></a>

 </td> </tr></tbody><thead><tr><th style="text-align: left;">What difference does the Contact Language field make in the import configuration?</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">None. This is purely in case you want to segment your contacts via language, for example when sending newsletters in multiple languages.<a name="configure8"></a>

 </td> </tr></tbody><thead><tr><th style="text-align: left;">What does the source file language refer to?</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Changing the language setting of the import file can affect two things:

1. The field names and values If a file language is defined, Suite will use that language to match the fields and their values in the import file. Please note that this requires you to provide the relevant translations for any custom fields included, in the respective language(s).
2. The date format Certain date formats are associated with different languages. Suite will check the sample file for the date format and if this does not match the language, an error will be shown in the auto-import wizard.<a name="general1"></a>
 
</td> </tr></tbody><thead><tr><th style="text-align: left;">Why are the import files deleted from my SFTP or FTPS servers?</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">This is a precaution that we take to ensure that the same file cannot be imported twice.<a name="general2"></a>

 </td> </tr></tbody><thead><tr><th style="text-align: left;">Why can't I edit all of the auto-imports in the list?</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Auto-import configurations which were set up prior to the release of Suite version 8.2 (February 2015) can still have settings which are either not yet supported by the new import feature, or which have since been superseded by improved functionality. Examples of such features are 'Newsletter opt-in', 'on-import campaign' or 'no duplication handling'. If you want to edit these auto-imports, please contact Emarsys Support.<a name="general3"></a>

 </td> </tr></tbody><thead><tr><th style="text-align: left;">Can I add imported contacts to an existing contact list?</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">No. To do this you should include a unique field in the import file (e.g. named after the auto-import name) and create a segment that filters for contacts with the appropriate value for this field.<a name="errors1"></a>

 </td> </tr></tbody><thead><tr><th style="text-align: left;">I received an error that my source connection could not be accessed. What can I do to resolve this issue?</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">In order for Suite to be able to access your external source, please ensure that:

- Emarsys Support have the external source IP and domain so that they can whitelist them on the Emarsys firewall
- Emarsys is whitelisted on your own firewall (contact Emarsys Support for all the necessary information)
- The external source username and password are correct, and have the correct user rights (read and write access for downloading and removing files)<a name="errors2"></a>
 
</td> </tr></tbody><thead><tr><th style="text-align: left;">What if I enter the wrong source credentials while configuring the auto-import?</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Suite will check these credentials when you exit the wizard and save your configuration. If there is a problem you will receive a notification within minutes.<a name="errors3"></a>

 </td> </tr></tbody><thead><tr><th style="text-align: left;">What happens if I select the wrong text or field delimiter?</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">You will soon notice if the wrong delimiters are used, as the entire sample file will show up as one single field with all the values in each line: [![wrong-delimiter](/assets/images/2015/02/wrong-delimiter.png)](/assets/images/2015/02/wrong-delimiter.png)<a name="errors4"></a>

 </td> </tr></tbody><thead><tr><th style="text-align: left;">What should I do if I see auto-import errors in the Notification Center?</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">If you get a notification that **Suite could not reach the server** , please check: - That the credentials you entered are correct
- That Emarsys is whitelisted and not blocked by your firewall
- That your server is working properly
 
 If you get a notification that **the import failed because of an issue with the import file**, please check that the encoding, delimiters, fields and rows of the import file are correct. If this error persists, upload a new sample file and check the configuration again.</td> </tr></tbody></table>
---
title: 'Data Transfer'
subject: ''
old_url: 'http://emarsys.dev/resources/data-transfer/'
---

In order to ensure that data transferred in and out of Suite is matched to the right contact and stored in the right format, you will need to ensure that your database fields are correctly set up.

In addition to this, you can choose from a number of available transfer protocols to match your own resources and business needs.

### Suite Data Fields

 All data transfer in and out of Suite is conducted using Suite data fields. There are a variety of options available, from manual through to fully automated imports and exports. Whichever method you use, it is very important to ensure that the fields being imported also exist in Suite, with the correct names and field types, so that the data can transfer correctly. It is also important to specify one field as the unique identifier, which will ensure that the right data is matched to the right person. In many cases, the field **email address** can serve as the unique identifier. However, since Emarsys Predict and many third-party applications look for the field **externalId** we recommend that you create a short text field with this name and use it in all your data transfers. When you update contact properties in Suite, the following rules apply:

- Single-choice and free text fields which contain values will overwrite any existing value
- Multiple-choice fields will overwrite all values every time. In other words, existing values will be deleted if they are not included in every update.
- Fields with no values will remain unaffected
- If you want to overwrite a value with an empty string, you must therefore explicitly define a NULL value for that field.
 
**Note:** All contacts fields can also be manually edited in the **Contact Properties** page. For more information, see:

- [Suite system fields](/Resources/system-fields.md "The Suite System Fields")
- [Creating custom fields](/Suite/custom-fields.md "Creating Custom Fields")
 
**Please note:** Whenever data is imported into Suite, the new values will always replace the existing ones. It is important to remember this in case you have more than one method of updating contact data, since automatic updates could result in manual updates being overwritten.

### Transfer Protocols

#### 1. Updating the Suite database using WebDAV

 When your Suite account is setup a WebDAV folder is also setup for you, which allows you to automate your data imports and exports in a safe and secure way. WebDAV uses the HTTPS protocol which means that it does not need to have exceptions added to firewalls to work which means you can start using it faster. You are issued with the following details:

- Server name
- Login
- Password
- The directory to use

 Using the above details you simply map in the directory as a shared folder, or use a client such as [www.bitkinex.com](http://www.bitkinex.com/) or [www.cyberduck.ch](http://www.cyberduck.ch/), and are then ready to start transferring files. Please note: If you already have an SFTP server on your side, we can link this to our WebDAV for you.

#### 2. Updating the Smart Insight database using FTPS

 If you have an existing SFTP/FTPS server that you use, then we can link it so that you can transfer files to and from Suite. To use your SFTP/FTPS server you just need to provide Emarsys Support with the following details, and they can then arrange for the facility to be configured for you:

- Server name
- Login
- Password
- The directory to use
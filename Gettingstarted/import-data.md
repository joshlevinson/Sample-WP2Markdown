---
title: 'Importing Data into Suite'
subject: 'Gettingstarted, SuiteContacts'
old_url: 'http://emarsys.dev/old/getstarted/contact-data/import-data/'
---

The Suite **Data Import** page provides functionality for performing manual imports and setting up automated imports.

### Prerequisites

 Before you begin to import data into Suite it is important to identify what fields you will need to store the data properly, consider the following:

- Have you selected which field will serve as unique identifier?
- Which contact properties do you want to include?
- Do any of the properties require a custom field to be created in Suite?
- Do the field types match the controls which collect the data on your side? For example: - Drop-down lists should use single-choice fields
- Tick boxes should use multiple-choice fields
- Use the correct text field type (short, long, very large)
- Dates should be formatted the same way

### Manual data import

 You can import a .CSV file from any location into Suite via the [**Data Import**](/SuiteContacts/manual-import.md "Manually Importing Contacts") page. This is an easy-to-use, intuitive feature which allows to you define settings such as the field separator and date format, as well as map fields and their values. You can also define whether or not to perform duplication handling on the imported contacts, set their opt-in status, save them as a contact list and even trigger an email.

### Automated data import

 Automated imports are an easy way to make batch updates to Suite from an external application, and can also be used to trigger email campaigns. To set up an automated import, simply follow the steps in the intuitive Auto-import Wizard. Then all you have to do is make sure that the right import file is sent to the storage location, at the right time. There is no limitation to the number of automated imports you can configure, but for reasons of duplication handling, only one import will run at a time. Automated imports also support so called pre-processing, which is where encrypted files can be automatically uncompressed and imported. The pre-processing can be configured as part of the Automated Import configuration, and relies on the password for each file remaining the same. Both PGP ([Pretty Good Privacy](https://en.wikipedia.org/wiki/Pretty_Good_Privacy)) and GPG ([GNU Privacy Guard](https://en.wikipedia.org/wiki/GNU_Privacy_Guard)) are supported. Suite supports a variety of standard compression formats, similar to those supported by[ 7-zip.org](http://www.7-zip.org/). For more information, please contact Emarsys Support.
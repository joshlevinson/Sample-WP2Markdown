---
title: 'Admin - About Fields'
tags: 'olh, SuiteAdmin'
old_url: 'http://emarsys.dev/suite/online-help/about-fields/'
---

**Admin menu ->** Field Editor**

#### Data field types

 In Emarsys eMarketing Suite, there are three types of data fields:

- **Custom fields**

Custom fields are created by you or another administrator. They can be edited, deleted or copied as required. On the **Field Editor Overview** page, click **New** or select a field and click **Edit** to open the **Field Generator** (see below), where you can create and adapt fields according to your needs.

- **System fields**

System fields were predefined by Emarsys; typical system fields are *Salutation, Title, First name, Last name, etc*.

**Attention**: These fields can neither be edited nor deleted. If you need a system field to be defined differently, for example, because you want to include more or other options in the *Title* field, you must create a copy of the system field and rename it; the new field will then behave like a custom field.

- **Voucher fields**

Voucher fields are specific fields which you create via [Voucher Management](/olh/voucher-management.md "Admin – Voucher Management Overview"). Basically, these fields are assigned to individual coupon pools which enable you to send vouchers with your emails.

#### Field formats

 In Emarsys eMarketing Suite, the following field formats can be used:

- **Text-entry field for numeric values only**

Fields of this type provide for a limited number of digits only; they are used for information like "the number of children in a household".

- **Text-entry field for short alphanumeric values**

Fields of this type can be filled with alphabetic characters as well as digits; input must not exceed 60 characters/digits.

- **Text-entry field for long alphanumeric values**

Fields of this type can be filled with alphabetic characters as well as digits; input must not exceed 255 characters/digits.

- **Text-entry field for large alphanumeric values with xy rows**

Fields of this type can be filled with any kind of information, and can contain any number of characters or numbers. If you expect more than one row for the entry (e.g. a box for comments), enter the number of desired rows.

- **Date-entry field**

Fields of this type are used to enter dates and consist of a drop-down menu which displays the numerals 1-31 for the day, another drop-down menu for January to December and a text-entry field for the year. These fields are used for information like the "date of birth".

- **Single choice**

Fields of this type can contain any number of options (so-called attributes), although only one option can be selected (e.g. "male" or "female" for the Gender field). Once you have selected Single choice, you can define the field further by deciding to use a drop-down box or radio buttons.

- **Multiple choice**

In fields of this type, more than one attribute can be selected. Once you have selected Multiple choice, you can define the field further by deciding to use check boxes or a multi-selection box.

- **URL field**

The URL field is a text-entry field created for entering links. This field type verifies the link syntax (i.e. the spelling, e.g. http://www.yourwebsite.at) which is entered; if the syntax is wrong, an error message is displayed.

**
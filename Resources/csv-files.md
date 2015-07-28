---
title: 'CSV Guidelines'
tags: 'DataManagement, Resources'
old_url: 'http://emarsys.dev/resources/data-transfer/csv-files/'
---

Data is transferred in and out of Suite in comma-separated file format (CSV). In order to ensure that the right values arrive in the right database fields, here is an overview of the conventions that we use. The most important thing is to ensure that your import/export settings in Suite match those of the external database, in particular:

- the field separator
- the date format
- whether or not the field names are in the first row

 Beyond using the .CSV file format itself, there are no real restrictions when transferring data to and from Emarsys. However, we recommend using the conventions described below as these are standard for the industry and will also enable you to take advantage of our import file validation feature.

### Consistency

 The most important rule for uploading data is that the format of all uploaded files must remain consistent. Once a format has been agreed upon, this should not subsequently be changed. If you do, please contact Emarsys Support before the changes take effect.<a name="encoding"></a>

### Encoding

 In order to maximize foreign language support and to ensure that content is correctly displayed, Emarsys uses UTF-8 encoding as a standard. However, encoding is determined by your recipient’s language, not by your location. For example, a sender based in Asia could use Latin1 encoding, if they intend to send to English-speaking countries only.

##### Changing the encoding

 Most standard texts editors will let you select the encoding of a file when you save it. You may have to activate this feature, or it will be offered directly in the **Save As** dialog, for example as with Notepad:

<div class="row">[![data-exchange-encoding](/assets/images/data-exchange-encoding.png)](/assets/images/data-exchange-encoding.png)</div>### Header Row

 The first row of the .CSV file must be a header row containing the field names, as this is required for field mapping.

### Separators

 The separator, or delimiter, character is what separates the individual data fields, and can be configured. The default character is the semicolon (';') but you can change it to comma (',') or tab {TAB}. <span style="color: #eb5a19;">**Please Note:**</span> Always select a character which does not appear in the actual data itself (or at least not often), to reduce the number of times you have to quote or escape values.

### Quoting

 If the data itself contains the separator character, then you need to indicate to the import mechanism that this is part of the field value, and it does not use it as an indication to start a new data row. To do this you must surround the entire field value with double quotes. In the example below, the separator ‘;’ appears in the text of the second field value. Therefore when this field comes to be imported, the entire value is enclosed in quotes.

<table align="left" border="1" class="wikitable" style="width: 100%;"><thead><tr><th>Value in Database</th> <th>Value in CSV</th> <th></th> </tr></thead><tbody><tr><td>Notebook computers</td> <td>…;Notebook computers;…</td> <td>No quoting required</td> </tr><tr><td>Laptops; notebooks</td> <td>…;"Laptops; notebooks";…</td> <td>Quotes required</td></tr></tbody></table>### 

### Escaping

 Similar to the separator character, if the imported text contains the quote character, this must also be indicated to the import mechanism, this time by ‘escaping’ it. Escaping is done by simply adding another quote character before. In the first example below, the quote character is the used in the text as an abbreviation for the measurement ‘inch’. In the second example, quotes are used not only to escape the ‘inch’ symbol but also to surround the entire value because of the use of the separator ‘;’ as well:

<table align="left" border="1" class="wikitable" style="width: 100%;"><thead><tr><th>Value in Database</th> <th>Value in CSV</th> <th></th> </tr></thead><tbody><tr><td>21" monitors</td> <td>…;21"" monitors;…</td> <td>Quote has been escaped</td> </tr><tr><td>21" monitors; flat screens</td> <td>…;"21"" monitors; flat screens";…</td> <td>Quotes and separators are used</td></tr></tbody></table> Attention:  Both the separator and the quote characters can be customized, but in each case the character used should be chosen with care.

### Empty Values

 Fields with no values must be still exported as an empty value without any quoting, so that the structure of the data is not affected.

##### **Example**

<table align="left" border="1" class="wikitable" style="width: 100%;"><thead><tr><th>Value in Database</th> <th>Value in CSV</th> <th></th> </tr></thead><tbody><tr><td>NULL</td> <td>…;;…</td> <td>Import recognises an empty field</td></tr></tbody></table>  
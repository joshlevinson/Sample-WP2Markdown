---
title: 'Using HTTPS Feeds in Suite'
subject: Suite
old_url: 'http://emarsys.dev/suite/contacts/http-feeds/'
---

Introduction
------------

 Suite supports the use of HTTPS Feeds to perform background data registration tasks, which can range from adding new contact data, updating existing data or even triggering transaction-specific emails. HTTPS Feeds use .php registration links that run in the background to transfer content, and trigger bespoke email campaigns. As a method for data transfer it provides an easy-to-configure powerful solution that is fast to set up with no programming skill requirements. However, it should be pointed out that this is less secure than using the Suite API (since it uses visible URLs) and is also both slower and can handle lower volumes of data traffic. Typical use cases for this feature are when embedded forms are used for contact registration or updates, triggering transactional mails from a web page, and as a smart way to create double opt-in solutions.

HTTPS feed types available
--------------------------

 Suite uses two types of HTTPS feed called register.php and register_bg.php, which both perform similar functions with some slight variations. They can be differentiated by their transaction type and trigger, but from the customer point of view the main differences are the speed with which the requests are processed and how the volume of traffic will affect this. Both are equally simple to set up, and can be integrated into external software (e.g. a web shop). Determining which type to use should be done based on customer requirements, using the following table:

<table border="1" cellpadding="1" class="wikitable" style="width: 100%;"><thead><tr><th>HTTPS Feed type</th> <td>register.php</td> <td>register_bg.php</td> </tr><tr><th>Immediacy</th> <td>Request is queued</td> <td>Request is immediate</td> </tr><tr><th>Volume limit</th> <td>10,000 requests per hour, fixed rate</td> <td>around 10,000 per hour, variable</td> </tr><tr><th>Track user_ID</th> <td>no</td> <td>yes</td> </tr><tr><th>Triggered by</th> <td>link</td> <td>link</td> </tr><tr><th>Form use</th> <td>Form must contain all required fields</td> <td>Only form ID is required</td> </tr><tr><th>Data Import method</th> <td>form</td> <td>import</td> </tr><tr><th>Duplication handling</th> <td>yes (standard fields only)</td> <td>yes (any field can be chosen)</td></tr></thead></table>### register.php

 This feed type makes use of a Suite form to add or update contacts, and can be used directly from Suite or integrated within a web page. All the fields used in the transaction and feed must exist in the form in order for this feed to work. Incoming transactions from this feed type are queued and processed at a fixed rate of 10,000 requests per hour. This results in very stable and predictable performance, and high volumes of incoming transactions will not affect (or be affected by) any other aspects of system performance. The downside to using this feed type is that because the transactions are queued, contact updates are not immediate – and the user_ID of the contact is not returned. This means that you cannot track the contact updates, emails or responses without logging into your Suite account. Register.php uses standard duplication handling (first name, last name, email address), except if a specific external key has been defined for this account. Emarsys Support will tell you if a specific external key has been set. The following parameters are used by register.php. Those in <span style="color: #ff0000;">red</span> are mandatory and must be included for the HTTPS feed to work.

<table border="1" cellpadding="1" class="wikitable" style="width: 100%;"><thead><tr><th>Parameter</th> <th>Description</th> </tr></thead><tbody><tr><td><span style="color: #ff0000;">CID</span></td> <td><span style="color: #ff0000;">This is your account ID and will be supplied by Emarsys Support</span></td> </tr><tr><td><span style="color: #ff0000;">inp_*xx*</span></td> <td><span style="color: #ff0000;">These are the fields used in the transaction, with *xx* being the field ID.</span></td> </tr><tr><td><span style="color: #ff0000;">f</span></td> <td><span style="color: #ff0000;">This is the ID of the form used by the transaction, and is needed to trigger the email.</span></td> </tr><tr><td>optin*</td> <td>This is the opt-in status of the contact. Text values are used, e.g. *y*=TRUE, *n*=FALSE.</td> </tr><tr><td>nl_optin</td> <td>This is the opt-in used for newsletters. It must contain the form ID of the newsletter form to which the contact is subscribed.</td> </tr></tbody></table><sup>*</sup> Opt-in information is not mandatory but should be included for all HTTPS feeds, except those which are part of a double opt-in registration.

#### Register Example

 Below is an example of the kind of information that you might want to collect in your web page and then send to Suite using register.php:

<table border="1" cellpadding="1" class="wikitable" style="width: 100%;"><thead><tr><th>Information</th> <th>Parameter</th> <th>Value</th> </tr></thead><tbody><tr><td>Account ID</td> <td>CID</td> <td>987654321</td> </tr><tr><td>Suite registration form ID</td> <td>f</td> <td>1234</td> </tr><tr><td>First name</td> <td>inp_1</td> <td>Joe</td> </tr><tr><td>Last name</td> <td>inp_2</td> <td>Bloggs</td> </tr><tr><td>Email address</td> <td>inp_3</td> <td>joe.bloggs@example.com</td> </tr><tr><td>Contact’s opt-in status</td> <td>optin</td> <td>TRUE</td></tr></tbody></table> Creating the HTTPS Feed using the above would result in the following URL: `<a class="external free" href="http://www1.emarsys.net/u/register.php?CID=987654321&f=1234&p=2&a=r&SID=&el=&llid=&counted=&c=&optin=TRUE&inp_1=Joe&inp_2=Bloggs&inp_3=joe.bloggs@example.com" rel="nofollow" target="_blank">http://www1.emarsys.net/u/register.php?CID=987654321&f=1234&p=2&a=r&SID=&el=&llid=&counted=&c=&optin=TRUE&inp_1=Joe&inp_2=Bloggs&inp_3=joe.bloggs@example.com</a>`

### register_bg.php

 This feed type uses a link which includes the ID of a Suite form and the IDs of the required fields (and in the case of single- or multiple-choice fields, the IDs of their values), and can be triggered by associating that link to a specified action on a web page. Unlike register.php, this feed type does not require the form to have content or contain any of the fields. To trigger the form successfully only the ID is required; all transactions are processed immediately and a user ID is returned. As the forms are processed immediately without queuing, the speed of individual transactions will vary according to the incoming volume and whatever other actions are using the database at the same time. A large number of registrations or a large import or export will slow down the speed of requests considerably. Depending on your implementation, this may return a false error if your timeout settings are too restrictive. If you expect registrations to peak at certain times, you can use up to five threads and should set your timeout settings accordingly. Register_bg.php uses more flexible duplication handling and any field can be selected by using the key_id variable (see below). The following parameters are used by register_bg.php. Those in <span style="color: #ff0000;">red</span> are mandatory and must be included for the HTTPS feed to work.

<table cellpadding="1" class="wikitable" style="width: 100%;"><thead><tr><th>Parameter</th> <th>Description</th> </tr></thead><tbody><tr><td><span style="color: #ff0000;">owner_id</span></td> <td><span style="color: #ff0000;">This is your account ID and can be supplied by Emarsys Support</span></td> </tr><tr><td><span style="color: #ff0000;">key_id</span></td> <td><span style="color: #ff0000;">This is the ID of the field used as the external key for duplication handling.</span><span style="color: #ff0000;">Whichever field is used, e.g. an external database ID or the contact email address, this field must also be included in the field parameters of the feed. **Note:** You can disable duplication handling by giving a value of *n* here (*key_id=n*). This means that all requests will enter a new contact in the database, regardless of whether they already exist or not.</span></td> </tr><tr><td><span style="color: #ff0000;">inp_*xx*</span></td> <td><span style="color: #ff0000;">These are all the fields used in the transaction, with *xx* replaced by the field ID.</span></td> </tr><tr><td><span style="color: #ff0000;">f</span></td> <td><span style="color: #ff0000;">This is the ID of the form used by the transaction, and is needed to trigger the email.</span><span style="color: #ff0000;">**Note:** If you are using register_bg.php and leave this parameter out, the HTTPS request will simply write the corresponding values to the database and without triggering an email.</span></td> </tr><tr><td>optin*</td> <td>This is the opt-in status of the contact. Text values are used, e.g. *y=TRUE*, *n=FALSE*.</td> </tr><tr><td>del</td> <td>This is a Boolean parameter, meaning it can have one of only two values:*1* (=TRUE) or *0* (=FALSE).If the value is given as 1, when a contact is returned by this feed all their entries in the database will be deleted and only those contained in the feed itself will remain. This can be used to ensure only values entered via this feed remain in the database.</td> </tr><tr><td>newsletter</td> <td>This is the opt-in used for newsletters. It must contain the form ID of the newsletter form to which the contact is subscribed.</td> </tr><tr><td>landing</td> <td>Here you can enter the URL of a landing page, e.g. a registration confirmation message.</td> </tr></tbody></table><sup>*</sup> Opt-in information is not mandatory but should be included for all HTTPS feeds, except those which are part of a double opt-in registration.

#### Register_bg Example

 Below is an example of the kind of information that you might want to collect in your web page and then send to Suite using register_bg.php:

<table border="1" cellpadding="1" class="wikitable" style="width: 100%;"><thead><tr><th>Information</th> <th>Parameter</th> <th>Value</th> </tr></thead><tbody><tr><td>Account ID</td> <td>owner_id</td> <td>987654321</td> </tr><tr><td>Suite registration form ID</td> <td>f</td> <td>1234</td> </tr><tr><td>inp_46</td> <td>Mr</td> <td></td> </tr><tr><td>First name</td> <td>inp_1</td> <td>Joe</td> </tr><tr><td>Last name</td> <td>inp_2</td> <td>Bloggs</td> </tr><tr><td>Email address</td> <td>inp_3</td> <td>joe.bloggs@example.com</td> </tr><tr><td>External key</td> <td>key_id</td> <td>Email address is used</td> </tr><tr><td>Contact’s opt-in status</td> <td>optin</td> <td>TRUE</td></tr></tbody></table> Creating the HTTPS Feed using the above would result in the following URL: `<a class="external free" href="https://www.emarsys.net/u/register_bg.php?owner_id=123456789&key_id=3&optin=y&f=1234&inp_46=1&inp_1=Joe&inp_2=Bloggs&inp_3=joe.bloggs@example.com" rel="nofollow" target="_blank">https://www.emarsys.net/u/register_bg.php?owner_id=123456789&key_id=3&optin=y&f=1234&inp_46=1&inp_1=Joe&inp_2=Bloggs&inp_3=joe.bloggs@example.com</a>`

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">If you are using a multiple-choice field to capture information and want to include more than one value, then each value must be entered separately and the parameter must be followed by square brackets [ ], otherwise only the last value will be taken, - Correct use: inp_100[]=1&inp_100[]=4&inp_100[]=7
- Incorrect use: inp_100=1&4&7
 
 Where *100* is the field ID and *1*, *4* and *7* are the IDs of the values you want to capture.</td></tr></tbody></table>The Restrictions of Using HTTPS Requests
----------------------------------------

 Although quick and easy to set up, the implementations described do have some limitations which you should consider:

- If exactly the same request is resent within 15 seconds, it is treated as a mistake and ignored. The error returned is: `HTTP/1.0 409 Conflict`.
- If a contact makes repeated submissions, repeated requests are sent
- It is cumbersome to edit active on-event campaigns
- Standard on-event campaigns have no response analysis over time
- Custom fields and their associated variables must be created for each request in advance. This can create large amounts of data in the database which is rarely used. For example, an email for order confirmation would need fields like product_name_1, product_price_1, product_vat_1, product_name_2,… etc.
- If you want to display repeated content in its own sections (e.g. show multiple products with their images and descriptions), you have to create all the sections in advance and use section targeting to display them. A large number of sections in the email campaign will also have an adverse impact on the launch speed of the email.

 For these reasons it is always recommended to use the Suite API if you have the development resources yourself.

### Error Handling

 The registrations will be submitted as a regular HTTPS message, with the corresponding error codes.

<table border="1" cellpadding="1" class="wikitable" style="width: 100%;"><thead><tr><th>Examples of successful responses might be:</th> </tr></thead><tbody><tr><td>HTTP/1.0 200 OK insert user_id=11223344 (for a new user registration)</td> </tr><tr><td>HTTP/1.0 200 OK update user_id=11223344 (for a contact profile update)</td> </tr></tbody><thead><tr><th>Examples of unsuccessful responses might be:</th> </tr></thead><tbody><tr><td>HTTP/1.0 400 Bad Request</td> </tr><tr><td>HTTP/1.0 405 Method Not Allowed</td> </tr><tr><td>HTTP/1.0 503 Service Unavailable</td></tr></tbody></table> For a full list of HTTPS error codes, see: <http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html>.

Setting up HTTPS Feeds
----------------------

 HTTPS feeds can be set up via a simple, five-step process:

1. Prepare the database fields
2. Create the form
3. Create the custom HTTPS feed
4. Create the transactional email (if required)
5. Implement the HTTPS feed in your web shop or 3<sup>rd</sup>-party application

 These steps are described in detail below.

### Step 1: Preparing the Database Fields

 The database fields are used to capture content in the transaction and display it in the email, for example name, booking reference, etc. This content is sent to the database via the HTTPS feed and from there is added to the email via personalization variables. In order to include a field in the HTTPS feed, the field ID is required. For system fields, the IDs are listed in the document *Suite Field IDs and Values.* For custom fields, you must open the field in the **Field Generator** dialog in Suite. To do this, go to the **Administration** Menu, **Field Editor**, select the field and click **Edit**. The field ID can be found in the browser address bar of the **Field Generator** and is listed as *field_id=xxxx* where x is a numeric value (e.g. *field_id=1234*). [![Finding the field ID and value ID for a multiple-choice field](/assets/images/Using_HTTP_Feeds_1.png)](/assets/images/Using_HTTP_Feeds_1.png "Finding the field ID and value ID for a multiple-choice field") For single- and multiple-choice fields, you will also need to know the IDs of the hard-coded values (for all other fields you can simply enter the values manually). You can find the IDs as follows:

- System fields - *Suite Field IDs and Values* document.
- Custom fields - In the **Field Generator**, hover your mouse over the delete (**X**) icon for each value and you will see the ID in the bottom left of the dialog, displayed as *javascript:this.disabled=true;DeleteAtt('3')* where *3* is the ID of the value.

 Once you have selected and prepared the fields you will be using, make a note of their names and IDs for use in steps 3 and 4.

### Step 2: Creating the Form

 Each HTTPS feed needs its own registration form. To create a form, open the **Forms Manager**, choose *General Registration* in the **Create New** drop-down and click **Create**. Depending on the type of HTTPS feed used, you must now complete the form and add your selected fields to it (if using register.php), or leave it and only use the ID to trigger emails (if using register_bg.php). To find the form ID, hover the cursor over the icons to the right of the **Forms** list (View, Edit, Delete). The form ID is displayed in the bottom left of your browser window as: *javascript:Preview(‘2955’);* where *2955* is the form ID. Alternatively, open the preview of the form and the ID is displayed in the browser address bar as: *f=2955*. [![Finding the ID of a form](/assets/images/Using_HTTP_Feeds_2.png)](/assets/images/Using_HTTP_Feeds_2.png "Finding the ID of a form")

### Step 4: Creating the Transactional Email in Suite

 If you want to trigger a transactional email with the HTTPS feed, once you have completed the above steps you must now create an email campaign. This campaign must be an on-event campaign, based on a registration form, with the transactional feed registration form selected. For example: [![Creating the transactional on-even email campaign](/assets/images/Using_HTTP_Feeds_3.png)](/assets/images/Using_HTTP_Feeds_3.png "Creating the transactional on-even email campaign") On the Content Creation page you add the fields which should be displayed by using the personalisation variables. The example below is how a booking confirmation email might look in Suite: [![Using personalisation variables in the email](/assets/images/Using_HTTP_Feeds_4.png)](/assets/images/Using_HTTP_Feeds_4.png "Using personalisation variables in the email") And here is how it might look in the email itself: [![Filling the personalisation variables via the HTTP feed](/assets/images/Using_HTTP_Feeds_5.png)](/assets/images/Using_HTTP_Feeds_5.png "Filling the personalisation variables via the HTTP feed") Once you have finished creating your campaign, go to the Scheduling page and select whether the email will be sent immediately after the submission has been received, or with a delay (in hours or days). After checking the personalisation you can activate the email campaign, and the transactional email is now ready to launch.

### Step 3: Creating the Custom HTTPS Feed

 The next step is to define the HTTPS feed that submits the data which triggers the database update and/or the transactional email. This feed is a URL and is constructed as follows: 1. URL - this is the URL containing the environment domain of your Suite account, and will be one of:

- https://www.emarsys.net/u
- https://www1.emarsys.net/u
- https://login.emarsys.net/u
- https://suite.emarsys.net/u
- https://suite5.emarsys.net/u

 2. HTTPS feed type - this refers to the file used for the feed and can be either of:

- register_bg.php?
- register.php?

 3. Parameters - these contain all the necessary data required to identify the email, add content and launch it. Multiple parameters can be separated by '&'. An example URL would therefore look something like this: `<a class="external free" href="https://www.emarsys.net/u/register_bg.php?parameter=value&parameter=value&parameter=value(%E2%80%A6)" rel="nofollow" target="_blank">https://www.emarsys.net/u/register_bg.php?parameter=value&parameter=value&parameter=value(…)</a>`

### Step 5: Implementing the HTTPS feed

 Once all the above steps have been completed, you simply pass on your URL to the administrator of your web shop (or other software application), and instruct them to send this request according to your requirements. This is the only part of the process which requires any degree of technical knowledge. Once this step is complete, the HTTPS feed will be up and running.
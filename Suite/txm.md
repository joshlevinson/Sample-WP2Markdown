---
title: 'Transactional Emails in Suite'
subject: Suite
old_url: 'http://emarsys.dev/old/suite/campaigns/txm/'
---

Introduction
------------

 A transactional email is a single message sent to a single recipient, which refers to a specific interaction between the recipient and the sender (the 'transaction'). As opposed to batch mailings, where the same content is sent to a large volume of contacts at the time of the sender’s choosing, a transactional mail is triggered by the recipient, typically via an action performed on a web page, and contains information relevant only to that person. Transactional emails are also referred to as real time messages (RTM). Examples of such emails would be payment confirmation, password reset request, travel confirmation, etc. In many cases a transactional email does not require an opt-in from the recipient, and consequently such mailings may not contain any marketing content or advertising. Transactional emails can be launched either immediately after being triggered, or scheduled to be launched after a pre-set time delay. In eMarketing Suite, there are several ways to set up transactional emails:

- Using an HTTP request
- Using the Automation Center basic functionality
- Using the Suite API to create transactional programs
- Using the Suite API to create transactional emails with transaction-specific content

 Using an http request is simple to set up and requires minimal effort on the part of the customer. The Automation Center is even easier to use but has limited functionality. The Suite API does require an initial development effort but offers a correspondingly greater set of functionality. It can be used to create more complex Automation Center programs and also to create transactional emails which contain transaction-specific content. In all cases, a single email campaign is created and activated, which is then launched as individual emails every time the transaction is performed. The method you select will depend on your own technical resources and the use cases you wish to implement. For more information please contact Emarsys Support.

Method 1: Using an HTTP Request
-------------------------------

 The HTTP method makes use of Suite fields and forms. The fields transfer data from the transaction source to the Suite database, and the forms trigger the email launch. HTTP feeds can be set up via a simple, five-step process:

1. Prepare the database reference fields.
2. Create the transactional form.
3. Create the custom HTTP feed.
4. Create the transactional email.
5. Implement the HTTP feed in your web shop or 3<sup>rd</sup>-party application.

 These steps are described in detail below.

### Step 1: Preparing the Database Fields

 The database fields are used to capture content in the transaction and display it in the email, for example name, booking reference, etc. This content is sent to the database via the HTTP feed and from there is added to the email via personalization variables. In order to include a field in the HTTP feed, the field ID is required. For system fields, the IDs are listed in the Appendix of this document. For custom fields, you must open the field in the Field Generator dialog. To do this, go to the **Administration Menu**, **Field Editor**, select the field and click Edit. The field ID can be found in the browser address bar of the **Field Generator** and is listed as *field_id=xxxx* where x is a numeric value (e.g. *field_id=1234*). For single- and multiple-choice fields, you will also need to know the IDs of the hard-coded values (for all other fields you can simply enter the values manually). You can find the IDs as follows:

- System fields - there is a list of the IDs of all values for system single- and multiple-choice fields in the Appendix to this document.
- Custom fields - In the Field Generator, hover your mouse over the delete (**X**) icon for each value and you will see the ID in the bottom left of the dialog, displayed as `javascript:this.disabled=true;DeleteAtt('1')`, where *1* is the ID of the value.

 Once you have selected and prepared the fields you will be using, make a note of their names and IDs for use in steps 3 and 4.

<div class="center"><div class="floatnone">[![Finding the field ID and value ID for a multiple-choice field](/assets/images/2014/04/Transactional_in_Suite_Page_05_Image_0002.png)](/assets/images/2014/04/Transactional_in_Suite_Page_05_Image_0002.png)</div></div>### Step 2: Creating the Transactional Form

 Each transactional email needs its own registration form. To create a form, open the **Forms Manager**, choose *General Registration* in the **Create New** drop-down and click **Create**. You should enter a name related to your transactional email then click **Save**. Depending on the type of HTTP feed used (see below), you must now complete the form and add the fields you have selected to it (if using register.php), or leave it and use only the ID to trigger emails (if using register_bg.php). To find the form ID, hover your mouse over the icons to the right of the **Forms** list (View, Edit, Delete). The form ID is displayed in the bottom left of your browser window as: `javascript:Preview('2955');`, where *2955* is the form ID. Alternatively, open the preview of the form and the ID is displayed in the browser address bar as: *f=2955*.

<div class="center"><div class="floatnone">[![Finding the ID of a form](/assets/images/2014/04/Transactional_in_Suite_Page_05_Image_0003.png)](/assets/images/2014/04/Transactional_in_Suite_Page_05_Image_0003.png)</div></div>### Step 3: Creating the Customer HTTP Feed

 The next step is to define the HTTP feed that submits the data which triggers the transactional email. This feed is a URL and is constructed as follows: 1. URL - this is the URL containing the environment domain of your Suite account, and will be one of:

- https://www.emarsys.net/u
- https://www1.emarsys.net/u
- https://login.emarsys.net/u
- https://suite.emarsys.net/u
- https://suite5.emarsys.net/u

 2. HTTP feed type – this refers to the file used for the feed and can be either of:

- register_bg.php?
- register.php?

 3. Parameters – these contain all the necessary data required to identify the email, add content and launch it. Multiple parameters can be separated by '&'. An example URL would therefore look something like this: `https://www.emarsys.net/u/register_bg.php?parameter=value&parameter=value&parameter=value(…)`

#### HTTP feed types

 There are two types of feed available, register_bg.php and register.php. Both are equally simple to set up and both can be fully integrated into external software (e.g. a web shop). However, there are some important differences which should influence your decision. Both types have mandatory and optional parameters, which are listed below.

##### register.php

 Use this type of feed if you want to use a Suite form to add or update contacts. The form can be used directly or integrated into a web page. All the fields used in the transaction and the feed must also exist in the form. Incoming transactions from this feed type are queued, which means that it can handle high volumes (up to 10,000 requests per hour) without the performance being affected. The downside of this is that contact updates are not immediate. Furthermore, the user_ID of the contact is not returned, therefore you will not be able to track the emails or their responses without logging in to your Suite account. Standard duplication handling is used here (first name, last name, email address), except is a specific external key has been defined for this account. **Mandatory parameters**

<table class="wikitable"><thead><tr><th>Parameter</th> <th>Description</th> </tr></thead><tbody><tr><td>CID</td> <td>This is your account ID and can be supplied by Emarsys Support</td> </tr><tr><td>inp_*xx*</td> <td>These are the fields used in the transaction, with *xx* being the field ID</td> </tr><tr><td>f</td> <td>This is the ID of the form used by the transaction, and is needed to trigger the email</td> </tr></tbody></table>**Optional parameters**<table class="wikitable"><thead><tr><th>Parameter</th> <th>Description</th> </tr></thead><tbody><tr><td>optin</td> <td>This is the opt-in status of the contact. Text values are used, e.g. *y*=TRUE, *n*=FALSE</td> </tr><tr><td>nl_optin</td> <td>This is the opt-in used for newsletters. It must contain the form ID of the newsletter form to which the contact is subscribed</td></tr></tbody></table>##### register_bg.php

 Use this type of feed if you only want to attach a link to whatever action should trigger the email. The form itself is not used; only the ID is required. Incoming transactions are processed immediately, and a user_ID is returned. However, performance is affected by high volumes and therefore we recommend a limit of 10,000 requests per hour. **Mandatory parameters**

<table class="wikitable"><thead><tr><th>Parameter</th> <th>Description</th> </tr></thead><tbody><tr><td>owner_id</td> <td>This is your account ID and can be supplied by Emarsys Support</td> </tr></tbody><thead><tr><td>key_id</td> <td>This is the ID of the field used as the external key for duplication handling. Whichever field is used, e.g. an external database ID or the contact email address, this field must also be included in the field parameters of the feed.**Please Note:** You can disable duplication handling by giving a value of n here (*key_id=n*). This means that all requests will enter a new contact in the database, regardless of whether they already exist or not.</td> </tr></thead><tbody><tr><td>inp_*xx*</td> <td>These are all the fields used in the transaction, with *xx* replaced by the field ID.</td> </tr></tbody><thead><tr><td>f</td> <td>This is the ID of the form used by the transaction, and is needed to trigger the email.**Please Note:** If you are using register_bg.php and leave this parameter out, the HTTP request will simply write the corresponding values to the database and will not trigger any email.</td> </tr></thead></table>**Optional parameters**<table class="wikitable"><thead><tr><th>Parameter</th> <th>Description</th> </tr></thead><tbody><tr><td>optin</td> <td>This is the opt-in status of the contact. Text values are used, e.g. *y*=TRUE, *n*=FALSE.</td> </tr><tr><td>del</td> <td>This is a Boolean parameter, meaning it can have one of only two values:1 (=TRUE) or 0 (=FALSE).If the value is given as 1, when a contact is returned by this feed all their entries in the database will be deleted and only those contained in the feed itself will remain. This can be used to ensure only values entered via this feed remain in the database.</td> </tr><tr><td>newsletter</td> <td>This is the opt-in used for newsletters. It must contain the form ID of the newsletter form to which the contact is subscribed.</td> </tr><tr><td>landing</td> <td>Here you can enter the URL of a landing page, e.g. a registration confirmation message.</td> </tr></tbody></table>**Example** Here we will show how a URL would be constructed (using register_bg.php) to send the following information to Suite.

<table class="wikitable"><thead><tr><th>Information</th> <th>Value</th> <th>Parameter</th> </tr></thead><tbody><tr><td>Account ID</td> <td>987654321</td> <td>owner_id</td> </tr><tr><td>Suite registration form ID</td> <td>1234</td> <td>f</td> </tr><tr><td>Salutation</td> <td>Mr</td> <td>inp_46</td> </tr><tr><td>First name</td> <td>Joe</td> <td>inp_1</td> </tr><tr><td>Last name</td> <td>Bloggs</td> <td>inp_2</td> </tr><tr><td>Email address</td> <td>joe.bloggs@example.com</td> <td>inp_3</td> </tr><tr><td>External key</td> <td>Email address is used</td> <td>key_id</td> </tr><tr><td>Contact’s opt-in status</td> <td>Opt-in is TRUE</td> <td>optin</td></tr></tbody></table>`https://www.emarsys.net/u/register_bg.php?owner_id=987654321&key_id=3&optin=y&f=1234&inp_46=1&inp_1=Joe&inp_2=Bloggs&inp_3=joe.bloggs@example.com`<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px solid #999;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon AdditionalInfo.png](/assets/images/2014/04/Icon_AdditionalInfo.png)](/assets/images/2014/04/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">If you are using a multiple-choice field and you want to include more than one value, each value must be entered separately and the parameter must be followed by square brackets `[ ]`, otherwise only the last value will be taken, e.g.`inp_100[]=1&inp_100[]=4&inp_100[]=7`, where *100* is the field ID and *1*, *4* and *7* the IDs of the respective values.</td> </tr></tbody></table>**Error Handling** The registrations will be submitted as a regular HTTP message, with the corresponding error codes. *Examples of successful responses might be:*`HTTP/1.0 200 OK insert user_id=11223344 (for a new user registration)``HTTP/1.0 200 OK update user_id=11223344 (for a contact profile update)` *Examples of unsuccessful responses might be:*`HTTP/1.0 400 Bad Request``HTTP/1.0 405 Method Not Allowed``HTTP/1.0 503 Service Unavailable`

<table cellpadding="1" class="wikitable" style="width: 100%; border: 1px solid #fff;"><tbody><tr><td scope="col" style="text-align: left; border: 1px solid #fff;" width="60px">[![Icon FurtherReading.png](/assets/images/2014/04/Icon_FurtherReading.png)](/assets/images/2014/04/Icon_FurtherReading.png)</td> <td scope="col" style="border: 1px solid #fff;">For a full list of HTTP error codes, see <http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html></td></tr></tbody></table>### Step 4: Creating the Transactional Email in Suite

 Once you have created your fields and transactional feed form, and defined your https feed, the next step is to create an email campaign to send the transactional emails. This campaign must be an on-event campaign, based on a registration form, with the transactional feed registration form selected. For example:

<div class="center"><div class="floatnone">[![Creating the transactional on-event email campaign](/assets/images/2014/04/Transactional_in_Suite_Page_10_Image_0002.png)](/assets/images/2014/04/Transactional_in_Suite_Page_10_Image_0002.png)</div></div> On the **Content Creation** page you add the fields which should be displayed by using the personalization variables. The example below is how a booking confirmation email might look in Suite:

<div class="center"><div class="floatnone">[![Using personalisation variables in the email](/assets/images/2014/04/Transactional_in_Suite_Page_10_Image_0003.png)](/assets/images/2014/04/Transactional_in_Suite_Page_10_Image_0003.png)</div></div> And here is how it might look in the email itself:

<div class="center"><div class="floatnone">[![Filling the personalization variables via the HTTP feed](/assets/images/2014/04/Transactional_in_Suite_Page_10_Image_0004.png)](/assets/images/2014/04/Transactional_in_Suite_Page_10_Image_0004.png)</div></div> Once you have finished creating your campaign, go to the **Scheduling** page and select whether the email will be sent immediately after the submission has been received, or a number of hours/days afterwards. After checking the personalization you can activate the email campaign. The transactional email is now ready to launch.

### Step 5: Implementing the HTTP feed

 Once all the above steps have been completed, you simply pass on your URL to the administrator of your web shop (or other software application), and instruct them to send this request according to your specifications. This is the only part of the process which requires any degree of technical knowledge. Once this step is complete, the transactional email will be up and running.

### The Restrictions of Using HTTP Requests

 Although quick and easy to set up, the implementation described above is limited in two important areas: performance and usability.

#### Performance issues

- If the upper limit of requests is reached, the system will stop accepting more requests until there is room for them. Any requests arriving in the meantime are lost.
- If register.php is used, since no user ID is returned, there is no notification of such lost requests.
- If a contact makes repeated submissions, repeated requests are sent.

#### Usability issues

- It is cumbersome difficult to edit active on-event campaigns
- Standard on-event campaigns have no response analysis over time
- Custom fields and their associated variables must be created for each request in advance. This can create large amounts of data in the database which is rarely used. For example, an email for order confirmation would need fields like product_name_1, product_price_1, product_vat_1, product_name_2, … etc.
- If you want to display repeated content in its own sections (e.g. show multiple products with their images and descriptions), you have to create all the sections in advance and use section targeting to display them. A large number of sections in the email campaign will also have an adverse impact on the launch speed of the email.

 Emarsys therefore recommends to all its customers that they use the *Automation Center* for the more straightforward transactional emails, or the *Suite API* if they can, since this overcomes all of the limitations described above.

Method 2: Using the Automation Center
-------------------------------------

 Many of the Automation Center programs can be described as real time messages, since they are individually triggered based on an action by the contact. They cover the more straightforward use cases, and are perhaps closer to event-based messages that true transactional emails, but they are simple to set up and require no development effort or technical knowledge. The *entry points* that you can use for event-based programs are:

- **Form** - The contact has submitted a registration form
- **Data change** - The value for the selected data field for the contact has been changed
- **New contact **- The contact has been entered in the account database for the first time
- **Abandoned shopping cart** - The contact has failed to complete a purchase in a web shop
- **External source** - This is the true transactional program, available through the Suite API (see below)

 Transactional Automation Center programs are triggered immediately rather than being queued, and there are no known limitations to sending volumes. Furthermore, the Program Summary provides an easy way to track the progress of a program over time.

Method 3: Using the API to Create Transactional Programs
--------------------------------------------------------

 In the Automation Center you can create programs with the entry point External source. These will be triggered by an API call which matches a contact ID to the external source of the program. The contact then enters the program and progresses along it according to the defined workflow. The advantage of this type of email is that it can be the start of a more complex process, such as a new lead welcome program. You can also use the program summary function to track contact responses through the programs, and use the API to return email response data. There are no known limitations on sending volumes for emails triggered via the API.

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/2014/04/Icon_BeCareful.png)](/assets/images/2014/04/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">The same external source can be used to trigger an On External Event email (see below) as well as an external source Automation Center program. There is no exclusivity check between the two features, which means you can trigger a program and send an external event email at the same time. This may be desired behavior; this is just an advisory note.</td></tr></tbody></table> Transactional programs are set up as follows:

1. Create an external source in Suite.
2. Create the transactional program in the Automation Center.
3. Create the API call to match the contact to the program.

### Creating the external source

 To create an external source, go to the **Administration** menu in Suite and open the **External Source** page. Here you can simply add a new source to the list. The sources you create here are the connectors which link the contact to the email. They are available in the Automation Center for selection as the program entry points, and also as trigger events in API calls. You should therefore try to give them intuitive names that are easily understandable.

### Creating the transactional program

 To create the transactional program, you only need to select **External source** as the entry point. The rest of the program can contain whatever actions or responses you want. In the External source node, you select the source that you created in the **External sources** page. An external source may only be used by one program at any one time.

### Creating the API call

 When you have your transactional program set up, you will need an API call containing the `Event` and `Trigger` methods. Once this call has been set up, and the program is active, every time a contact interacts with the API call, they will immediately enter the program. However, this is all that happens - the contact is matched to the program; no other data is transmitted. To include transaction-specific content in the API call you must set up a different type of email, as described below.

Method 4: Creating Emails with Transaction-specific Content
-----------------------------------------------------------

 Transactional emails with transaction-specific content are not part of the Automation Center but are individual on-event emails of the type **On External Event**. These types of emails contain two important functions which greatly improve the workflow of users when setting up transactional emails:

- **Content can be sent directly via the API and inserted via placeholders** - This means that customers no longer need to create many entries for product data in the contact database and use personalization variables to add the content to the email.
- **Dummy sections can be created which are set to duplicate** - This means that users no longer have to create as many sections as they have products, and use section targeting to display them. Instead the section is repeated as many times as its content appears in the API.

 This means that transactional emails can be created from integrated applications such as Magento and sent with content from that application, without that content ever having to be stored by Suite. The following transaction-specific content can be contained in the API call:

- Plain text, to be inserted anywhere in the email via the placeholders
- A link URL, to overwrite the section link (template-based emails only)
- An image URL, to replace the section image with an externally-hosted one (template-based emails only)

 Emails sent via this method are not restricted in terms of volume (as is the case with the HTTP requests), but launch time can be affected by the number of sections which have to be created. Otherwise the only limitations to mail sending are those of the environment and application itself. In other words, if an environment is not experiencing heavy load, there is no reason why an account cannot send tens of thousands of transactional emails per hour. However, we cannot give a guaranteed figure for the sending volume at this time. Setting up a transactional email which can receive and display transaction-specific content is a little more complicated and involves adding placeholders to the section content, which are then included in the API call. For this purpose the API uses JSON (JavaScript Object Notation), which is an easily-readable method of transmitting data.

### The API Call

 Here is an example for a JSON payload that can be used to trigger external events.


    {
     "key_id": "3",
     "external_id": "test@example.com",
     "data":
     {
      "global":
      {
       "itemName": "keyboard",
       "itemPrice": "123",
       "<placeholder_name>": "<placeholder_value>",
       …
      }
     }


### Passing Data with the API Call

 This section explains the various ways how you can work with the `data` parameter. JSON transmits data as "<placeholder>:<value>" pairs. Wherever the placeholder is located in the email, the corresponding value is substituted. These pairs are grouped in one of two ways, in an **object** or in an **array**. An **object** defines where in the email to apply them (i.e. globally or only in a particular section), by grouping them in a set of curly brackets: { }. There are two levels of objects:

- The first-level objects - These are the **"global"** object, which contains only "placeholder:value" pairs and applies to the entire email, and those for the section external identifiers, which contain an array of second-level objects and apply only to that specific section.
- The second-level objects - These are contained within the arrays of the section external identifiers and contain more "placeholder:value" pairs.

 First-level objects can only occur once in the JSON. If they are repeated, the values in the last object will overwrite those from the earlier ones. Here is an example of a JSON API call containing just two first-level objects and one second-level object:


    "data": {
     {
      "global": {
       "header": "default header",
       "item": "default item"
      },
      "single_section": [
       {
        "header": "sample header",
        "item": "sample item"
       }
      ]
     }
    }


 The advantage of placing the placeholder pairs in an array for the second object is that their values can ignore the global values. This means that you can define different values for the same placeholder in different sections. Here is an example of another API call which contains multiple second-level objects inside an array:


    "data": {
     {
      "global": {
       "header": "default header",
       "item": "default item"
      },
      "repeating_section": [
       {
        "header": "Header 1",
        "item": "Item 1"
       }
       {
        "header": "Header 2",
        "item": "Item 2"
       }
      ]
     }
    }


 In this case, Suite will repeat the section with the external identifier "repeating_section" as many times as there are objects within that array. In this way, for example, you can add as many products as you like to an email without having to create a separate section for each one.

### About the placeholders and their values

 The placeholders are added to the email using the format: %%placeholder_name%%. This applies both to custom-HTML and template-based emails. You can give them whatever name you like but can only use standard (latin1) alphanumeric characters (a-z, A-Z) and the underscore ( _ ). You cannot use blank spaces. The same character restrictions apply to the section external identifiers. It is therefore important to emphasize to customers who work in UTF-8 environments and use other character sets that the placeholders and identifiers must be formatted correctly, otherwise this feature will not work. The values that are returned by the JSON object may be encoded in UTF-8 without a problem. Depending on whether you are using a custom-HTML or template-based email, these values may also contain HTML formatting (see below). If a placeholder exists in an email but does not exist in the JSON object, it will be displayed as plain text in the email (e.g. ‘%%placeholder%%’). However, you can give an empty string as a value, in which case the placeholder will effectively be stripped out. There are also some system placeholders which can be used in the JSON, but are not included in the sections themselves. These start with an underscore, e.g. the "_url" placeholder in the example above. These can be used to overwrite the default image or link in a section (see *Testing the email in the preview*, below).

### Custom-HTML vs Template-based Emails

 The placeholders can be used in both custom-HTML and template-based emails. In custom HTML there are certain limitations, namely:

- You can only use a single JSON object (the "global"), containing just "placeholder:value" pairs. These pairs should not be repeated in the object, otherwise the final pair will overwrite the previous instances.
- You cannot use any arrays. If the JSON contains an array, this feature will not work and the content will not be added to the email.

 However, there is also a major advantage, in that you can include an entire HTML block in one single value, which will be inserted whole into the placeholder. This means that the customer can display a table with product information for multiple products in the same way that the sections in a template can be duplicated, but they have to take care of this themselves (i.e. add the required number of rows with content to the table in the HTML code). In template-based campaigns you can use placeholders in both advanced and standard mode. The main differences to custom-HTML emails are:

- You can use arrays to duplicate sections
- You can apply different values to the same placeholder in different sections

 Because the functionality for template-based campaigns is so much more extensive than for custom-HTML campaigns, the rest of this document will refer only to them.

Creating Emails with Transaction-specific Content
-------------------------------------------------

 To create a transactional email with transaction-specific content, the workflow is as follows:

1. Prepare the email to receive the transaction-specific content
2. Test the email in the preview
3. Activate the email
4. Set up the API call

### Preparing the email for transaction-specific content

[![](/assets/images/2014/04/Suite_API_Transactional_Page_07_Image_0002.png)](/assets/images/2014/04/Suite_API_Transactional_Page_07_Image_0002.png)#### Creating an On External Event email

 The email you use must be an on-event email of the type **On External Event**. You must also specify the **external source** which will identify this email in the API call. [![](/assets/images/2014/04/Suite_API_Transactional_Page_07_Image_0003.png)](/assets/images/2014/04/Suite_API_Transactional_Page_07_Image_0003.png)

#### Adding the external identifier to the section

 Once you have set up the framework of the email you can decide which sections you want to contain the transaction-specific content. For each of these sections you must enter an **external identifier**: The **external identifier** is used to create a new JSON object for this section. If multiple sections use the same identifier, then their placeholders will all have the same values. You can now add the placeholders and place them wherever you want in the email. You can add a placeholder wherever text input is possible, for example in the section header, body text, and also the link name and image name as well as the alternative text for images.

### Testing the email in the preview

 Once you have created the email with all the static content and all the placeholders for the dynamic content, you can test how this will look in the preview. In the example below, an email has been created with three section groups: [![](/assets/images/2014/04/Suite_API_Transactional_Page_08_Image_0002.png)](/assets/images/2014/04/Suite_API_Transactional_Page_08_Image_0002.png)

#### An example dummy repeating section

- **Recommended products** - This contains one dummy section which will repeat to display all the recommendations for the contact. It contains an external identifier, as well as placeholders for the name, price and description of the recommended products.
 
[![](/assets/images/2014/04/Suite_API_Transactional_Page_08_Image_0003.png)](/assets/images/2014/04/Suite_API_Transactional_Page_08_Image_0003.png)<div class="thumbcaption">#### One of two static sections for special offers

- **Special offers** - These are two fixed sections which will display special offers for that day. They also contains external identifiers, and details of the products on special offer at the time.

- **Images** - There are three fixed sections which display the images of the day. The preview for this email looks like this:

<div class="center"><div class="floatnone">[![Suite API Transactional Page 09 Image 0002.png](/assets/images/2014/04/Suite_API_Transactional_Page_09_Image_0002.png)](/assets/images/2014/04/Suite_API_Transactional_Page_09_Image_0002.png)</div> </div> The three images below can be replaced by using the system placeholders, and can display additional products according to whatever recommendation system the customer is using on their side. When you click **Edit Placeholders** (a new button on the top right of the pop-up), you can see all of the email content which can be added via the API. Sample values are provided for all placeholders by Suite. <div class="center"><div class="floatnone">[![Suite API Transactional Page 10 Image 0002.png](/assets/images/2014/04/Suite_API_Transactional_Page_10_Image_0002.png)](/assets/images/2014/04/Suite_API_Transactional_Page_10_Image_0002.png)</div> </div> This pop-up has the following information and controls: - **Global placeholders** - These are placeholders that are present in more than one section. The values defined here will be used if the checkbox **Use global** is checked for a placeholder or if no alternative values are defined.
- **Section placeholders** - These are the placeholders in each section, as entered by you.
- **System placeholders** - Placeholders which begin with an underscore, e.g. *_url_name*, are system placeholders which can be used to overwrite the section image and link. In this way you can link to an external image for each section and change these images whenever you like. These placeholders are not used in the section itself but can be added to the JSON if you want to replace the values in the section.
 
<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">If you use an external link to overwrite the section link, this does not use the Suite link redirect function and therefore these links cannot be tracked. Furthermore, if you use external images, these are not uploaded to the Suite Media Database and therefore Suite has no control over how they are displayed.</td></tr></tbody></table>- **Use global** - If a section contains a global placeholder, you can use this checkbox to take the global value, or leave it empty and manually define a different value.
- **Use section default** - This checkbox defines whether a system placeholder takes the section default link or image, or uses an external one.
- **Duplicate section (+)** - This icon duplicates the section so that you can test how this will look with multiple entries.
- **Show JSON** - This button creates a JSON object for the section according to the way you have previewed it. This can be copied and passed on to your API developer to give them an idea of the way you want your API call structured.
 
 Following the above example, we have entered some test values to our preview and repeated the recommended products section (1). One special offer has a defined value (2), the other is set to take the global values (3): <div class="center"><div class="floatnone">[![Suite API Transactional Page 12 Image 0002.png](/assets/images/2014/04/Suite_API_Transactional_Page_12_Image_0002.png)](/assets/images/2014/04/Suite_API_Transactional_Page_12_Image_0002.png)</div> </div> The email preview now shows the new values for the recommended products and special offers: <div class="center"><div class="floatnone">[![Suite API Transactional Page 13 Image 0002.png](/assets/images/2014/04/Suite_API_Transactional_Page_13_Image_0002.png)](/assets/images/2014/04/Suite_API_Transactional_Page_13_Image_0002.png)</div> </div> If you click the **Show JSON** button in the **Edit Placeholders** dialog, you will get the corresponding code example: <div class="center"><div class="floatnone">[![Suite API Transactional Page 13 Image 0003.png](/assets/images/2014/04/Suite_API_Transactional_Page_13_Image_0003.png)](/assets/images/2014/04/Suite_API_Transactional_Page_13_Image_0003.png)</div> </div> Note the single "global" object containing all the other data, and the arrays for each section. At the bottom I have manually added another object to the "recommended_products" array. This would create a third such section in the email. This JSON viewer is very useful for Suite users to be able to pass over a detailed description of how they want their content supplied by the API. They can copy and paste the example into an email for their developer to use as the basis of the API calls. ### Activating the email

 Emails with transaction-specific content are activated like any other on-event email. In the Scheduling page the delay is specified (if so desired), the personalization variables are checked and the email is activated. <table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">As described above, the personalization variables can only be in the permanent section content and not in the JSON object.</td></tr></tbody></table>### Setting up the API Call

 Once the email has been tested and activated, the API developer needs to set up the API call to provide the contact ID, email ID and the requisite content. Once this is done, the email is ready and will trigger to every contact that is returned by the API call. </div>
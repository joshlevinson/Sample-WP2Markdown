---
title: 'Getting Started with the Suite API'
tags: 'Getting Started, SuiteAPI'
old_url: 'http://emarsys.dev/suite-api/'
---

Our API documentation can be found on a separate website dedicated to the development and IT teams of our integrating partners: [**dev.emarsys.com**](http://dev.emarsys.com). You can reach this website via the **Developers** option in the main navigation menu. This contains the full interface reference, as well as code examples, the API demo tool and everything that you need to get started with the integration. On this page you can see a brief overview of the available functionality offered by the Suite API, and on the following pages you can find some [use cases and examples](/Getting%20Started/use-cases.md "API Use Cases") of how you might use the API to automate your digital marketing activities.

Basic Functionality
-------------------

 In this section we list the most important functionality available via the eMarketing Suite API, grouped by feature.

#### Contact Management

[![](/assets/images/EMS_API_DoWithIt_Contacts.png)](/assets/images/EMS_API_DoWithIt_Contacts.png) One of the main uses of an API is to synchronize contact data between the two databases. The eMarketing Suite API therefore offers a range of functions for creating, retrieving, updating and deleting contacts, which can be used to perform ad hoc actions or set up an automated synchronization process. **Functions**

- Create and update contacts individually or in batches (up to 1,000 at a time)
- Create contact lists
- Retrieve the values of multiple- and single-choice fields
- Retrieve the email response summary of individual contacts over a given time range
- Retrieve the registration source of individual contacts

#### Content Management

[![](/assets/images/EMS_API_DoWithIt_Content.png)](/assets/images/EMS_API_DoWithIt_Content.png) Another important feature is the ability to pass content for use in email campaigns, without having to log in to eMarketing Suite. The API lets you create and save HTML content for emails as well as include files retrieved from the Media Database. **Functions**

- Create new custom HTML emails
- Preview HTML and text versions of emails
- View the online version of the email
- Upload files to the Media Database
- Retrieve file URLs from the Media Database and use them in the email content

#### Campaign Management

[![](/assets/images/EMS_API_DoWithIt_SendMail.png)](/assets/images/EMS_API_DoWithIt_SendMail.png) Once the content for an email has been finalized, you can use the API to launch, schedule and test email campaigns. **Functions**

- Send test mails
- Schedule or launch email campaigns
- Trigger transactional emails
- Retrieve the launch status of an email campaign
- Assign (existing) email categories
- Use (existing) conditions and personalizations
- Select the recipient source (segment or list)

#### Data Export and Reporting

[![](/assets/images/EMS_API_DoWithIt_Reports.png)](/assets/images/EMS_API_DoWithIt_Reports.png) The export functions allow you to keep track of all new contact registrations, as well as follow the response rates for individual campaigns and for individual contacts. These can then be used in an external tool to cross-reference with other statistics, for example web analytics. **Functions**

- Export new registrations over a given time range
- Export data changes to new or existing contacts
- Export entire contact lists
- Query the status of an export
- Export all responses to specific emails or to all emails over a given time range
- Retrieve the delivery and response overview statistics for individual or multiple campaigns
- Retrieve the delivery and response details for all contacts on the launch list of an individual email

### Additional Features

 This section gives some additional information on how the API interacts with other eMarketing Suite features to enhance and automate your eMarketing activities.

#### Sending Transactional (Real-Time) Messages

 The eMarketing Suite API can be used to send transactional (real time) messages by triggering external events attributed to an email.

#### Using the Automation Center

 As an alternative, you can also set up Automation Center programs with entry points that are triggered by API calls. A number of different API calls can be used, depending on the desired workflow.

- **New Contact** entry point (uses the **Create Contact** function)

 In the Automation Center you can create a program with the entry point **New Contact**. Once this program is activated, it will be triggered by every **Create Contact** call made by the API.

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px solid #999;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">This program will also be triggered by any other method of adding new contacts (e.g. via import or form registration).</td></tr></tbody></table>- **Data Change** entry point (uses the **Update Contact** function)

 You can also use this call to trigger transactional emails using the **Data Change** entry point. The emails will be sent to every contact whose properties have been updated. This can be done for individual contacts or for batch updates.

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">- A different field must be selected for each program using this entry point.
- The updated value must be different from the previous value. One way to ensure this is to add a current time stamp to a custom field.
- This program will also send emails to any other contacts, new or existing, who have new values entered for this field via other methods (e.g. via import).
 
</td></tr></tbody></table>- **External Event** entry point (uses the **Event** function)

 The **Event** call retrieves unique identifiers which are created in Suite in the **External Events** page, and can be appended to any other API call. If a program is created with this entry point, all contacts returned by the first call are automatically added to the program with the respective external event identifier.

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px solid #999;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">Programs with this entry point can only be triggered by eMarketing Suite API calls.</td></tr></tbody></table>#### Link Tracking

 When using the API to launch emails created in Suite, all links in the HTML and text sources are still automatically tracked. There is no need for an explicit API call for this. Furthermore, you can define the name of the link and its category as special attributes of the HTML tag. **Example**`<a href="http://www.emarsys.com" ems:name="emarsys" ems:category="marketing">eMarketing Suite</a>` â&#134;&#146; When the email is created, the link is automatically converted into a trackable link with the name "emarsys" and in the category "marketing".

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px solid #999;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">- Either attribute may be empty, in which case the link is still tracked but without a name or category.
- Links in the text version are automatically tracked without a name or category, except when it is the same link as in the HTML version. In this case the text link is created with the same name.
- If an existing category is provided it is assigned to the newly created link.
- If the category is not present in the system at the time of creating the email, it is automatically created and assigned to the link.
 
</td></tr></tbody></table>
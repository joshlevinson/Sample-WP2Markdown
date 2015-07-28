---
title: 'Salesforce Integration: Use cases and examples'
tags: ''
old_url: 'http://emarsys.dev/suite/connect/salesforce-use-cases/'
---

Now that your integration is set up, you can begin to work with it. Here are a few use cases and examples:

##### 1. Managing contacts and contact data

- Export all contacts and leads from Salesforce to Suite
- Export campaign members from Salesforce to Suite
- Map fields between Salesforce and Suite
- Update existing contacts in Suite
- Add new contacts to Suite

##### 2. Sending campaigns

- Trigger transactional emails from Salesforce
- Trigger ad hoc batch campaigns from Salesforce

##### 3. Viewing responses

- View Suite response data in Salesforce

1. Managing contacts and contact data
-------------------------------------

#### Use case 1: Export all contacts and leads from Salesforce to Suite

 The first action following successful set-up should be a one-off import of all leads and contacts from Salesforce to Suite. Given the size restrictions of Salesforce campaigns, the easiest way to do this is to export your full list and import this manually into Suite, or ask Emarsys Support for assistance.

#### Use case 2: Export members of a single campaign from Salesforce to Suite

 Once you have your Campaign in Salesforce set up (with Type =Â *emarsys Email*) and added some Leads and/or Contacts, you can proceed by exporting campaign members to Suite. Click the **Create & Add** button in the **Add Campaign Members to Suite** List box:

<div class="row">[![sf-create-add-members](/assets/images/sf-create-add-members.png)](/assets/images/sf-create-add-members.png)</div> A new window will open (make sure you do not have pop-ups blocked):

<div class="row">[![sf-provide-contactlist-name](/assets/images/sf-provide-contactlist-name.png)](/assets/images/sf-provide-contactlist-name.png)</div> Add a name for the Suite contact list and click **Create & Add**. You will receive a confirmation that the contact list has been created and can already log in to Suite to work with it.

<table style="width: 100%;"><tbody><tr><td style="text-align: left; width: 80px; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</td> <td>For very large campaigns (> 10,000 members) it can take a few minutes until the contact list is fully complete.</td></tr></tbody></table><div class="row"></div>#### Use case 3: Map fields between Salesforce and Suite

#### 

#### Use case 4: Update existing contacts in Suite

  

#### Use case 5: Add new contacts to Suite

  

2. Sending Campaigns
--------------------

#### Use case 1: Trigger transactional emails from Salesforce

  

#### Use case 2: Trigger ad hoc batch campaigns from Salesforce

      

3. Viewing Responses
--------------------

  

#### Use case 1: View Suite response data in Salesforce

    

Export Salesforce contacts to Suite and work from there
-------------------------------------------------------

 You can export your Salesforce contacts or leads to Emarsys Suite. All you need to do is to set up a campaign in Salesforce and add contacts or leads (i.e., â&#128;&#156;Campaign Membersâ&#128;&#157;) to it. This campaign can then be exported. A typical workflow could look like this: Content from: https://emarsys.jira.com/wiki/display/DOCU/Suite+Integration+Manual <a name="_Toc336876733"></a>     **Â **

Automatic creation and update contacts/leads in Suite
-----------------------------------------------------

   Automatic creation and update of contact and leads can be enabled in the **EMS Cockpit **Tab:

<table><tbody><tr><td width="761"></td></tr></tbody></table>  

<a name="_Toc287085508"></a>1.3Â Â Â Â Â Â Â Â Â  Viewing email responses in Salesforce
---------------------------------------------------------------------------------------

 Once a day Email responses are retrieved from Suite. You can track your campaign's responses by viewing the responses directly from the **EMS Emails** Tab and selecting a specific Email:

<table><tbody><tr><td width="702"></td> </tr><tr><td width="702"></td></tr></tbody></table>  

<table><tbody><tr><td width="702"></td> </tr><tr><td width="702"></td></tr></tbody></table>   **View Response Summary** Click this button in order to have a look at the general Suite Email statistics:     View Email Preview Click this button in order to have a look at the Emailâ&#128;&#153;s content:  
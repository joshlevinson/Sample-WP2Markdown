---
title: 'Campaigns - Personalisation and Conditional Text'
subject: 'olh, SuiteCampaigns'
old_url: 'http://emarsys.dev/suite/online-help/personalization/'
---

**Campaigns** menu ->** Email Campaigns** -> **CMS** -> **Section editor** You can add placeholders to your email content which will then be replaced by dynamic text when the email is launched or previewed. There are two options: #### Personalization

 Personalization variables are an easy way to include personal contact data in your email. Wherever you see this icon you can select from a list of database fields and add a placeholder to the text. The placeholder will be displayed in the form: $FieldName$. When the email is sent to a contact, or a full campaign testmail is created, the corresponding value for this field will be substituted instead. In this way you can personalize your content by using the contact's real name, address,etc. #### Conditional Text

 Conditional text is a more flexible way to personalize your emails. This adds placeholders which will substitute text defined by you, according to filter conditions. In this way you can have one subject line for women and one for men, or different text in different languages, etc.  The placeholder will be displayed in the form: $COND_RuleName$. Click to open the **Available Rules** pop-up. It lists all existing rules plus general information on these rules (responsible user, creation date, etc.). - **Insert rules**

To insert a rule, activate the radio button next to it, then click **Insert**.

- **Create rules**

To create a new rule click **New Rule** and provide the required information:

1. Provide a name.
2. Provide a format, either text or HTML.
3. Select a variable, or **Choice**, e.g. Salutation.
4. Below, all available values for the variable are shown, e.g. Mr and Ms Make your selection.

**Please Note**: Variables and values are retrieved from the data fields.

1. In the text field below, enter the text which appears when the condition is fulfilled. Click to personalize the text.

To create alternative rules, click **New** **condition** and proceed as described above.

1. Finally, you can enter a text in the **Alternative text** field; this text is displayed when a value is missing. Make it something neutral, in accordance with our Salutation example above, this could be Dear customer.
2. Save the conditional rule and add it to the selected field by clicking **Insert**. If you do not want to use the rule right away and to go back to the **Available Rules** page, click **Close**.

#### Alternative Text

 If you are using the Simple Scheduling feature, you can enter alternative text for your personalization variables via this button in the **Content Creation** page.
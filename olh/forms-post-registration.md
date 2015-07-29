---
title: 'Forms - Post Registration'
subject: 'olh, SuiteFeatures'
old_url: 'http://emarsys.dev/suite/online-help/forms-post-registration/'
---

**Forms menu >** Post Registration** On the **Post Registration** page, you make settings for the page which confirms a registration, and for the email which notifies you about new registrations. The notification email contains information on the new subscriber and a link to their profile.

#### Make settings for the confirmation page

1. Decide if the Submit/Subscribe button in the form is to display the text you enter or an image which you upload. You can also use an image from the Media Database. To display an image, click **View Image**. To remove an image from the button, click **Clear Image**.
 
**Attention**: The image file name must not contain spaces, umlauts or other special characters.

1. You can enter a URL which takes customers to a web page of your choice (e.g. your homepage) after they clicked the Submit/Subscribe button in the registration form. If you do not enter a forwarding URL, the registration form window is closed after registration is complete.
 
**Attention:** The URL must have the format www.xxxxxxx.yyy. The http:// prefix is added automatically by the system.

Alternatively, you can also decide to direct customers to a page which is created by the system: Activate the corresponding option and click Create Landing Page; the Edit Landing Page dialog box opens, where you can make settings for the page. You can set up only one landing page per registration form; existing landing pages can be edited.

 Click **Save** to save your settings.

#### Make settings for the notification email

1. Enter an email address you or your company owns; after a customer has registered, a notification email will be sent to this address.
2. Specify the language to be used in the email.
3. Specify which additional information on the subscriber you want to receive; select a field name from the list and click [![r-arrows](/assets/images/r-arrows.png)](/assets/images/r-arrows.png); remove a field from the custom list by clicking [![l-arrows](/assets/images/l-arrows.png)](/assets/images/l-arrows.png).

 Click **Save** to save your settings. It is worth noting that although both forms of HTTP Feed are capable of performing duplication handling, due to the nature of register_bg the fields required are not as flexible as register.php. If duplication handling is a key factor then it is advisable to use register.php as you can specify whatever variables you want, rather than register_bg which is limited to using first name, last name & email address.

**
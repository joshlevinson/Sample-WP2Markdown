---
title: 'Integrating Suite Forms into Facebook'
subject: Suite
old_url: 'http://emarsys.dev/old/suite/contacts/facebook-forms/'
---

Introduction
------------

<span lang="EN-GB">Facebook allows owners of Facebook pages to integrate content from external websites, such as forms and applications, which can be used to enrich your contact database by generating new registrations and merge marketing channels. The forms can be hosted either by eMarketing Suite or on an external website.</span>

Prerequisites and Parameters
----------------------------

 Before you can start integrating an external form, you need the following:

- A verified Facebook Developer Account
- A good understanding of Facebook apps and Suite forms
- The form URL

 To verify a Facebook Developer Account you have to store your phone number or credit card information, and ensure the account is kept live by using it regularly. Facebook does sometimes block accounts that have not been used for a while. For the Facebook Application setup stage you will need two variants of the form URL:

- Domain URL
- Full URL

 See below for examples.

### Using Suite forms: identifying the URL

 You can collect new registrations from Facebook by integrating a Suite General Registration form. The other Suite forms (Newsletter registration, Tell-a-Friend and Contact Us) are also available if they better suit your objectives. To integrate a Suite form, proceed as follows:

1. Log in to Suite and then go to the **Forms** section, and locate the form that you wish to use in Facebook.
2. Click the form’s **edit** icon ([![edit-icon](/assets/images/2015/02/edit-icon.png)](/assets/images/2015/02/edit-icon.png))
3. Click **Source Code** in the menu on the left
4. In the **Hyperlink** section – copy the URL as follows:

<div class="floatnone" style="padding-bottom: 10px; padding-top: 10px;">[![facebook-forms-url](/assets/images/2015/05/facebook-forms-url-300x28.png)](/assets/images/2015/05/facebook-forms-url.png)</div>1. Change link.sampledomain.com with your suite environment link; see below for an example.

 The URL includes both parts for you will need Facebook form integration; make a note of them as follows:

- Full URL: `https://suite.emarsys.net/u/register.php?CID=123456789&f=12345`
- Domain URL: `suite.emarsys.net`

 You are now ready to proceed with the App setup.

App Setup Process
-----------------

 The process to create the app varies slightly depending on whether the form is hosted by Emarsys or embedded into a web page (i.e. hosted externally and based on an https feed). The main difference is that a form hosted on a web page needs a little more preparation.

### Creating the Facebook App

 To create the app in Facebook, proceed as follows:

1. Test to make sure that the form looks correct by pasting the Full URL into your browser.
2. Log in to the Facebook developer page <https://developers.facebook.com>
3. Click **My Apps** in the top left corner and then select **Add a New App**.
4. Select **Facebook Canvas** in the pop-up.
5. Name your new app and choose a category for your application.

<div class="floatnone" style="padding-bottom: 10px; padding-top: 10px;"> [![create-new-app-id](/assets/images/2015/05/create-new-app-id-300x162.png)](/assets/images/2015/05/create-new-app-id.png)</div>1. Click **Create App ID **to proceed with the creation, and then select the appropriate objects in security check.
2. You will be redirected to your application dashboard. Click **Settings** in the left panel.
3. In the **Contact Email **field, enter the email address of your Emarsys Success Manager or your email address.
4. In the **App Domains **field, enter your Domain URL.

<div class="floatnone" style="padding-bottom: 10px; padding-top: 10px;">[![contact-email-and-app-domain](/assets/images/2015/05/contact-email-and-app-domain-300x135.png)](/assets/images/2015/05/contact-email-and-app-domain.png)</div>1. Click **Add Platform** and choose **Facebook Canvas**.
2. In the **Secure Canvas URL**, enter the form's full URL.

<div class="floatnone" style="padding-bottom: 10px; padding-top: 10px;">[![facebook-canvas](/assets/images/2015/05/facebook-canvas-300x155.png)](/assets/images/2015/05/facebook-canvas.png)</div>1. Click **Add Platform** again and choose **Page Tab**.
2. In the **Secure Page Tab URL** field, enter the form's full URL.
3. In the **Page Tab Name** field, enter a name for the tab which will be displayed in your Facebook page.
4. In the **Page Tab Image**, click to upload an image for your tab.
5. Double-check all settings and then click **Save Changes**.
6. Go to the dashboard by clicking **Dashboard** on the left panel which will then display the App ID. Make a note of this ID.

<div class="floatnone" style="padding-bottom: 10px; padding-top: 10px;">[![check-app-id](/assets/images/2015/05/check-app-id-300x85.png)](/assets/images/2015/05/check-app-id.png)</div>### Adding the App to your Fan page

 Now that you have created the app, the next step is to integrate it to your Facebook page(s) after which it will be ready for use. Facebook uses a default URL which needs to have the App_ID added to it, which takes you to an interface that allows you to select what page(s) to link the app to. Proceed as follows:

1. Add the App_ID to the Facebook URL. The default Facebook URL is always the following:
 

    https://www.facebook.com/dialog/pagetab?app_id=YOUR_APP_ID&redirect_uri=YOUR_URL

1. Add your App_ID to the URL. Using the example from the setup process above (`832864850213207`) the URL would be:
 

    https://www.facebook.com/dialog/pagetab?app_id=832864850213207&redirect_uri=https://apps.facebook.com/832864850213207

1. Copy the URL you have just created, and paste it into a browser to launch the **Facebook Setup** page.
2. Use the **Choose Facebook Pages** dropdown menu to select the Fan page you want to link to.

<div class="floatnone" style="padding-bottom: 10px; padding-top: 10px;">[![add-page-tab](/assets/images/2015/05/add-page-tab-300x122.png)](/assets/images/2015/05/add-page-tab.png)</div>1. Click **Add Page Tab** to complete the process. You will be redirected to your application
2. By default, your Facebook app will not be public. In order to make your application available to the general public, click **Status & Review** in your app configuration page.
3. Switch to **Yes **to make your application publicy available.

<div class="floatnone" style="padding-bottom: 10px; padding-top: 10px;">[![emarsys-sample-application](/assets/images/2015/05/emarsys-sample-application-300x96.png)](/assets/images/2015/05/emarsys-sample-application.png)</div> You have now successfully linked the app to your Facebook page, and should be able to see the app with the embedded content in it. If your application is not visible in your Facebook Page, go to your page and click **More** in the top menu.
---
title: 'Mobile-optimized Custom HTML'
subject: 'SuiteContent, WebExtend'
old_url: 'http://emarsys.dev/old/suite/content/cms/custom-html/'
---

Introduction
------------

 This document outlines how to adapt the HTML code of an email so that it behaves in the same way as the mobile–ready templates created by Emarsys. <table style="width: 100%;"><tbody><tr><td style="text-align: left; width: 80px; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</td> <td>These guidelines are designed for custom-HTML emails, rather than for the Advanced Mode of sections in template-based campaigns. Although it is possible to use HTML code in mobile–ready templates, there are some limitations. We recommend that if you do intend to use custom HTML for mobile–ready templates, that you use a single-column layout in your design.</td></tr></tbody></table>### Brief Overview and History of Email Formats

 In order to understand how a mobile-ready template differs from standard HTML mail you need to understand the core concept of how an HTML template is composed. Email is now 30 years old and has gone through various evolutions with regard to content integration, enabling more and richer content messages. In 1996 email evolved from plain text to be able to support rich media content, and then in 1997 the HTML (4.0) format support was introduced which is now the core language of modern rich content messages. Email clients implemented HTML handling (MIME) and as web pages started to be made with nested tables – email messages also started using the same technique. In 1998 CSS was introduced to separate content from formatting, which enabled web developers to create semantic web pages using elements. But while web browsers followed and implemented the new standards and started to act and render the same way, email clients did not. Therefore their approach to content still falls short of full and proper HTML and CSS support. Furthermore, since email is an easy way to transmit viruses and other malware, security issues have led to further restrictions. For this reason Microsoft replaced the Outlook rendering engine in 2007, from the one used in its Internet Explorer browser to that used in MS Word. This led to some core HTML and CSS features becoming unsupported. For the same reasons, Gmail strips out everything outside the  section of an email, meaning that only inline styles can be used. On the other hand, web-based mail clients are becoming more popular and some of the main players like Hotmail, Yahoo! Mail and Gmail all rely on the web browser’s rendering engine to display email content. This should help to close the gap a little in terms of allowing for the same level of content as web pages to be displayed. ### The Difference between Desktop and Mobile Mail

 When sending content to a mix of mobile and desktop users it is important to bear in mind that your content will look very different depending on how it is opened. On a desktop monitor it is easy to spot links within text, for example, but on a mobile device they can be hard to find, let alone click. Also, comparing products with side-by-side images may look good on a wide screen but would be far too small on a mobile phone. So, in order to ensure the best looking content is delivered to all platforms, you can add a little code to your email which will enable it to display differently according to the device that opens it. Technical Approach
------------------

 If you want to send a mobile-ready email to your customers, the easiest way is to design a single column layout and use a style sheet to make changes specific to mobile devices. This allows for the content to be selectively displayed based on how the client accesses the content. This can be done by placing a media query section inside the `<style>` element in the `` section of your HTML code: 
    @media (max-device-width: 767px) { /* MOBILE CSS GOES HERE */ }

 Everything you put between the curly brackets will only be visible to mobile phones. Here you can: - Define the width of the email to fit mobile devices (e.g. 320 pixels, which is a typical width).
- Selectively hide or show sections of the email.
- Make the default font size, buttons, and links bigger.
- Adjust the images' width to fit the screen.
- Replace images with other images specifically for display on mobiles.
 
 Below is an example of some HTML code containing a media query and a mobile CSS. 
    
      
        <meta name="viewport" content="initial-scale=1">
        <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
        <title>Mobile-Ready Code Sample</title>
        <style type="text/css"> body, .yshortcuts { color: #000; } a,
        .yshortcuts a span { color: #00f; text-decoration: none; font-weight: normal; }
        #outlook a { padding: 0; } table { border-collapse: collapse; mso-table-lspace: 0pt;
        mso-table-rspace: 0pt; border: 0;
        } table td { border-collapse: collapse; } body { width: 100% !important; }
        .ReadMsgBody { width: 100%; } .ExternalClass, .ExternalClass p,
        .ExternalClass span, .ExternalClass font, .ExternalClass td, .ExternalClass
        div { line-height: 100%; } .ExternalClass img[class^=Emoji]
        { width: 10px !important; height: 10px !important; display: inline !important; }
        body { margin: 0; color: #000; background: #fff; } a { color: #00f; }
        a:active { color: #00f; } a:visited { color: #00f; }
    
        /* DESKTOP AND GLOBAL CSS GOES HERE */
        /*#MEDIAQUERY_START#*/
        @media (max-device-width: 767px) { body { margin: 0; padding: 0;
        -webkit-text-size-adjust: none; -ms-text-size-adjust: none; }
        div[class="yfix"] td[align=right] { text-align: left; }
        div[class="yfix"] .mobile_hidden { display: none !important; }
        div[class="yfix"] .reset_height_on_mobile { height: auto !important; }
        div[class="yfix"] .section { width: 100% !important; float: none !important; }
        div[class="yfix"] .section_image { max-width: none !important; }
        div[class="yfix"] .container { width: 320px !important; }
        div[class="yfix"] #header_image { content:
        url(http://example.com/path/to/mobile/image.jpg); width: 320px
        !important; height: 100px !important; } } /*#MEDIAQUERY_END#*/
        </style>
      
      
        <div class="yfix">
          <table cellspacing="0" cellpadding="0" border="0" width="100%" bgcolor="#fff">
            <tr>
              <td align="center">
                <table cellspacing="0" cellpadding="0" border="0" width="600" class="container">
                  <tr>
                    <td>
                      <img src="http://example.com/path/to/desktop/image.jpg" alt=""
                      width="600" height="120" id="header_image"/>
                      <p>This is visible in all clients</p>
                      <p class="mobile_hidden">This is visible only in desktop clients</p>
                    </td>
                  </tr>
                </table>
              </td>
            </tr>
          </table>
        </div>
      
    

### <span class="mw-headline" id="4adf6cbc93eec75501f1786caf55e03c">Setting the email's width<a name="bs-ue-jumpmark-492e8d3a29488f1794ec378828ac06bd"></a></span>

 We added a class named `container` to the `<table>` which contains the content of the email. Than we set a CSS rule for that in the mobile CSS section (inside the `@media` query) and made it 320 pixels wide. 
    div[class="yfix"] .container { width: 320px !important; }

 And later it is inserted in the ``: 
    <table cellspacing="0" cellpadding="0" border="0" width="600" class="container">

### Showing and Hiding Sections

 You can add a `mobile_hidden` CSS class to apply to elements that you want to hide for mobile users. 
    <p class=”mobile_hidden”>This is hidden from mobiles</p>

### Mobile Formatting

 You can override the desktop appearance of the message by adding a rule to the mobile CSS section. Generally you can override any style there. #### Font size and formatting

 
    div[class="yfix"] p {
      font-size: 14px;   /* Bigger text */
      color: blue;       /* Changing color /
      text-align: left;  /* Always align paragraph to left */
      line-height: 20px; /* Define the height of the lines */
    }

#### Links

 
    div[class="yfix"] a {
      border: 1px solid blue;
      background: silver;
      color: #fff;
      font-size: 16px;
      text-decoration: none;
    }

#### Image Resizing

- Add `id="my_image"` to the referenced `<img>` tag, to apply the changes.
 

    div[class="yfix"] #my_image {
      width: 320px !important;
      height: 120px !important;
    }

#### Replacing Images

 To replace an image in the mobile version, you have to add an id attribute to the image in the content. In the sample template we gave it "header_image" and we added a CSS style to the mobile CSS section: 
    div[class="yfix"] #header_image {
      content: url(http://example.com/path/to/mobile/image.jpg);
      width: 320px !important;=
      height: 100px !important;
    }

 Here we defined new URL with the content rule which allows you to override the dimension of the image. {{Note|Text=Start the selector with `div[class="yfix"]` to prevent Yahoo! Mail applying mobile CSS to desktop content. Due to the way some mobile clients work, it is always a best practice to apply the `!important` flag to the dimension rules (width and height). Later in the `` section add the id attribute to the `<img>`: 
    <img src="http://example.com/image.jpg" alt="" width="600" height="120" id="header_image">

Mail Client Specific Bugs, Restrictions and Issues
--------------------------------------------------

 Below is a list of issues that have been experienced when testing individual mail clients, but could be used as a general Best Practice guideline. - Never use comments in `<style>` tags because **Yahoo! Mail** will handle them incorrectly.
- **GMail** will strip out all inline style rules that it doesn’t recognize unless you specify them as `!important`.
- In **Hotmail**, you can't use conditional comments in the `` section. Everything after a conditional comment is stripped out and your email will be broken.
- Some issues that affect **Android** built-in Mail clients can be worked around by using a `<meta name="viewport">` tag (as you can see in the code example) and by leaving the `` tag without any attributes.
- You can force **Outlook** to provide a "view in browser" button by adding:
 

    #outlook a { padding: 0; }

- If a gap appears in tables in **Outlook 2007/2010**, you can remove it with:
 

    table { border-collapse: collapse; mso-table-lspace: 0pt; mso-table-rspace: 0pt; border: 0; }
    table td { border-collapse: collapse; }

- To force **Hotmail** to display emails at full width, add:
 

    body { width: 100% !important; }
    .ReadMsgBody { width: 100%; }

- To force **Hotmail** to display normal line spacing, add:
 

    .ExternalClass,
    .ExternalClass p,
    .ExternalClass span,
    .ExternalClass font,
    .ExternalClass td,
    .ExternalClass div { line-height: 100%; }

 <dl><dd>You can read more on that at: <http://www.emailonacid.com/forum/viewthread/43/></dd></dl>- To stop **Hotmail** from breaking the email with oversized emoji, add:
 

    .ExternalClass img[class=Emoji] {
      width: 10px !important;
      height: 10px !important;
      display: inline !important;
    }

- To force the **WebKit** rendering engine to float tables, add:
 

    @media screen and (-webkit-min-device-pixel-ratio: 0) {
      table[class*="sectiongroup"] td[align="center"] {
        text-align: center !important;
      }
      table[class*="sectiongroup"] table.section td[align="center"] {
        text-align: -webkit-center !important;
      }
    }

 To prevent **WebKit** and **Windows Mobile** platforms from changing default font sizes, add: 
    body { margin: 0; padding: 0; -webkit-text-size-adjust: none; -ms-text-size-adjust: none; }
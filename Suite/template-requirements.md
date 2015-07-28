---
title: 'CMS Template Requirements'
tags: Suite
old_url: 'http://emarsys.dev/suite/content/cms/template-requirements/'
---

Introduction
------------

 The email templates used in Emarsys eMarketing Suite are a fast and efficient way for you to create great-looking and effective email campaigns. Based on your designs, these templates are created with a variety of content, ranging from hard-coded elements such as headers or footers, to standard pre-formatted sections and finally to free areas available for complex editing in Advanced Mode. Emarsys templates are constructed within a framework which is designed to ensure your emails are displayed properly in all standard mail clients, be they web-based, desktop or mobile. The requirements for this framework are listed in this document. All email designs must be compliant with this document before they will be accepted by the Emarsys Web Development team. This document is intended to give you an insight into the template framework, as well as explain the reason for some of the limitations, to ensure that your designs are suitable right from the start. Some deliverability considerations are also included. If you have any questions regarding template design, the Emarsys Strategic Consultants will be happy to advise you.

### Message

 Before you start to think about the look and feel of your template, make sure that you are absolutely clear what the message of the email will be. This will have a knock-on effect for the rest of the decisions you make. Questions to consider: Your campaign is a direct channel from you to the inbox of your customers; does it reflect your corporate CI and represent your brand? Does the overall layout fit your industry sector? Is this a seasonal campaign (such as Christmas Sales), a one-off (such as a welcome email), or a recurring one which will need regular content changes?

Preview Pane Elements
---------------------

 You have a key area of 2-3 inches (5-8 cm). In this very limited space, the added value, your corporate branding and editorial/personalization should be visible, even without the images being displayed. If nothing valuable is shown here, try to improve the design. Have a look at some best-practice examples if you need ideas. For very large emails, you should consider using a table of contents (TOC). Ask the Emarsys Consultants to explain how this can affect template’s behavior. For language versions, translation must be included:

- Please specify clearly which texts need to be translated.
- In addition to the creative artwork files, please also send us a table with all the translated strings.

### PSD File for Template Setup Requirements

 So that we can create your new CMS template we recommend that you create a mock-up in Photoshop, and then send Emarsys Support the .PSD file. It is important that you do not rasterize any fonts or shapes, or merge/flatten any layers in the .PSD file. The following information is required in addition to the .PSD file itself:

- Total width of the design (not exceeding 600 – 650px)
- Desired vertical and horizontal line spacing (in pixels) between: - Lines
- Images
- Texts
- Maximum image heights and widths
- Font type to use (no custom or non-web fonts)
- Desired font colour as hex code (e.g. #dd15as)
- Desired font size in pixels

 If you have any additional requirements such as hard-coded groups, URLs for fixed links in the navigation, etc. then please include in them as well.

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">Due to the way the images work, there can be no overlap in the CMS Template, so please make sure that images in your PSD are carefully placed side by side.</td></tr></tbody></table>### Images

- Since the Emarsys template framework does not use layers, images can not overlap. Be careful to place images side-by-side.

#### Background Images

 Background images should be avoided, since some email clients do not (or at least not fully) display them (e.g. Outlook 2007, 2010). However, exceptions can be made if you need to display text over an image (e.g. for a banner).

<div class="center"><div class="floatnone">[![CMS tmpl Page 06 Image 0002.png](/assets/images/CMS_tmpl_Page_06_Image_0002.png)](/assets/images/CMS_tmpl_Page_06_Image_0002.png)</div></div>### Text

- Define the pre-header element to use (text group with or without link)

#### Headings

 In the case that no heading is required, the whole heading (or even parts of it) can be hidden. Also, headings or parts of them can be linked.

<div class="center"><div class="floatnone">[![CMS tmpl Page 06 Image 0003.png](/assets/images/CMS_tmpl_Page_06_Image_0003.png)](/assets/images/CMS_tmpl_Page_06_Image_0003.png)</div></div>#### Line Height

 Try to avoid the use of defined line heights. These are not (or only partly) displayed in some email clients (e.g. Hotmail, Outlook). These clients will display the line height too large, breaking your layout. If you need to use defined line heights, leave some extra space in the design to ensure that sections are displayed correctly.

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px solid #999;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">This mostly applies to sections that have a border and to multi-column groups that should have balanced lengths (see Multi-Column Groups below).</td></tr></tbody></table><div class="center"><div class="floatnone">[![CMS tmpl Page 07 Image 0002.png](/assets/images/CMS_tmpl_Page_07_Image_0002.png)](/assets/images/CMS_tmpl_Page_07_Image_0002.png)</div></div>#### Bullet Lists

 If you want to use bullet lists, these are only available in Advanced Mode, and no special icons or list styles can be used (i.e. only black discs are possible), since special list styles do not work with all email clients.

### Group Design

 For each group, specify:

- Heading
- Body Text
- Image
- Link

<div class="center"><div class="floatnone">[![CMS tmpl Page 07 Image 0003.png](/assets/images/CMS_tmpl_Page_07_Image_0003.png)](/assets/images/CMS_tmpl_Page_07_Image_0003.png)</div></div>#### Multi-Column Groups

 If you need two or more columns in your template, bear in mind that the width has to be the same for all sections. A section cannot have 200 px, and then later 202 px. Also, spaces between sections must be identical.

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px solid #999;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon AdditionalInfo.png](/assets/images/Icon_AdditionalInfo.png)](/assets/images/Icon_AdditionalInfo.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">Example: 2-col group with overall template width of 600 px.600 px-20 px = 580 px/2 columns = 290 px per column.If you want all columns to be of equal height (i.e. to be balanced), you can use a minimal height for this section. If more content is entered, the section will still increase its height.</td></tr></tbody></table> Use symmetric columns whenever possible:

<div class="center"><div class="floatnone">[![CMS tmpl Page 08 Image 0002.png](/assets/images/CMS_tmpl_Page_08_Image_0002.png)](/assets/images/CMS_tmpl_Page_08_Image_0002.png)</div> </div><table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">When using mobile templates, the spacing between the individual elements needs to be > 2px, since floating tables are used.When using borders in multi-column groups:The groups are independent of each other, so minimal heights have to be used. Consider the line spacing and spacing between the elements.</td></tr></tbody></table>#### 1/3 and 2/3 Groups

 We recommend avoiding combinations of ⅓ and ⅔ content layouts, instead group content with a symmetric width, e.g. 50% each in a two-column layout. ⅔ groups are not flexible and need to be hard-coded into the template and have their position defined, e.g. at the top or bottom of a template. Sections with varying width cannot be used as flexibly as those with an equal width, and also cannot be defined on a group basis. The same applies to the Main Content and Side Section, or groups where the framework has to be hard-coded into the template.

Requirements for Sending Emails via Emarsys
-------------------------------------------

 Emarsys has implemented a strict rule set to ensure a healthy sending environment for all its clients. These requirements and guidelines will help you to increase your email deliverability. Besides keeping your campaigns away from that Spam folder, they help you to directly and dramatically increase your click and open rates.

### Legal Requirements (Compulsory)

 All Emarsys clients must be aware of, and comply with, applicable law and the regulations of the individual countries involved; the latter may include:

- The ***Directive on Privacy and Electronic Communication 2002/58/EU*** of the European Parliament and Council from July 12th, 2002, concerning the processing of personal data and the protection of privacy in the electronic communications sector
- The ***Directive on Electronic Commerce (2000/31/EC)*** of the European Parliament and Council from June 8, 2000, on the legal aspects of information society services, in particular, electronic commerce in the internal market
- The ***US CAN SPAM Act of 2003*** (Controlling the Assault of Non-Solicited Pornography and Marketing Act)

 The following legal requirements are absolutely necessary:

- *Unsubscribe link* is present and clearly visible
- *Link to privacy policy* is included, containing: - Information about how to unsubscribe (e.g. 1-click-unsubscribe)
- Physically summonable address
- Company email address
- Company phone number
- *Physically summonable company address* included in the footer

 Furthermore, the following are additional legal requirements in some markets:

- Copyrights/Trademarks are included
- Link to imprint (with name of CEO) We recommend including the following information in the imprint, even though some aspects are already covered by the privacy policy: - Company name is stated, together with
- Company email address
- Company URL
- Company phone number
- Authorised representative(s)
- Commercial registration and tax number information

### Emarsys Deliverability Standards (Best Practices)

 The high level of deliverability which you enjoy with Emarsys is partly due to our reputation as an email sender, which in turn reflects the behavior of all our customers. Therefore, even though you are not obliged to follow the Emarsys standards, we strongly advise you to implement them as they will not only improve you click and open rates, but help to maintain the Emarsys reputation as well. Consider adding a line like "Add sender to address book". This will ensure that images will be displayed, but will also increase open rates. Also, this information is tracked by email providers, so Emarsys' reputation will increase with this provider. Include a brief editorial and use personalization where possible, for example, mention the recipient's name, have short greeting line, etc. Explain to your recipients why they are receiving this message, how often you send it, and allow them to change their settings for receiving messages from you). Have a look at your image-to-text ratio, i.e., how many pictures are included in the HTML version, compared to text? If this is too high, your campaign might be considered as spam by the email providers. Here is a brief overview of items to check:

- Font size between 11 px – 19 px (8 pt - 14 pt)
- No Flash or Rich Media embedded
- Minimal use of red fonts (even if CI is red!)
- No JavaScript used
- No forms embedded in campaign

Addons, Forms & User-Generated Content
--------------------------------------

 Addon texts are hardcoded into the template, and will not change when switching the email language; these would require a separate template for each language. The Addons "Contact Us" and "Change Profile" can only be used when a contact form has been created. Please discuss with Emarsys Support if the Emarsys social network sharing functionality should be used – if so, certain placeholders need to be included in the design. You will also need to specify if Emarsys standard icons shall be used, or if you will provide your own icon set. When discussing the design, all possible icon placements (template, sections) should be discussed.

### Links

 In Standard Mode, only one link is permitted. Further links can be added in Advanced Mode. You can specify different designs for each mode. Your link designs should match the overall design.

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">In Advanced Mode we recommend not to use images in the link design, as this limits the possibilities for linking text (the image will disrupt the text block). Be careful with link formatting, since they might not appear as intended with some email clients (e.g., Outlook).</td></tr></tbody></table> The link to the right shows how Outlook would format it:

<div class="center"><div class="floatnone">[![CMS tmpl Page 10 Image 0002.png](/assets/images/CMS_tmpl_Page_10_Image_0002.png)](/assets/images/CMS_tmpl_Page_10_Image_0002.png)</div></div> "View online version" links: If the default link and default text is used for the online version, changing the email language will change the language of the links. If the online link is hardcoded into the template, this cannot be changed. Also keep in mind that links which are hardcoded into the template cannot always be tracked. Contact Emarsys Support if you have any questions in this regard.

Ecommerce (if applicable)
-------------------------

 Here is a short list of items to check:

- Link to Secure Shopping Info included?
- Link to applying terms and conditions included?
- Link to payment methods included?
- Link to iPhone/Android App download included?
- Link to Shipping Information included?
- Link to info on return policy included?
- Info on Customer Service Hotline phone number included?
- Info on Customer Service Hotline email address included?
- Info on Customer Service Hotline contact hours included?

Suite-Specific Template Requirements
------------------------------------

### Standard Mode

 The Suite templates are constructed to enable you to create new email campaigns with the minimum of effort. The functionality available in Standard mode is based on the idea that no sections have more than one image, one link and no more than one form link. For body text, only one font style is possible (e.g., Verdana, Regular, black, 12pt). Use the Standard Mode to specify…

- Section Heading
- Body text
- Images
- Links
- Form Links

<div class="center"><div class="floatnone">[![CMS tmpl Page 11 Image 0002.png](/assets/images/CMS_tmpl_Page_11_Image_0002.png)](/assets/images/CMS_tmpl_Page_11_Image_0002.png)</div></div>### Advanced Mode

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/Icon_BeCareful.png)](/assets/images/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">Emarsys cannot guarantee that changes made in the Advanced Mode are displayed correctly in all email clients, even if "Browse Preview" looks fine.Since the Advanced Mode splits the source code into two versions (HTML/Text), you need to make all changes *twice*, once in HTML, and once more in the Text tab.</td></tr></tbody></table>- Click **Advanced Mode** in Standard Mode to switch editing modes:

<div class="center"><div class="floatnone" style="padding-top: 20px;">[![CMS tmpl Page 12 Image 0002.png](/assets/images/CMS_tmpl_Page_12_Image_0002.png)](/assets/images/CMS_tmpl_Page_12_Image_0002.png)</div></div> Use the Advanced Mode to specify…

- Section Heading
- Body text
- Multiple images
- Multiple links
- Form Links

<div class="center"><div class="floatnone">[![CMS tmpl Page 12 Image 0003.png](/assets/images/CMS_tmpl_Page_12_Image_0003.png)](/assets/images/CMS_tmpl_Page_12_Image_0003.png)</div></div> Please be aware that line breaks entered in Advanced Mode are encoded via "Shift+Enter". If you start new *paragraphs* (pressing Enter), your layout will break. Different headings must be separated by "ǀ" (pipe character), e.g. Heading1ǀHeading2ǀHeading3ǀ… . Ensure that you do not use more than one URL per section.
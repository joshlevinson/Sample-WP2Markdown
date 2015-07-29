---
title: 'Guidelines for HTML Email'
subject: 'Suite, SuiteContent'
old_url: 'http://emarsys.dev/suite/content/cms/html-guidelines/'
---

Introduction
------------

 The purpose of this document is to outline Best Practices for content design and coding for HTML email. Many of these rules are simply a matter of adhering to HTML 3.2 specification. We have written these rules down for your convenience and subsequent referral so that the production of your email campaign will proceed as smoothly as possible from a production standpoint. Developing HTML for email requires more precision and adherence to guidelines than developing content for websites. The following is a list of guidelines that should be followed in writing HTML email templates along with examples of good and bad code. Sometimes HTML code renders differently on different web browsers. To make sure you are using code that is not dependent on browser-specific tags, before saving content in Emarsys, check your template on the latest versions of Microsoft Internet Explorer, Firefox, and Safari. Also, if your company uses a non-standard email client, please check the HTML code on that platform as well. Emarsys can provide platform testing on Outlook 2003, 2007, 2010 & Outlook Web Access, Apple Mail, Mozilla Thunderbird, AOL 9 (PC & MAC) as well as Hotmail, Yahoo, Gmail, AOL Webmail (AIM) and other local email clients. Layout
------

### Maximum Width Enclosing Email Content

 Some email clients and/or hardware configurations can only show 600 pixels of width at one time. An HTML email without any set width may look good on Outlook Express on a high resolution monitor, but low-end users will not be able see the entire width of the email. The recommended maximum width of all emails is 600 pixels wide. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <table width="600" align="left">
      <tr>
        <td>[…contents of email…]</td>
      </tr>
    </table>

 </td> <td> 
    […contents of email…] or
    <table align="left">
      <tr>
        <td>[…contents of email…]</td>
      </tr>
    </table>

 </td></tr></tbody></table>### Tags with Limited Support

 HTML 4/5 tags, CSS, JavaScript, Animated Gifs, Forms, and Flash are only supported by a limited number of browsers and email clients and are NOT recommended for HTML emails. They will likely cause errors in many email clients and hence should only be used when you have already discussed the ramifications with your AM. ### CSS

- Inline CSS is supported, but is limited to the use of font styles and size.
- For the use of colour, the six-digit-hexadecimal colour should be referenced.
- CSS should not be used for positioning.
- Use of external style sheets is not supported.
- Using CSS to reference background images is not supported:
- Example: `background:#e76f00 url(im/btn_orange.gif) repeat-x center center`

### Quick Tips

- Do not use ``, `<meta>` or `<title>` tags.
- Do not use `<div>`, `<tbody>` or `<p>` tags.
- Do not use `<embed>` tags.
- Do not include attributes with `` tags.
- Use `<b>` and `<i>` instead of `<strong>` and `<em>`.
- Always close tags.
- JavaScript tends to be stripped out or ignored in most email browsers.
- Do not use `GENERATOR` tags in the `HEAD` of the message such as `META` tags.
 
<table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <tr>
      <td align="left">
        <font face="verdana, arial, sans-serif">Text goes here.</font>
      </td>
    </tr>

 </td> <td> 
    <div align="left" style="font-family: verdana;">Text goes here.</div>

 </td></tr></tbody></table>### The <Body> Tag

 Some email clients, such as Yahoo and Hotmail strip out or modify the `body` tag in emails. You should not include any attributes in the `body` tag that you don’t mind not being displayed, since they may not be rendered. If you are using light text on a dark background, be sure to set values such as background colour in the `bgcolor` attribute of the `table` tag. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <table bgcolor="#ffffff" width="600">
      <tr>
        <td align="left">[…contents of email…]</td>
      </tr>
    </table>

 </td> <td> 
    <body bgcolor="#ffffff">
      […contents of email…]
    

 </td></tr></tbody></table>### WYSIWYG Editors

 WYSIWYG (What You See Is What You Get) editors often automatically create browser-specific or otherwise non-standard HTML code. If using a WYSIWYG editor, please remove browser-specific or other non-standard HTML coding and review the code in a program such as Notepad or Dreamweaver to make sure that it meets our guidelines. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    
      
        <center><br>
          <table bordercolor="#333366"
          cellspacing="0" cellpadding="0"
          width="730" align="center"
          bgcolor="#ffffff" border="8">
            <tr>
            …

 </td> <td> 
    
    
      
        <title>HTML Codes - Table of
        ascii characters and symbols</title>
        <META http-equiv=Content-Type
        content="text/html; charset=windows-1252">
        <META http-equiv=PICS-Label
        content='(PICS-1.1
        "http://www.rsac.org/ratingsv01.html"
    
        l gen true for "http://www.ascii.cl" r (n
        0 s 0 v 0 l 0))'><link
        href="HTML Codes - Table of ascii
        characters and symbols_files/ascii.css"
        type=text/css rel=stylesheet>
        <META content=all name=robots>
        <META content=Global name=distribution>
        <META http-equiv=Content-Script-Type
        content=text/javascript>
        <META http-equiv=reply-to
        content=webmaster@10sites.com>
        <META content="MSHTML 6.00.2600.0"
        name=GENERATOR>
        <body text=#333366 vLink=#3300cc
        aLink=#cc0033 link=#cc0033
        bgColor=#ffffff>
          <center><br>
          <table bordercolor=#333366
          cellspacing=0 cellpadding=10 width=730
          align=center
          bgcolor=#ffffff border=8>
            <tbody>
              <tr>
                …

 </td></tr></tbody></table>### Syntax

 All attribute values must be defined with double quotes and use the proper syntax such as "#" before color attributes and ";" after style elements. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <td align="center" bgcolor="#000000"
    valign="middle">

 </td> <td> 
    <td align=center bgcolor=000000
    valign=middle>

 </td></tr></tbody></table>### Special Characters

 Many email clients are unable to correctly render raw 8 Bit characters. Consequently, you must encode them with their corresponding numeric entities (ASCII Character Codes). For example, the HTML entity for the copyright symbol is `©` <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    Copyright © 2014 Emarsys.

 </td> <td> 
    Copyright © 2014 Emarsys.

 </td></tr></tbody></table>### Image Maps

 Image Mapping is when you redefine the area that is linked within an image. This is performed with the `<map>` HTML tag. Moreover, when using Image Maps, ensure that each separate map is contained within its own `<td>`. When multiple maps are entered in the same `<td>` issues occur in some platforms; currently Apple Mail and Outlook 2007. Image Maps are an excellent design technique to achieve a visually pleasing marketing message, but only when used correctly. ### Encoding

 The optimum encoding for email in most languages is UTF-8. UTF-8 is widely supported, and with the exception of some multi-byte languages, should be the default encoding for creative assets. Table Content
-------------

 Some browsers and email programs can have problems with content that exists outside of `<td>` tags. Make sure that all content for the email sits within the table cell tags (`<td>`s). Make sure all `<td>`s have a width assigned and that the width is not "0". <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <table bgcolor="#ffffff" width="250"> 
      <tr>
        <td width="200">
          Here is some text.<br />
          <img src="images/spacer.gif" 
          width="200" height="12" vspace=”0“ 
          hspace=”0” border="0" 
          style="display:block;"><br />
          Here is some more text.
        </td>
      </tr>
    </table>

 </td> <td> 
    <table bgcolor="#ffffff" width="250">
      Here is some text.<br />
      <tr>
        <td width="200">
          <img src="images/spacer.gif" width="200"
          height="12" border="0"><br />
          Here is some more text.<br />
        </td>
      </tr>
    </table>

 </td></tr></tbody></table>### ROWSPAN and COLSPAN

 Keep the use of rowspan and colspan to a minimum since they limit template flexibility. In some cases, options such as nesting a `<table>` within another `<table>` cell offer a better solution. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <table border="0" cellpadding="0"
    cellspacing="0" width="130">
      <tr>
        <td width="130">
          <img height="20" width="130" vspace=”0“ hspace=”0”
          src="magnolia.gif" border="0"
          style="display:block;">
        </td>
      </tr>
      <tr>
        <td width="130">
          <table border="0" cellpadding="0"
          cellspacing="0" width="130">
            <tr>
              <td width="60">
                <img height="1" width="60"
                src="magnolia.gif" border="0">
              </td>
              <td width="70">
                <img height="1" width="70"
                src="magnolia.gif" border="0">
              </td>
            </tr>
            <tr>
              <td width="60" valign="top">text goes
              here</td>
              <td width="70">
                <table border="0" cellpadding="0"
                cellspacing="0" width="23">
                  <tr>
                    <td width="70" valign="top">
                    Text goes here</td>
                  </tr>
                  <tr>
                    <td width="70" valign="top">
                    Text goes here</td>
                  </tr>
                </table>
              </td>
            </tr>
          </table>
        </td>
      </tr>
    </table>

 </td> <td> 
    <table border="0" cellpadding="0"
    cellspacing="0" width="130">
      <tr>
        <td colspan="2">
          <img height="20" width="130" src="magnolia.gif"
          border="0">
        </td>
      </tr>
      <tr>
        <td width="60" rowspan="2"
        valign="top">Text goes here</td>
        <td width="70">Text goes here</td>
      </tr>
      <tr>
        <td width="70">Text goes
        here</td>
      </tr>
    </table>

 </td></tr></tbody></table>### Widths and Heights

 Setting an exact width in all table elements adds stability to your design and will more likely render consistency across email clients and can make the email render faster. Avoid using percentages. Make sure all columns have a width assigned and that the width is not "0". Making sure columns have a set pixel width helps to ensure table structure. Also do not mix percentage widths with pixel width when defining column widths. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <td width="250" height="100">
      <img src="logo.gif" width="250"
      height="100" vspace=”0“ hspace=”0”
      alt="Company Name" border="0"
      style="display:block;"/>
    </td>

 </td> <td> 
    <td width="100%">
      <img src="logo.gif"/>
    </td>

 </td></tr></tbody></table>### Empty Table Cells

 Older browsers have problems with empty Table cells (`<td>`s). Make sure to put something in every table cell. A 1×1 transparent image inserted into the empty table cell solves this issue. Do not use ` ` as a filler. Other empty tags can also be an issue. Once a design is completed it is always a good idea to review and clean up the code to avoid any problems down the line. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <td width="200">
      <img src="images/spacer.gif" width="200"
      height="1" vspace=”0“ hspace=”0” border="0"
      style="display:block;"/>
    </td>

 </td> <td> 
    <td width="200"> </td>
    - OR -
    <td width="200"></td>

 </td></tr></tbody></table>### Vertical Text Spacing

`<p>` tags render inconsistently across emails, frequently adding more or less space than desired. Setting the amount of white space with a `"spacer.gif"` image will set the spacing to an exact value and achieves a more consistent end-user experience. For large amounts of text, use `<br />` tags to achieve spacing between blocks of text. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <tr>
      <td width="200">Here is some text.<br>
        <img src="images/spacer.gif"
        width="200" height="12" vspace=”0“
        hspace=”0” border="0" style="display:block;"><br />
        Here is some more text.
      </td>
    </tr>

 </td> <td> 
    <p>Here is some text.<p/>
    <p>Here is some more text.</p>

 </td></tr></tbody></table>### Spacing Between Elements

 To achieve spacing between elements avoid using `cellpadding`, `cellspacing` or `margin padding` as they are not universally supported. Instead use transparent gifs within a table structure for more precision. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <tr>
      <td width="200" height="10">
        <img src="images/spacer.gif" width="10"
        height="10" vspace=”0“ hspace=”0”
        border="0" style="display:block;">
      </td>
    </tr>
    <tr>
      <td width="200">Here is some
      text.
      </td>
    </tr>

 </td> <td> 
    <tr>
      <td width="200" style="margin-top:
      10px;">Here is some text.</td>
    </td>
    - or -
    <table width="640" cellspacing="10"
    cellpadding="2">

 </td></tr></tbody></table>### Table Stability

 When design allows, it is recommended to build a "cement" row to guarantee a table remains to its exact width. In the first row of a table, create a series of 1 pixel high, transparent `"spacer.gif"` images with the appropriate widths for each cell. While this is not a necessity, it will decrease the chance of an unforeseen table error. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <table bgcolor="#ffffff" width="250">
      <tr>
        <td width="10">
          <img src="images/spacer.gif" width="10"
          height="1" vspace=”0“ hspace=”0”
          border="0" style="display:block;">
        </td>
        <td width="200">
          <img src="images/spacer.gif" width="200"
          height="1" border="0">
        </td>
        <td width="40">
          <img src="images/spacer.gif" width="40"
          height="1" border="0">
        </td>
      </tr>
      <tr>
        <td width="10">
          <img src="images/spacer.gif" width="10"
          height="1" border="0">
        </td>
        <td width="200">Text goes here</td>
        <td width="40">
          <img src="images/spacer.gif" width="40"
          height="1" border="0">
        </td>
      </tr>
    </table>

 </td> <td> 
    <table bgcolor="#ffffff" width="250">
      <tr>
        <td width="10"><br /></td>
        <td>Text goes here</td>
        <td width="40"><br /></td>
      </tr>
    </table>

 </td></tr></tbody></table>### Background Color

 Certain email software packages strip out values appearing in the body tag; setting the colour in the table ensure colour settings will appear consistently. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <td bgcolor="#9c7bbd">

 </td> <td> 
    <body bgcolor="#9c7bbd">

 </td></tr></tbody></table>### Alignment

 Setting alignment value in table elements adds stability as default values may not render properly in all email clients. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <table width="600" align="center">
      <tr>
        <td align="left" valign="top"
        width="600">Text goes here</td>
      </tr>
    </table>

 </td> <td> 
    <table>
      <tr>
        <td>Text goes here</td>
      </tr>
    </table>

 </td></tr></tbody></table>Tag Formatting
--------------

### Closing Tags

 All tags must be matching pairs, opening and closing. Validate your code. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <font face="arial, helvetica,
    verdana">click here!</font>
    <font face="times, garamond">For your
    shopping needs</font>

 </td> <td> 
    <font face="arial, helvetica,
    verdana">click here!…
    <font face="times, garamond">For your
    shopping needs…

 </td></tr></tbody></table>### Tag Case

 All attributes must be either uppercase or lowercase. Do not mix both. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <b>say something bold</b>

 </td> <td> 
    <b>say something bold</B>

 </td></tr></tbody></table>### Tag Nesting

 Make sure that all tags are nested properly (i.e. if multiple tags are used, they will need to be closed in the proper order). <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <i>
      <b>say something bold and exciting</b>
    </i>

 </td> <td> 
    <i>
      <b>say something bold and exciting
      </i>
    </b>

 </td></tr></tbody></table>### Quoting Values

 All attribute values must be defined with double quotes. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <td align="center" bgcolor="#000000" valign="middle">

 </td> <td> 
    <td align=center bgcolor=#000000
    valign=middle>

 </td></tr></tbody></table>### Font Face and Size

 Not all users have every font in their system; specifying multiple fonts allows you to choose the fonts you'd prefer the user to see. If the specified fonts or font types are not found, text will render in the user's default font. Standard Fonts sizes (1, 2, 3…) will look quite different between different browsers and email platforms. emarsys suggests a workaround using an inline style tag as well, with a size defined in pixels for a more consistent look. `style="font-size:12px;"` <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <font face="arial, helvetica, 
    sans-serif" style="font-size:12px;"
    size="2">email</font>

 </td> <td> 
    <font face="arial" size="2">email</font>

 </td></tr></tbody></table>### Defining Colors

 Hexadecimal values guarantee consistent and true colour values. Some older browsers do not recognize named values or display them differently than others. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <font color="#7bc618">email</font>

 </td> <td> 
    <font color="green">email</font>

 </td></tr></tbody></table>Images
------

### Size

 The best practice is to keep an email size under a total of 49 kB or longer download times will be experienced and messages will have lower response rates. Only .jpg and .gif image formats should be used for HTML, .png files are NOT supported by all email browsers. Email content and images should be optimized to the minimum file size. The combined size of image files referenced should not exceed 500 kB. ### Border

 Images that are linked and do not have the `border` attribute set to zero will display a bold blue line around the edges, which doesn't look very good with some templates and can throw off the table structure. Make sure to set `border="0"` for all images to prevent this. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <img src="image.gif" width="1"
    height="1" vspace=”0“ hspace=”0”
    alt="Descriptive text here" border="0"
    style="display:block;">

 </td> <td> 
    <img src="image.gif" width="1"
    height="1" alt="Text here">

 </td></tr></tbody></table>### Height and Width

 Always include `height` and `width` attributes for all images. Designating the size attributes for an image will affect the time it takes for an email to download. If no `height` or `width` attributes are set for an image, the image must fully download before the email client's HTML interpreter can render the rest of the page. For optimum download speed, set the `height` and `width` attributes of all images to absolute values (rather than percentages). Images should be used at their actual size. Resizing an imaging using HTML properties will be ignored in email clients such as Outlook 2007 and will likely cause errors in the table’s structure. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <img src="image.gif" width="10"
    height="10" vspace=”0“ hspace=”0”
    alt="text here" border="0"
    style="display:block;">

 </td> <td> 
    <img src="image.gif" alt="Text here" border="0">
    - or -
    <img src="image.gif" width="50%"
    height="50%" alt="Text here" border="0">

 </td></tr></tbody></table>### Alternate Text

 When viewing HTML emails while offline, users will see a broken image or image placeholder rather than the image intended in online viewing. To make the email easier to view, be sure to enter a description of the image in the `alt` tag. Please make the `alt` tag description something that the recipient would understand (i.e. "Flowers only £9.99" instead of "flower image 22"). <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <img src=”headline1.gif” width=”1”
    height=”1” vspace=”0“ hspace=”0”
    alt=”Save today on Airline tickets!”
    border=”0” style=”display:block;”>

 </td> <td> 
    <img src=”image.gif” width=”1”
    height=”1” border=”0”>

 </td></tr></tbody></table>### Image Naming

 To make the email integration process go more smoothly, it is desirable to have images that are intuitively named. Please use one word, lowercase names, with no underscores, for all images (Some browsers do not render images with underscores). <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <img src=”magnolia.gif” width=”50”
    height=”50” vspace=”0“ hspace=”0”
    alt=”Magnolia Bouquet” border=”0”
    style=”display:block;”>

 </td> <td> 
    <img src="image.gif” width="50"
    height=”50” border=”0”>

 </td></tr></tbody></table>### Images in Hotmail viewed in Firefox

 When viewing HTML emails in Hotmail, with the Firefox browser, users will see a broken image with spacing above and below the image. Although email messages might look fine in Internet Explorer, Hotmail adds spacing equal to the height of one line of text, to each image only in Firefox. With Firefox gaining more and more browser market share, fixing this is important. To make the email easier to view, be sure to code with all images as separated as possible from font. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <td><img src=xxx/></td>

 </td> <td> 
    <td>
      <img src=xxx/>
      <font>To receive email to your inbox, 
      add xxx to your address book.</font>
    </td>

 </td> </tr></tbody></table> Here is an example of how we add a work-around inline style code to make it more Firefox/Hotmail friendly: Original code: 
    <td><img src=xxx/></td>

 Transformed code: 
    <td style=”font-size:0px; line-height:0px;”><img src=xxx/></td>

 → This type of inline style will force Hotmail to render the images correctly. ### Default Blocking of Images by Various ISPs

 For the most part, there is not much that can be done coding-wise to combat the issue of ISPs that block images by default. We suggest incorporating the following best practices: - Provide informative alt-tags for images so that those will be displayed should the images be blocked
- Use a clean layout/template for effective email degradation
- Place "Add-to-Address book" verbiage at the top of emails for Welcome messages or "Having trouble viewing this email" link in other emails

### Animated GIFs

 Many of our customers do make the use of animated GIFs, however close attention to file size must be given as animated GIFs can become file size heavy and effect download time. Also some browsers such as Outlook 2007 do not render them properly and will only display the first frame of the GIF. Thus, the first frame should be relevant enough to work in the message. ### Background Images

 Background images are not universally supported in all email clients, such as Outlook 2007. It is recommended that background images not be used at all for HTML emails but if they are incorporated within a design they should be used in such a way that if they do not appear it does not greatly affect the design or hamper the intent of the displayed message. If text is displayed on top of a background image, it is good practice to also fill the cell with a background colour which will appear when the image does not. Another workaround is to simply create an image that includes the background and text and place this within the table cell. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <td background=”images/red_pattern.gif”
    bgcolor=”#ff0000”> Hurry! Sale Ends
    Saturday!</td>
    - or -
    <td width="100" height="50">
      <img src="sale.gif" width="100"
      height="50" vspace=”0“ hspace=”0”
      alt="Hurry! Sale ends Saturday!"
      border="0" style="display:block;"/>
    </td>

 </td> <td> 
    <td background="images/red_pattern.gif">
      Here is some text.</td>

 </td></tr></tbody></table>### Style Use in Image Tags

 When using image tags it is important to use styles correctly and include user friendly alternative descriptions of the image in case it is not displayed correctly by using `alt=` for the text. In addition when using non-floating images you should always include the display:block style in images to ensure that there are no gaps after the image, or other alignment issues. Finally when linking to your images you should always make sure that you use absolute paths, and not relative paths. <table class="wikitable"><thead><tr><th>Good ✔</th> <th>Bad ×</th> </tr></thead><tbody><tr><td> 
    <img 
    src="http:/www.site.com/headline1.gif" 
    width="100" height="50" vspace="0" 
    hspace="0" alt="Save today on Airline 
    tickets!" border="0" 
    style="display:block; font-family: 
    arial, sans-serif; font-size:20px; 
    font-weight:bold; color:#000000;">

 </td> <td> 
    <img
    src="http:/www.site.com/headline1.gif"
    width="100" height="50" vspace="0"
    hspace="0" alt="Save today on Airline
    tickets!" border="0">

 </td></tr></tbody></table>Special Considerations
----------------------

 Integration for Lotus Notes can be very tedious and stressful. The easiest and most efficient way to have "Lotus-friendly" HTML is to prepare for integration before jumping into it. Use the included tips in the following sections when creating HTML email for Lotus Notes specifically. Please keep in mind that Lotus Notes makes up a very small portion of all email readers in the market today. Remember, if something won’t work or you're having too much trouble getting it to work, feel free to contact your Emarsys account team for additional troubleshooting and insight. ### Creating a Template

 Follow these steps to create a template: 1. Draw the layout of the email on a piece of paper. This helps to visualize the overall structure before looking at the details.
2. Still working on paper, separate sections that look like they should be in their own table.
3. Open your WYSIWYG program (e.g., Adobe Dreamweaver) and start by creating one large container table. This table sets the margins of the email, and it allows you to place nested tables inside to hold the email together.
4. Continue placing nested tables where you need them while following the guidelines listed in *Things to Avoid* and *Things that Don't Work* below.

### Things to Avoid

#### Borders

 Table cells of 1 pixel will automatically be increased to 5 pixels (or higher). <table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Table borders do work, but are "boxy" and are <span style="text-decoration: underline;">not flexible</span> in terms of style or thickness. If borders are necessary, use images of at least 5 pixels wide by 5 pixels high and stretch to the desired size.</td></tr></tbody></table>#### Rowspan and Colspan (in tables)

 Always try to use nested tables to avoid all use of `rowspan` and `colspan`. Although a table and its contents may look fine in your browser, Lotus Notes tends to stretch and distort emails when they have `rowspan` and `colspan`. #### Variable widths and heights

 Avoid the use of 100% values on tables and images. These can be used, but tend to cause problems with the layout. Always specify a width for tables and columns, however, and use exact pixel dimensions to do so. Furthermore, make sure that all space is accounted for. For example, if you have three columns in one table row, make sure that the total width of the columns is the same as the parent table width. #### Forms

 These will display and function, but they won’t always be the size you want and can cause distortion in the email. #### Image Maps

 These are very unpredictable. One time they could would flawlessly, another not at all. It’s best to use image slicing and link each individual image rather than link sections of one image. #### Paragraph Tags

 These tend to be huge spaces or gaps inside Lotus Notes. For instance, a `<p>` tag used in Internet Explorer/Outlook would create one line break before and after the indented text, image, etc. but in Lotus Notes it creates a space closer to 2 or 3 line breaks before and after. Always use `<br />` or spacer images to create white space. #### Unordered Lists

 Lotus Notes pushes the list up against any text that comes before and after. A better solution would be to create bullets in a nested table and a spacer gif should be used in the first and last rows of the table to force padding around the text. This is the only way to create the same look across platforms; simply adding spacer images before and after a `<ul>` list creates huge gaps in anything other than Lotus Notes. #### Line Height

 Lotus Notes ignores any line-height settings in style tags (i.e. `<font style="line-height:10px">`). #### Microsoft Word

 Copying and pasting text from Microsoft Word (or Excel) will cause a lot of disruption to your messages. Microsoft handle character sets different to other text editors, and if your content is in MS Word, copy and paste it into a text editor first, review it and then copy it into your HTML. Furthermore if you copy content from MS Word straight into a WYSIWYG editor, it will add tags and code that is not compatible with email clients or even web-browsers. If you can avoid the use of MS Word when building messages, you will face fewer issues. ### Things that Do Not Work

#### Background images

 These will appear in a majority of browsers and email platforms, but Lotus Notes strips these out from page backgrounds and table backgrounds. <table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Background colors will work.</td></tr></tbody></table>#### Style Sheets (external and attached)

 These are stripped from Lotus Notes emails, but will display properly as a web page in Lotus Notes. Always use inline styles! #### Jump Links (a.k.a. Named Anchors)

 Jump links allow you to click a link and jump to another part of the email. These will work with most other email platforms, but not in Lotus Notes. #### Anchor Tag Targeting

`_blank` value does not work as a target value for links to open in a new window. Additional Resources and Articles
---------------------------------

- <http://emailgarage.wordpress.com/2007/08/28/html-email-design-tips-for-lotus-notes/>
- <http://www.sitepoint.com/blogs/2005/09/11/html-email-and-lotus-notes/>
- <http://www.templatekit.com/lotusnotes1.php>
- <http://www.graphics.com/modules.php?name=Sections&op=viewarticle&artid=110>
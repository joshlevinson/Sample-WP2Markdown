---
title: 手机兼容定制的HTML
subject: ''
old_url: 'http://emarsys.dev/old/%e6%89%8b%e6%9c%ba%e5%85%bc%e5%ae%b9%e5%ae%9a%e5%88%b6%e7%9a%84html-2/'
---

<span class="mw-headline" id="01ffed4eb006e91728f6f2e0d0712ac8">介绍<a name="bs-ue-jumpmark-ff4bc2ac36afc43aec7de39bf30f7b59"></a></span>
---------------------------------------------------------------------------------------------------------------------------------------

本文件概述了如何改编电子邮件的HTML代码，以便使它按Emarsys生成的手机兼容模板同样的方式运行。

 <table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**

 </th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">请注意这些指南是专为定制HTML电子邮件设计的，而不是为基于模板活动中生成的各部分的先进模式。尽管有可能使用手机兼容模板中的HTML代码，仍存在一些限制。我们建议：如果你确实为了手机兼容模板而使用定制HTML，则你可以在你的设计中使用单列布局。

 </td></tr></tbody></table>### <span class="mw-headline" id="c1af9843aa812280641b684149c8c76c">简要概况及电子邮件格式的历史<a name="bs-ue-jumpmark-570b315133ba3c2229bae851ea9b1d05"></a></span>

为了理解手机兼容模板与标准HTML电子邮件之间的区别，你需要理解HTML模板构成的核心理念。到如今，电子邮件已经30岁了，在内容集成、允许更多和更丰富的内容信息方面经历了各种发展历程。

1996年，电子邮件从纯文本进化到能够支持多元媒体内容。1997年，引入了HTML(4.0)格式，而这种格式现在是当今现代丰富的内容信息的核心语言。电子邮件客户实施了HTML操作方法（MIME），并且由于开始使用嵌套表格生成网页，电子邮件信息也开始使用同样的技术了。

 1998年，级联样式表（CSS）从格式中引入到独立内容中，这可使网页开发者能够使用各种元素生成语义性网页。与使用嵌套表不同，开发者开始为容器和部分表达使用 <div>，而元素被设计用于显示表格数据，比如电子表格（例如Excel）。 但是当网页浏览者跟随并实施了新标准，而且开始按同样方式提供时，电子邮件客户却没有跟进。因而，他们对于内容的方法仍然缺少足够正确的HTML和CSS支持，并且仍然严重依赖表格应用。况且，既然电子邮件是传播病毒和其他恶意软件的捷径，安全问题已经导致进一步的限制。为此，微软于2007年更换了Outlook渲染引擎，即从用于因特网Explorer浏览器的软件转换为用于MS Word的软件。这就导致一些核心HTML和CSS特性变得不被支持。为了同样的原因，Gmail剥离了电子邮件部分以外的一切内容，意味着只能使用内嵌样式。

另一方面，基于网页的电子邮件客户越来越多，Hotmail, Yahoo! Mail 和 Gmail等一些主要厂商都依赖于网页浏览器的渲染引擎显示电子邮件内容，这有助于把同样级别的内容视为显示的网页方面的差距缩小一点。

### <span class="mw-headline" id="7bedbd47d2837179e10974b5f7c44080">桌面邮件和手机邮件之间的区别<a name="bs-ue-jumpmark-971faa8b26f16fd45b63efce117dade5"></a></span>

当向手机和桌面双用户发送内容时，很重要的一点是，注意因打开方式的不同，你的内容将看起来完全不同。比如，在桌面显示器上很容易在文本内找到链接，但是在手机上却很难发现，更别提点击了。同样，在宽屏幕上使用并排图像比较产品看起来不错，但是在手机上却小得很。

所以，为了确保最佳显示的内容被提交到所有平台上，你可以向你的电子邮件添加一些代码，这样可以让它根据将来打开邮件的设备进行不同的显示。

<span class="mw-headline" id="44651d0a3009c56a6e6a691ecce05fe0">技术方法<a name="bs-ue-jumpmark-0be62d675885448687d15ccae876ea05"></a></span>
-----------------------------------------------------------------------------------------------------------------------------------------

如果你想要把手机兼容的电子邮件发送给你的客户，最容易的方法是设计一个单列布局，并且使用样式表，以便使变化适应不同的移动设备。这样就可以根据客户存取内容的方式，让内容有选择性地显示内容。

方法是把媒体查询放在你的HTML代码``部分中`<style>`元素内。

 
    @media (max-device-width: 767px) { /* MOBILE CSS GOES HERE */ }

你在大括号内放置的代码将仅对手机可视。这样你可以：

- 定义电子邮件的宽度适合手机设备（例如320像素，这是一个典型的宽度）。
- 选择性地隐藏或显示电子邮件的各个部分。
- 让缺省的字体大小、按钮和链接更大一些。
- 把图像宽度调整到适合屏幕。
- 把图像替换为能够特别显示在手机上的其他图像。

下面是一些包含媒体查询和手机CSS的案例。

 
    
      
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
      
    

### <span class="mw-headline" id="ae54ca7ddcf0f5ff763f76944ec37514">设置电子邮件宽度<a name="bs-ue-jumpmark-0f987cf624954cb9b855fd6592740b7c"></a></span>

我们向包含电子邮件内容的`<table>`添加命名为“容器”的类。然后，我们为手机CSS部分（`@media` query内）设置CSS规则，并使它的宽度达到320像素。

 
    div[class="yfix"] .container { width: 320px !important; }

然后，将它插入到``中。

 
    <table cellspacing="0" cellpadding="0" border="0" width="600" class="container">

### <span class="mw-headline" id="50bdf84939db257acc036c1f4fccb728">显示并隐藏部分<a name="bs-ue-jumpmark-2bd5816c3b47ab269b8bd3da5542b87f"></a></span>

你可以添加“手机隐藏”CSS类，以便应用到你想针对手机用户进行隐藏的元素。

 
    <p class=”mobile_hidden”>This is hidden from mobiles</p>

### <span class="mw-headline" id="6b419f53f104a774a21382c0494348ad">手机格式<a name="bs-ue-jumpmark-6931e2d75289cde66a1db4becdd4ca04"></a></span>

你可以向手机CSS部分添加一条规则，覆盖信息的桌面外观。通常你可以覆盖那里的任何样式：

#### <span class="mw-headline" id="939539ae65e3afe3faa19e830d43c6ee">字体大小和格式<a name="bs-ue-jumpmark-273d246f788313bad91ea445cb8b91a9"></a></span>

 
    div[class="yfix"] p {
      font-size: 14px;   /* Bigger text */
      color: blue;       /* Changing color /
      text-align: left;  /* Always align paragraph to left */
      line-height: 20px; /* Define the height of the lines */
    }

#### <span class="mw-headline" id="1c97b9bfaed2e84bdebc73144613d88a">链接<a name="bs-ue-jumpmark-0800670cede5bb1017bf0bd51c90a2bb"></a></span>

 
    div[class="yfix"] a {
      border: 1px solid blue;
      background: silver;
      color: #fff;
      font-size: 16px;
      text-decoration: none;
    }

#### <span class="mw-headline" id="059963863f112c86395b72ecde22fa2f">图像大小调整<a name="bs-ue-jumpmark-ad871fa555f96b2cce584b53225b7e16"></a></span>

- 图像尺寸调整－必须向参照的`<img>`标签添加`id="my_image"`以便使变化生效。
 

    div[class="yfix"] #my_image {
      width: 320px !important;
      height: 120px !important;
    }

#### <span class="mw-headline" id="cfcec12ff7d1fb9418e2a2bc5f65317e">替换图像<a name="bs-ue-jumpmark-6a11bf1133e881f99e5028f9db08a289"></a></span>

为了替换手机版的图像，你必须向内容中的图像添加id属性。在简单的模板中，我们向其赋值"header_image"，而且我们向手机CSS部分添加CSS样式。

 
    div[class="yfix"] #header_image {
      content: url(http://example.com/path/to/mobile/image.jpg);
      width: 320px !important;=
      height: 100px !important;
    }

这里我们定义了具有内容规则的新URL（统一资源定位符），让你可以覆盖图像的尺寸。

 <table><tbody><tr><td></td> </tr></tbody><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**请注意：**

 </th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">你在选择器的开始应设置`div[class="yfix"]`，以防止雅虎电子邮件把手机CSS应用到桌面内容上。由于一些手机客户工作方式的不同，最好的做法是把`!important`标记应用到尺寸（宽度和高度）规则上。

 </td></tr></tbody></table>  
 然后，在``部分中，向`<img>`添加id属性。

 
    <img src="http://example.com/image.jpg" alt="" width="600" height="120" id="header_image">

<span class="mw-headline" id="802c9e7fa6c1f33435afb10b73c14ca0">电子邮件客户特定的故障、限制和问题<a name="bs-ue-jumpmark-09534e7a4705f775fac6cc1380b0e918"></a></span>
------------------------------------------------------------------------------------------------------------------------------------------------------

下面是测试各个电子邮件客户时遇到的问题清单，但是可以用作通常最佳实践指南。

- 绝对不要在`<style>`标记内使用备注，因为雅虎邮箱对它们的处理不正确。
- **Gmail**将剥离它不识别的所有内嵌样式规则，除非你把它们设为`!important`。
- 在**Hotmail**中，你不能在部分中使用条件注释。在条件注释之后的所有内容都会被剥离，你的电子邮件将出现中断。
- 通过使用`<meta name="viewport">`标记（如你在代码样例所见）并且让``标记不含任何属性，影响安卓内置电子邮件客户的一些问题将会迎刃而解。
- 你可以添加下列代码，强制**Outlook**提供一个“浏览器中查看“的按钮。
 

    #outlook a { padding: 0; }

- 如果在**Outlook 2007/2010**中的表格出现了缺口，你可以通过下列代码消除缺口：
 

    table { border-collapse: collapse; mso-table-lspace: 0pt; mso-table-rspace: 0pt; border: 0; }
    table td { border-collapse: collapse; }

- 为强制使**Hotmail**以全宽显示电子邮件，添加如下代码：
 

    body { width: 100% !important; }
    .ReadMsgBody { width: 100%; }

- 为强制使**Hotmail**显示常规行距，添加：
 

    .ExternalClass,
    .ExternalClass p,
    .ExternalClass span,
    .ExternalClass font,
    .ExternalClass td,
    .ExternalClass div { line-height: 100%; }

 <dl><dd>你可以在 [http://www.emailonacid.com/forum/viewthread/43/上阅读更多的内容。](http://www.emailonacid.com/forum/viewthread/43/%E4%B8%8A%E9%98%85%E8%AF%BB%E6%9B%B4%E5%A4%9A%E7%9A%84%E5%86%85%E5%AE%B9%E3%80%82) </dd></dl>- 为了阻止**Hotmail**中过大尺寸的表情符号中断了电子邮件，添加：
 

    .ExternalClass img[class=Emoji] {
      width: 10px !important;
      height: 10px !important;
      display: inline !important;
    }

- 为了强制使**WebKit**渲染引擎适用于浮动表，添加：
 

    @media screen and (-webkit-min-device-pixel-ratio: 0) {
      table[class*="sectiongroup"] td[align="center"] {
        text-align: center !important;
      }
      table[class*="sectiongroup"] table.section td[align="center"] {
        text-align: -webkit-center !important;
      }
    }

- 为防止**WebKit**和**Windows Mobile**平台改变缺省的字体尺寸，添加：
 

    body { margin: 0; padding: 0; -webkit-text-size-adjust: none; -ms-text-size-adjust: none; }

</div>
---
title: 'Пользовательский код HTML для мобильных устройств'
subject: ''
old_url: 'http://emarsys.dev/old/%d0%bf%d0%be%d0%bb%d1%8c%d0%b7%d0%be%d0%b2%d0%b0%d1%82%d0%b5%d0%bb%d1%8c%d1%81%d0%ba%d0%b8%d0%b9-%d0%ba%d0%be%d0%b4-html-%d0%b4%d0%bb%d1%8f-%d0%bc%d0%be%d0%b1%d0%b8%d0%bb%d1%8c%d0%bd%d1%8b%d1%85-2/'
---

<span class="mw-headline" id="1082ea8f9f93725b78349d51c8772bfa">Введение<a name="bs-ue-jumpmark-492a2099341ea140f56fea3d815b670a"></a></span>
---------------------------------------------------------------------------------------------------------------------------------------------

 В этом документе описано, как адаптировать HTML-код электронного письма, чтобы обеспечить такое же поведение, как у шаблонов для мобильных устройств, созданных Emarsys. <table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Примечание.**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Эти рекомендации предназначены для пользовательских электронных писем в формате HTML, а не для расширенного режима подготовки рассылок на основе шаблонов. Несмотря на то что HTML-код можно использовать в шаблонах для мобильных устройств, существуют некоторые ограничения. Если предполагается задействование пользовательского HTML-кода в шаблонах для мобильных устройств, то для письма рекомендуется использовать одноколоночную схему.</td> </tr></tbody></table>   ### <span class="mw-headline" id="d98a83c34a2a6d51cc323fc7517a35bd">Краткий обзор и история форматов электронных писем<a name="bs-ue-jumpmark-f9efd9e6efecdf6a44ad981ed796ab15"></a></span>

 Чтобы понять отличие шаблона для мобильных устройств от стандартного письма в формате HTML, необходимо знать основные принципы создания шаблона в формате HTML. Электронная почта используется уже 30 лет, в течение которых были пройдены различные этапы развития в отношении интеграции контента. В настоящее время увеличился объем и усложнилось содержание контента. До 1996 году в электронных письмах еще использовался неформатированный текст, затем он был усовершенствован для обеспечения поддержки контента мультимедийной рекламы, после этого в 1997 году была введена поддержка формата HTML (4.0), который теперь является основным языком современных мультимедийных сообщений со сложным контентом. Почтовые клиенты поддерживают обработку HTML-кода (MIME), и так как веб-страницы создаются с использованием вложенных таблиц, то и для электронных сообщений стала использоваться та же технология. В 1998 году была введена поддержка CSS для отделения контента от элементов форматирования, что позволило веб-разработчикам создавать семантические веб-страницы с использованием элементов. Вместо вложенных таблиц разработчики начали использовать элемент <div> для представления контейнеров и разделов, кроме того, были созданы элементы <table> для отображения табличных данных, таких как электронные таблицы (например, Excel). Однако если для веб-браузеров были внедрены и стали применяться новые стандарты использования и отображения контента, то для почтовых клиентов это не было сделано. Поэтому в почтовых клиентах отсутствует полнофункциональная поддержка HTML и CSS для контента, и работа этих клиентов сильно зависит от использования вложенных таблиц. Кроме того, так как электронная почта является удобным средством для передачи вирусов и других вредоносных программ, проблемы обеспечения безопасности привели к возникновению дополнительных ограничений. Поэтому в 2007 году корпорация Майкрософт заменила механизм рендеринга Outlook: вместо механизма, используемого в браузере Internet Explorer, стали применять механизм, используемый в MS Word. Это привело к прекращению поддержки некоторых основных функций HTML и CSS. По этим же причинам в сообщениях Gmail игнорируется вся информация за пределами раздела письма , в результате чего можно использовать только встроенные стили. С другой стороны, увеличивается популярность почтовых веб-клиентов, и у некоторых основных участников рынка, таких как Hotmail, Yahoo! Mail и Gmail, для отображения контента используется механизм рендеринга веб-браузера. Это должно помочь заполнить пробел в отношении отображения контента одного и того же уровня, как и на веб-страницах. ### <span class="mw-headline" id="d0402bed96663a7e5a9ec47bcc9162c2">Отличие между почтовыми сообщениями для настольных компьютеров и мобильных устройств<a name="bs-ue-jumpmark-bbb7108b00279757fa39125da195ee11"></a></span>

 При отправке контента пользователям и настольных компьютеров, и мобильных устройств важно помнить, что внешний вид контента будет значительно отличаться в зависимости от того, как будет открыто письмо. Например, на мониторе настольного компьютера легко найти ссылки среди текста, но на экране мобильного устройства это может быть затруднительно, не говоря уже о том, что эту ссылку неудобно щелкнуть. Кроме того, сравнение продуктов с помощью расположенных рядом изображений на широком экране может выглядеть хорошо, но на экране мобильного телефона эти изображения могут быть слишком маленькими. Чтобы обеспечить наилучшее отображение контента на всех платформах, вы можете добавить небольшой программный код в свое электронное письмо. В результате этого на разных устройствах контент будет отображаться соответствующим образом. <span class="mw-headline" id="d89166638ac8eaa3d0231ef9942bb3cc">Технический подход<a name="bs-ue-jumpmark-ec4c1ca377d2004f4e208570a4007b3a"></a></span>
-------------------------------------------------------------------------------------------------------------------------------------------------------

 Если вы хотите отправить своим клиентам электронное письмо, подготовленное для мобильного устройства, самым простым способом будет использование одноколоночной схемы и таблицы стилей для внесения специальных изменений для отображения на мобильных устройствах. Это позволит обеспечить избирательное отображение контента в зависимости от типа доступа к нему. Это можно сделать, поместив раздел с запросом на предоставление информации внутри элемента `<style>` в разделе `` вашего HTML-кода: 
    @media (max-device-width: 767px) { /* MOBILE CSS GOES HERE */ }

 Все, что находится между фигурными скобками, будет отображаться только на мобильных телефонах. Здесь можно выполнить следующее: - Определите ширину электронного письма для полного заполнения экранов мобильных устройств (например, 320 пикселей — стандартная ширина).
- Укажите, отображать или скрыть разделы электронного письма.
- Увеличьте размеры шрифта, кнопок и ссылок, указанные по умолчанию.
- Настройте ширину изображения для полного заполнения экрана.
- Замените изображения на специально предназначенные для мобильных устройств.
 
 Ниже приведен пример HTML-кода, содержащего медиазапрос и CSS для мобильных устройств. 
    
      
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
      
    

### <span class="mw-headline" id="62f4e02a1c2cfd1973462705bfbcbb94">Установка ширины электронного письма<a name="bs-ue-jumpmark-fdab4d19d204682c6da446e3d1b0cba1"></a></span>

 Мы добавили класс `container` в элемент `<table>`, содержащий контент письма. Затем мы определили правило CSS в разделе CSS для мобильных устройств (внутри запроса `@media`) и установили ширину, равную 320 пикселям. 
    div[class="yfix"] .container { width: 320px !important; }

 Затем вставили в элемент ``: 
    <table cellspacing="0" cellpadding="0" border="0" width="600" class="container">

### <span class="mw-headline" id="fed9627249c143004b8bc4416796bf03">Отображение и скрытие разделов<a name="bs-ue-jumpmark-eac9bb6ea7e30a36bc3a4882dfb38801"></a></span>

 Вы можете добавить CSS-класс `mobile_hidden` для тех элементов, которые хотите скрыть для пользователей мобильных устройств. 
    <p class=”mobile_hidden”>This is hidden from mobiles</p>

### <span class="mw-headline" id="c6d53580f0f4bcacb0fa4668f5d16d73">Форматирование сообщений для мобильных устройств<a name="bs-ue-jumpmark-7af0ab697b0d210494d96dddbc63e80b"></a></span>

 Вы можете изменить внешний вид сообщения для настольных компьютеров, добавив правило в раздел CSS для мобильных устройств. В большинстве случаев здесь вы можете переопределить любой параметр стиля. #### <span class="mw-headline" id="b6d865f455d0941c0be88a9471025699">Размер шрифта и форматирование:<a name="bs-ue-jumpmark-080e78969cc42b7173eb2627c786eb9c"></a></span>

 
    div[class="yfix"] p {
      font-size: 14px;   /* Bigger text */
      color: blue;       /* Changing color /
      text-align: left;  /* Always align paragraph to left */
      line-height: 20px; /* Define the height of the lines */
    }

#### <span class="mw-headline" id="a289fca7c64f6b29083674032122f8d3">Ссылки<a name="bs-ue-jumpmark-205b9edecb28b3cc5c6f05d2b2838a78"></a></span>

 
    div[class="yfix"] a {
      border: 1px solid blue;
      background: silver;
      color: #fff;
      font-size: 16px;
      text-decoration: none;
    }

#### <span class="mw-headline" id="f14b947a88552ba6fed9dc3766a5508d">Изменение размера изображений<a name="bs-ue-jumpmark-d6e8137b7b1b3f0e7b9e744fd24d47fb"></a></span>

- Изменение размера изображения — добавьте `id="my_image"` в соответствующий тег `<img>`, чтобы изменения вступили в силу:
 

    div[class="yfix"] #my_image {
      width: 320px !important;
      height: 120px !important;
    }

#### <span class="mw-headline" id="0dca3e40bb720c07086ded85b7a915f2">Замена изображений<a name="bs-ue-jumpmark-e40cebf0fdd67d5d68c540b3b12b37a8"></a></span>

 Чтобы заменить изображение в версии для мобильных устройств, добавьте атрибут id для изображения в контенте. В примере шаблона указан атрибут «header_image», и в разделе CSS для мобильных версий мы добавили стиль CSS: 
    div[class="yfix"] #header_image {
      content: url(http://example.com/path/to/mobile/image.jpg);
      width: 320px !important;=
      height: 100px !important;
    }

 Здесь мы указали новый URL-адрес с правилом для контента, позволяющим изменить размер изображения. <table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Примечание.**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Селектор должен начинаться с `div[class="yfix"]` чтобы предотвратить использование CSS-класса Yahoo! Из-за разных способов работы мобильных клиентов рекомендуется применять признак `!important` к правилам определения размеров (width и height).</td> </tr></tbody></table> Затем в разделе `` добавьте атрибут id в элемент `<img>`: 
    <img src="http://example.com/image.jpg" alt="" width="600" height="120" id="header_image">

<span class="mw-headline" id="bae4780d949e016e7f45e3d991402959">Ошибки, ограничения и вопросы, связанные с почтовым клиентом<a name="bs-ue-jumpmark-f19be8fc723f87aa78afa617b1d3110e"></a></span>
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

 Ниже приведен перечень проблем, с которыми нам пришлось столкнуться при тестировании конкретных почтовых клиентов. Они могут быть использованы как общие рекомендации. - Не используйте комментарии в `<style>` тегах, так как **Yahoo! Mail** обрабатывает их некорректно.
- **Gmail** будет игнорировать все встроенные стили, если не установлен атрибут `!important`.
- В **Hotmail** нельзя использовать условные комментарии в разделе ``. Вся информация после условного комментария игнорируется, и электронное письмо будет испорчено.
- Некоторые проблемы со встроенными почтовыми клиентами для **Android** можно решить с помощью тега `<meta name="viewport">` (см. пример программного кода) и удаления всех атрибутов для тега ``.
- Для **Outlook** можно принудительно определить кнопку view in browser (просмотреть с помощью браузера), добавив:
 

    #outlook a { padding: 0; }

 Пробел, появляющийся в таблицах в **Outlook 2007/2010**, можно удалить так: 
    table { border-collapse: collapse; mso-table-lspace: 0pt; mso-table-rspace: 0pt; border: 0; }
    table td { border-collapse: collapse; }

 Чтобы электронные письма отображались в **Hotmail** на полную ширину, добавьте: 
    body { width: 100% !important; }
    .ReadMsgBody { width: 100%; }

 Чтобы электронные письма отображались в **Hotmail** с нормальным междустрочным интервалом, добавьте: 
    .ExternalClass,
    .ExternalClass p,
    .ExternalClass span,
    .ExternalClass font,
    .ExternalClass td,
    .ExternalClass div { line-height: 100%; }

 <dl><dd>Более подробная информация представлена на сайте</dd></dl><http://www.emailonacid.com/forum/viewthread/43/>- Чтобы предотвратить разрыв электронного письма в **Hotmail** из-за символов эмоций очень большого размера, добавьте:
 

    .ExternalClass img[class=Emoji] {
      width: 10px !important;
      height: 10px !important;
      display: inline !important;
    }

- Чтобы в качестве механизма рендеринга в **WebKit** использовались всплывающие таблицы, добавьте:
 

    @media screen and (-webkit-min-device-pixel-ratio: 0) {
      table[class*="sectiongroup"] td[align="center"] {
        text-align: center !important;
      }
      table[class*="sectiongroup"] table.section td[align="center"] {
        text-align: -webkit-center !important;
      }
    }

 Чтобы предотвратить изменение размеров шрифтов по умолчанию на платформах **WebKit** и **Windows Mobile**, добавьте: 
    body { margin: 0; padding: 0; -webkit-text-size-adjust: none; -ms-text-size-adjust: none; }
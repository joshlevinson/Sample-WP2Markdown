---
title: 'Rastreo de eCommerce en Suite'
subject: ''
old_url: 'http://emarsys.dev/old/rastreo-de-ecommerce-en-suite-2/'
---

¿Qué es el rastreo de eCommerce de Emarsys?
-------------------------------------------

 La función de **rastreo de eCommerce** de Emarsys le proporciona la habilidad de rastrear la actividad del usuario final en su tienda Web, para después analizar los datos mediante eMarketing Suite. Esto le permite supervisar el éxito de sus campañas en términos de pedidos en línea junto con el comportamiento del usuario final, con respecto a las tendencias de compra actuales y abandonadas. Existen dos niveles de rastreo de eCommerce disponibles para integrarlos con Suite:

- Rastreo estándar
- Rastreo avanzado
 
**Rastreo de eCommerce estándar**: funciona mediante el etiquetado de secciones clave de su tienda Web con código, que a su vez permite a las secuencias de comandos ingresar datos a partir de cookies que Suite puede usar para la elaboración de informes. **Rastreo de eCommerce Avanzado**: se basa en la función de rastreo estándar y mejora esas capacidades al sincronizarse con la base de datos de contactos de Suite, lo cual permite la segmentación de los datos recopilados, así como el enriquecimiento de los datos de contacto.

### Rastreo estándar – ¿cómo funciona?

 En el rastreo de eCommerce estándar requiere que se integren fragmentos de código en dos áreas claves de su sitio Web (las páginas de **Confirmación del pedido** y la de **Gracias**) que a su vez hace posible obtener informes a nivel de campaña. Esto trabaja usando código en los vínculos de correo electrónico junto con los fragmentos de código integrados en el sitio Web, los que a su vez capturan la información por medio de cookies o datos de sesión que se generan cuando el usuario visita su sitio Web desde un vínculo de un correo electrónico. Los datos capturados se mantienen en una tabla separada que incluye la información de los pedidos, de los artículos y de los carritos de compra abandonados. Como los datos se mantienen separados de la base de datos de contactos, solo se pueden generar informes sobre ellos mas no interactuar con ellos o segmentarlos más a fondo. Como la mayoría de la configuración necesaria para que esto funcione la realiza usted o su equipo técnico en el sitio Web, esta función está disponible sin costo. Pero si requiere soporte para su implementación de rastreo estándar, puede obtenerlo de emarsys y se le cobrará en base a una tarifa por hora. Para mayor información comuníquese con su gerente de cuentas.

### Rastreo avanzado – ¿cómo funciona?

 El rastreo de eCommerce avanzado se basa en la función de rastreo estándar e incluye código en sus páginas Web diseñado especialmente para que capture datos adicionales y los escriba en la base de datos de contacto en Suite, mediante el uso de llamadas de HTTPS simples desde la misma lógica de la tienda. Al alimentar los datos en la base de datos de contacto, usted tiene entonces acceso a los datos generados por el comportamiento de la tienda Web para segmentarlos aún más. Por ejemplo, fecha de última compra, valor de última compra, número total de pedidos, valor total de pedidos, etc. Para usar el rastreo de eCommerce avanzado se requiere una configuración hecha a la medida por parte del equipo de soporte de emarsys y lo cual genera costos adicionales. Comuníquese con su gerente de cuentas para obtener más información.

Rastreo de eCommerce estándar
-----------------------------

### Activación del rastreo de eCommerce estándar

 Para usar el rastreo de eCommerce estándar necesita comunicarse con su gerente de cuenta para habilitarlo y luego seguir los pasos para integrar la función de rastreo, como se describe a continuación. Su gerente de cuenta necesitará una lista de usuarios que usted desee permitir que vean los informes de eCommerce. Estos usuarios se actualizarán al grupo de usuarios 'Administrador de eCommerce' y tendrán acceso completo a las características de Suite. Una vez configurado el acceso, recibirá una ID de cliente y se designará un entorno para que lo utilice:

- https://www.emarsys.net/u
- https://www1.emarsys.net/u
- https://login.emarsys.net/u
- https://suite.emarsys.net/u
- https://suite5.emarsys.net/u
- https://suite6.emarsys.net/u
- https://suite7.emarsys.net/u
- https://suite8.emarsys.net/u
- https://suite9.emarsys.net/u
- https://suite10.emarsys.net/u

  

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Recuerde que:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Después de configurar el rastreo estándar, emarsys también puede configurar el rastreo avanzado – pero tendrá qué comunicarse con su gerente de cuentas para pedir ayuda.</td></tr></tbody></table>  

#### Visualización de la integración del rastreo estándar de eCommerce

 A continuación se muestra un ejemplo de cómo podría funcionar el rastreo estándar de eCommerce para usted.

1. El código de rastreo elegido se inserta en su tienda en línea.
2. El contacto hace clic en el vínculo rastreable insertado en el correo electrónico que reciba.
3. eMarketing Suite reenvía el contacto a su tienda Web y agrega un parámetro `emst` al URL de destino.
4. La tienda Web detecta el parámetro `emst` y almacena la actividad del contacto mediante el uso de una cookie o sesión con una validez de hasta 30 días (por ejemplo).
5. Después de colocar un pedido con éxito, se recupera la página **Gracias** si se detecta una cookie o sesión con el parámetro `emst`.
6. Si un contacto accede a la página **Confirmación del pedido** pero no accede a la página Gracias, entonces no se genera una `ID de pedido` y el evento se marca como un evento de carrito de compras abandonado.
 
[![visualización de la integración del rastreo de eCommerce estándar](/assets/images/2014/04/Ecommerce_tracking_04-1.png)](/assets/images/2014/04/Ecommerce_tracking_04-1.png) Cuando el contacto llega a la página de **Confirmación del pedido**, empieza la captura de datos y éstos se marcan para un correo de carrito de compras abandonado, que solo se cancelará si completan la compra con éxito. Si no completan la compra dentro del periodo de tiempo designado (el valor predeterminado es de 30 minutos), entonces se registra un evento de carrito de compras abandonado.

### Integración del rastreo de eCommerce estándar

 Cuando se configura el acceso de eCommerce, usted tiene dos métodos para integrar las funciones de rastreo a Suite:

- [mediante código de JavaScript](/Suite/ecommerce-tracking-using-javascript.md)
- [mediante código de píxel de imagen](/Suite/ecommerce-tracking-using-an-imagepixel.md)

 Ambos métodos requieren que usted integre código en su sitio Web, pero tienen escenarios de uso ligeramente distintos puesto que el método de JavaScript necesita que los usuarios finales tengan configuraciones de seguridad menos estrictas en su navegador para funcionar. El método de JavaScript usa tres elementos:

- una secuencia de comandos de Emarsys que está alojada en su sitio Web
- un fragmento de código de JavaScript que se inserta en todas las páginas de su sitio Web
- fragmentos de código JavaScript especiales de que se insertan en las páginas designadas

 Algunos usuarios finales pueden tener JavaScript o las cookies deshabilitadas por cuestiones de seguridad, en cuyo caso el rastreo basado en JavaScript no funcionará. Si esto representa un problema para usted, es mejor que utilice la implementación de píxel de imagen para habilitar el rastreo de eCommerce.

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Recuerde que:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Con el método de JavaScript las funciones deben ejecutarse en el orden correcto para funcionar; por ejemplo, `emsTracking` debe ejecutarse antes que `emsSubmitOrder`. Si descarga la secuencia de comandos, estos ejemplos ya estarán preparados para ejecutarse en el orden correcto.</td></tr></tbody></table> Para integrar el método de JavaScript, proceda de la siguiente manera. Tenga en cuenta que debe realizar estos pasos en el orden en el que se listan, o de lo contrario la integración no funcionará.

- Download the script from `http://www.emarsys.net/u/emstrack.js`.
- Store it in a public folder on your web server, e.g. `http://www.yourdomainhere.com/js/emstrack.js`.
- Embed this script in the  section of every webpage:
 

    <script language="Javascript" type="text/javascript" src="http://www.yourdomainhere.com/js/emstrack.js"></script>


    <script type="text/JavaScript">// <![CDATA[
      emsSetEnv('<strong>www1</strong>');
      emsTracking("<strong>112734771</strong>","<strong>yourdomainhere.com</strong>");
    // ]]></script>

  

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/2014/04/Icon_BeCareful.png)](/assets/images/2014/04/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">- This code snippet must be loaded and executed before any `emsSubmitOrder()` calls.
- Replace ***www1*** with your Suite environment variable (your account manager can help you with this).
- Replace ***112734771*** with your Suite customer ID.
- Replace ***yourdomainhere.com*** with the address of your website.
 
</td></tr></tbody></table> Agregue el siguiente código a la página de **Confirmación del pedido** de su sitio Web:


    <form style="display:none;" name="emsform">
      <input type="hidden" name="total" value="totalprice_without_comma_only_with_dot">
      <input type="hidden" name="tax" value=" totaltax_without_comma_only_with_dot ">
      <input type="hidden" name="shipping" value="shippingcosts_without_comma_only_with_dot">
      <input type="hidden" name="city" value="city_of_the_client">
      <input type="hidden" name="country" value="country_of_the_client">
      <!-- Repeat the following line for each ordered product in the cart -->
      <input type="hidden" name="ems_items[]" value="id_of_ordered_product1;category_of_ordered_product1;name_of_ordered_product1;price_of_ordered_product1_without_comma_only_with_dots;quantity_of_ordered_product1_without_comma_only_with_dots">
    </form>
    <script type="text/javascript" language="JavaScript">
      // <!--
      emsSubmitOrder();
      // -->
    </script>

- Agregue el siguiente código a la página de **Gracias**:
 

    <form style="display:none;" name="emsform">
      <input type="hidden" name="tax" value="[totaltax]">
      <input type="hidden" name="shipping" value="[shippingcosts]">
      <input type="hidden" name="city" value="[customer_city]">
      <input type="hidden" name="country" value="[customer_country]">
      <input type="hidden" name="order" value="[order]">
      <input type="hidden" name="total" value="[total]">
      <!-- Repeat the following line of each product in cart -->
      <input type="hidden" name="ems_items[]" value="[sku/code];[category];[product name];[price];[quantity]">
    </form>
    <script type="text/javascript" language="JavaScript">
    // <!--
      emsSubmitOrder();
    // -->
    </script>

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Recuerde que:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Los corchetes en el código anterior son para indicar dónde se introduce el contenido y no deben incluirse; tampoco debe usar comas para separar números grandes. Por ejemplo: value="[total]" debe ser solo value="2999.00" y no value="[2,999.00]". Ahora el código de JavaScript que insertó interactuará con la secuencia de comandos descargada para llenar el contenido de su tienda Web. Al integrar el código, pueden quitarse valores si no se requieren para el informe. Las entradas opcionales son: [sku/código], [categoría], [nombre del producto], [precio], [cantidad].</td></tr></tbody></table> El rastreo de píxel de imagen funciona mediante el uso de un pequeño píxel integrado en la página, con el código asociado que habilita el rastreo. Al contrario del método de JavaScript, este método solo requiere que se inserte código y no hay necesidad de alojar una secuencia de comandos adicional en el sitio Web. A continuación, la tienda Web crea el parámetro URL del píxel de rastreo, que usa la etiqueta <img> insertada en las páginas de **Confirmación del pedido** y de **Gracias**. Para integrar el método del píxel de imagen, proceda de la siguiente manera:

- Agregue el siguiente código a su página de **Confirmación del pedido**:
 

    <img src="http://www.emarsys.net/upages/ti.php?
      ems_customer=123456789&
      ems_visitor=<customer_number>&
      ems_session=<sessionid>&
      ems_campaign=<emst>&
      ems_action=purchase&
      total=<order_total>&
      tax=<tax_total>&
      shipping=<shipping_total>&
      city=<city>&
      country=<country>&
      code[]=productid_of_product1>&
      category[]=<category_of_product1>&
      productname[]=<name_of_product1>&
      price[]=<price_of_product1>&
      quantity[]=<quantity_of_product1>&
      code[]=<productid_of_productX>&
      category[]=<category_of_productX>&
      poductname[]=<name_of_productX>&
      price[]=<price_of_productX>&
      quantity[]=<quantity_of_productX>"
    border="0" alt="" width="1" height="1" style="display:none;">

- Agregue el siguiente código a la página de **Gracias**:
 

    <img src="http://www.emarsys.net/upages/ti.php?
      ems_customer=123456789&
      ems_visitor=<customer_number>&
      ems_session=<sessionid>&
      ems_campaign=<emst>&
      ems_action=purchase&
      order=<orderid>&
      total=<order_total>&
      tax=<tax_total>&
      shipping=<shipping_total>&
      city=<city>&
      country=<country>&
      code[]=<productid_of_product1>&
      category[]=<category_of_product1>&
      productname[]=<name_of_product1>&
      price[]=<price_of_product1>&
      quantity[]=<quantity_of_product1>&
      code[]=<productid_of_productX>&
      category[]=<category_of_productX>&
      productname[]=<name_of_productX>&
      price[]=<price_of_productX>&
      quantity[]=<quantity_of_productX>"
    width="1" height="1" border="0" alt="" style="display:none;">

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Recuerde que:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Debe sustituir ***www.emarsys.net*** con el entorno de Suite apropiado y ***123456789*** con el ID de su cuenta de Emarsys.</td></tr></tbody></table> Ahora el código del píxel de imagen podrá recopilar datos de los contactos de la misma forma que el código de JavaScript, y los retroalimentará a Suite con el fin de elaborar informes. De la misma forma que cuando se integra el código de JavaScript, es posible enmendar el código del píxel de imagen para incluir o excluir datos para la sección del informe en Suite.

##### <span class="mw-headline" id="Explicaci.C3.B3n_de_los_par.C3.A1metros_del_p.C3.ADxel_de_imagen">Explicación de los parámetros del píxel de imagen<a name="bs-ue-jumpmark-a85df6e67960a0f2524fd643246cd7ba"></a></span>

 A continuación se muestra un desglose de los elementos utilizados en el método del píxel de imagen y los parámetros que pueden quitarse para personalizar el rastreo de la misma forma que con el método de rastreo de JavaScript:

<table align="left" border="1" cellpadding="1" class="wikitable" style="width: 100%;"><thead><tr><th>Variable</th> <th>Function</th> </tr></thead><tbody><tr><td>`ems_customer`</td> <td>The emarsys customer ID. Ask your account manager or emarsys Support for this.</td> </tr><tr><td>`ems_visitor`</td> <td>The contact ID</td> </tr><tr><td>`ems_session`</td> <td>The session ID of the contact</td> </tr><tr><td>`ems_campaign`</td> <td>The emst parameter passed in the URL on looking up the web shop</td> </tr><tr><td>`ems_action`</td> <td>constant value: purchase</td> </tr><tr><td>`total`</td> <td>Total value of the order</td> </tr><tr><td>`tax`</td> <td>The tax included in the order (if no parameter is specified, = 0)</td> </tr><tr><td>`shipping`</td> <td>Shipping costs in the order (if no parameter is specified, = 0)</td> </tr></tbody><thead><tr><th>Optional parameters</th> <th></th> </tr></thead><tbody><tr><td>`city`</td> <td>City where the contact is located</td> </tr><tr><td>`Country`</td> <td>Country where the contact is located</td> </tr><tr><td>`code[]`</td> <td>The internal product ID in the web shop</td> </tr><tr><td>`category[]`</td> <td>The corresponding category in the web shop</td> </tr><tr><td>`productname[]`</td> <td>The name of the product</td> </tr><tr><td>`price[]`</td> <td>The unit price of the product</td> </tr><tr><td>`quantity[]`</td> <td>The quantity of the product ordered by the contact</td></tr></tbody></table>### <span class="mw-headline" id="Uso_del_rastreo_de_eCommerce_est.C3.A1ndar_en_Suite">Uso del rastreo de eCommerce estándar en Suite<a name="bs-ue-jumpmark-5db0b6475be9bdd6351f37f18043fbd0"></a></span>

 Una vez que su gerente de cuenta habilita el rastreo de eCommerce, hay una nueva entrada disponible en el menú **Análisis** llamada **Rastreo de E-Commerce**. Esta sección lista los eventos de pedidos exitosos y los eventos de carritos de compras abandonados de la tienda Web, ambos pueden desglosarse para mostrar los artículos que contienen. Estas tres categorías de eventos rastreables se clasifican de la siguiente manera:

- Pedidos colocados con éxito
- Número de carritos de compras abandonados
- Artículos comprados con éxito

 Ambas secciones de pedidos y carritos abandonados tienen la misma información registrada, por ejmplo: fecha del pedido, ID del pedido, correo electrónico del contacto, nombre de la campaña y valor.

#### <span class="mw-headline" id="Pedidos">Pedidos<a name="bs-ue-jumpmark-d03fa8de0dec819b53f045ac0f7268c6"></a></span>

 La sección **Pedidos** proporciona una descripción general de todos los pedidos colocados con éxito, que pueden filtrarse por fecha o campaña de correo electrónico. Para obtener un desglose detallado de los artículos que se compraron en el pedido, solo haga clic en el icono de acercamiento a la derecha de los costos de envío. Al hacer clic en este icono será transportado a la página de artículos con una vista filtrada que sólo incluirá los artículos comprados como parte de ese pedido. [![Sección de pedidos en la pantalla de rastreo de eCommerce](/assets/images/2014/04/Ecommerce_tracking-009-024.jpg)](/assets/images/2014/04/Ecommerce_tracking-009-024.jpg)

#### <span class="mw-headline" id="Carritos_de_compras_abandonados">Carritos de compras abandonados<a name="bs-ue-jumpmark-b73c331dad189c306af028f1f9649f90"></a></span>

 La sección **Carritos de compras abandonados** lista los casos donde se colocaron artículos en un carrito de compras, pero la compra no se completó con éxito dentro de un límite de tiempo establecido (30 minutos). Al igual que con la sección de **Pedidos**, puede obtener un desglose detallado si hace clic en el icono de acercamiento a la derecha de los costos de envío. Los siguientes escenarios son posibles cuando un contacto abandona un carrito de compras:

- El contacto llega a la tienda Web mediante un correo electrónico de Emarsys.
- El contacto llega a la tienda Web mediante el navegador, pero hizo clic en un correo electrónico de Emarsys en los últimos 30 días (por lo cual tiene una cookie activa).
- El contacto llega a la tienda Web mediante el navegador pero sin ninguna cookie activa (esto solo está disponible con el rastreo de eCommerce avanzado).
 
[![Sección de carritos de compras abandonados en la pantalla de rastreo de eCommerce](/assets/images/2014/04/Ecommerce_tracking-010-026.jpg)](/assets/images/2014/04/Ecommerce_tracking-010-026.jpg)#### <span class="mw-headline" id="Art.C3.ADculos">Artículos<a name="bs-ue-jumpmark-d668dbebcf67ca23d263198e33594ca8"></a></span>

 La página de **Artículos** ofrece un desglose de todos los artículos individuales que se compraron, que a su vez pueden filtrarse con base en la campaña de correo electrónico que desencadenó la compra. Aquí las columnas se definen mediante campos del sistema y campos opcionales que se seleccionan al integrar la función de eCommerce estándar (campos opcionales: código de producto, nombre de producto, categoría, precio y cantidad). Figura 4: Sección de artículos en la pantalla de rastreo de eCommerce con los [![Sección de artículos en la pantalla de rastreo de eCommerce con los campos opcionales resaltados](/assets/images/2014/04/Ecommerce_tracking-011-028.jpg)](/assets/images/2014/04/Ecommerce_tracking-011-028.jpg)

#### <span class="mw-headline" id="An.C3.A1lisis_de_rastreo_de_eCommerce">Análisis de rastreo de eCommerce<a name="bs-ue-jumpmark-b88a4ac7d59d7e82696924bbdb492f38"></a></span>

 Una vez habilitada la función, se incluyen los resultados del rastreo de eCommerce en la sección **Resumen de resultados** de **Correos** en el menú **Análisis**. Proporciona un desglose de los ingresos totales, el número de compradores, número de pedidos, promedio de ingresos por pedido, así como el número de carritos de compras abandonados. [![resumen de resultados de eCommerce en la sección de correos](/assets/images/2014/04/Ecommerce_tracking-012-030.jpg)](/assets/images/2014/04/Ecommerce_tracking-012-030.jpg)

<span class="mw-headline" id="Rastreo_de_eCommerce_avanzado">Rastreo de eCommerce avanzado<a name="bs-ue-jumpmark-a0925eca48bdce0def4a6ac371ae8ed8"></a></span>
---------------------------------------------------------------------------------------------------------------------------------------------------------------

### <span class="mw-headline" id="Activaci.C3.B3n_del_rastreo_de_eCommerce_avanzado">Activación del rastreo de eCommerce avanzado<a name="bs-ue-jumpmark-f6e0bd3243cf8c1e101084dd027c6958"></a></span>

 Para usar la función de rastreo de eCommerce avanzado necesita tener el rastreo estándar configurado y funcionando para poder continuar. El siguiente paso es coordinarse con su gerente de cuentas para determinar qué tipo de datos desea que capture el rastreo y en qué campos de Suite deberán alimentarse estos datos. Cada configuración de eCommerce avanzada es única, ya que se basa en los requerimientos de cada cliente.

### <span class="mw-headline" id="Integraci.C3.B3n_del_rastreo_de_eCommerce_avanzado">Integración del rastreo de eCommerce avanzado<a name="bs-ue-jumpmark-379b0bfb338ae4419a632339abc03783"></a></span>

 Una vez que se acuerdan los datos a capturar y se asocian con los campos de datos de Suite, el rastreo avanzado está listo. Funciona generando una llamada de HTTPS a Suite cada vez que se completa una compra exitosa, incluyendo todo el contenido de los campos y la información de contacto en el URL. Esto puede hacerse con o sin el parámetro emst, ya que el único requerimiento para el rastreo avanzado es una dirección de correo electrónico y el `OrderID` (ID del pedido) al que se va a vincular el evento. A continuación se envía el contenido de la URL a Suite, en donde la base de datos de contactos actualiza y enriquece los campos de datos relevantes. El contenido capturado se define al configurar el rastreo y después se envía a Suite mediante HTTPS para asegurar un envío seguro. [![Campos de muestra agregados a la base de datos de contactos mediante el rastreo de eCommerce avanzado](/assets/images/2014/04/Ecommerce_tracking-014-055.jpg)](/assets/images/2014/04/Ecommerce_tracking-014-055.jpg)

#### <span class="mw-headline" id="Visualizaci.C3.B3n_de_la_integraci.C3.B3n_del_rastreo_de_eCommerce_avanzado">Visualización de la integración del rastreo de eCommerce avanzado<a name="bs-ue-jumpmark-2c9c3ecf005ebf2e47042e7b99569581"></a></span>

 A continuación se muestra un ejemplo de cómo podría funcionar el rastreo de eCommerce avanzado para usted.

1. El rastreo de eCommerce estándar está configurado y funcionando.
2. Emarsys prepara el código de rastreo avanzado para cumplir con sus requerimientos y después lo integra al sitio Web.
3. El contacto accede a la tienda Web mediante un vínculo en un correo electrónico, el cual provoca que se agregue el parámetro `emst` al URL, que la tienda Web selecciona y usa para generar una cookie/sesión.
4. El contacto finaliza el proceso de pasar a la página de pago.
5. Se genera una URL de rastreo en la lógica de la tienda y se solicita (por ejemplo, PHP usando el comando file, o file_get_contents), y se usa la información de `emst` cuando esté disponible.

 Si el contacto agrega contenido a su carrito de compras sin pasar a la página de confirmación, entonces esto también puede rastrearse si se detecta una cookie con el parámetro `emst`. [![visualización de la integración del rastreo de eCommerce avanzado](/assets/images/2014/04/Ecommerce_tracking-013-032.jpg)](/assets/images/2014/04/Ecommerce_tracking-013-032.jpg)

### <span class="mw-headline" id="Uso_del_rastreo_de_eCommerce_avanzado_en_Suite">Uso del rastreo de eCommerce avanzado en Suite<a name="bs-ue-jumpmark-a237f00fedaad475588ec860e27d4fd5"></a></span>

 Debido a la forma en que funciona el rastreo avanzado, no se ven pantallas adicionales en Suite en comparación con el rastreo estándar. El propósito principal es enriquecer la base de datos de contactos y permitir la segmentación con base en la actividad. Los segmentos provenientes del rastreo avanzado están disponibles para usarse en programas en el Centro de automatización; por ejemplo, trabajando con los hábitos de compras en línea de sus contactos y desencadenando la ejecución de programas con base en ellos. Mediante el uso del rastreo de eCommerce avanzado usted puede empezar a enriquecer los datos que mantiene sobre los contactos por medio de la forma en que se comportan en su tienda Web, lo que se traduce en segmentación de precisión para futuras campañas. No sólo puede aislar tendencias mediante el uso de informes estándar, sino que ahora tiene también la habilidad de aplicar esa información para segmentar campañas futuras. El rastreo de eCommerce avanzado es lel paso natural a seguir una vez se tenga el rastreo de eCommerce estándar, ya que además de capturar datos de usuarios que llegan a la tienda Web mediante una campaña de correo electrónico, también captura los datos de otros usuarios que completan compras y los agrega a la base de datos de contactos. Por medio de lógica y reglas personalizadas, es posible usar el rastreo de eCommerce avanzado para actualizar y enriquecer los perfiles de los contactos, con base en la forma en que se comportan en su tienda Web. Las integraciones del lado servidor resultan en solicitudes de rastreo de HTTPS sencillas, además de que permiten la inclusión y el rastreo de nuevos contactos a los que no se les hayan enviado campañas anteriores.

#### <span class="mw-headline" id="Ejemplos_de_programas_que_usan_el_rastreo_de_eCommerce_avanzado">Ejemplos de programas que usan el rastreo de eCommerce avanzado<a name="bs-ue-jumpmark-449b5f6ba71c1009f9ead0965bc6b370"></a></span>

 A continuación se muestran algunos ejemplos del tipo de programa que podría crear mediante el uso de los datos capturados con el rastreo de eCommerce avanzado. [![Programa de lealtad](/assets/images/2014/04/Ecommerce_tracking-016-058.jpg)](/assets/images/2014/04/Ecommerce_tracking-016-058.jpg) [![Reactivación](/assets/images/2014/04/Ecommerce_tracking-016-059.jpg)](/assets/images/2014/04/Ecommerce_tracking-016-059.jpg) [![Encuesta de satisfacción del cliente](/assets/images/2014/04/Ecommerce_tracking-017-107.jpg)](/assets/images/2014/04/Ecommerce_tracking-017-107.jpg)
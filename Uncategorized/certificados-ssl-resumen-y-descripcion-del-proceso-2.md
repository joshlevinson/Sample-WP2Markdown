---
title: 'Certificados SSL - Resumen y descripción del proceso'
subject: ''
old_url: 'http://emarsys.dev/old/certificados-ssl-resumen-y-descripcion-del-proceso-2/'
---

<span class="mw-headline" id="56e83b193dc8875b502c3e5d57d24d05">Introducción<a name="bs-ue-jumpmark-32639bc962ef586845548b55c8289be3"></a></span>### <span class="mw-headline" id="96f0eccbb5584221bb0b296be50d6990">Qué es SSL<a name="bs-ue-jumpmark-61fe79bc9c3a5b7b139c8f3db3f65409"></a></span>


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

 Secure Socket Layer (SSL) es un término utilizado para describir un protocolo que proporciona una comunicación segura en redes de ordenadores. Con el fin de identificar claramente los socios de comunicaciones, se utilizan los denominados certificados SSL. Emarsys utiliza certificados SSL para encriptar el acceso a nuestros servicios y a los dominios de vínculos de nuestros clientes.

<div class="center"><div class="floatnone">[![Conexión segura indicada por el navegador Web](/assets/images/2014/07/SSL_Cert_Process_address_bar.png)](/assets/images/2014/07/SSL_Cert_Process_address_bar.png)</div></div>#### <span class="mw-headline" id="46ff7b92325c2f65d6a820b314c726af">Ejemplo práctico<a name="bs-ue-jumpmark-f1aa07437a89fe89e1261cf8d545b606"></a></span>

 Una posible aplicación para los certificados SSL sería cuando se utiliza un formulario de autenticación. Debido a que en estos casos se introducen datos personales, la seguridad es indispensable. Tanto formularios que involucran datos personales como las aplicaciones eCommerce deben usar una comunicación codificada. Lo mismo se puede decir para las páginas de confirmación de registros, páginas para darse de baja, o cualquier otro recurso web fundamental en sus actividades de eMarketing: sus clientes siempre deben sentir que están operando en un entorno online seguro. Los certificados SSL permiten la creación de una conexión segura y codificada entre el navegador y el servidor Web. Esta se lleva a cabo habitualmente de forma transparente para el usuario (en la capa de aplicación del protocolo IP) mediante un protocolo de intercambio de claves entre el cliente y el servidor Web en las que están involucradas las claves pública y privada de este último. Una vez que se realiza la conexión segura, ésta se representa por un pequeño ícono de candado en la barra de dirección del navegador con el prefijo “https” (la ‘s’ es de seguridad) en la URL, que son las únicas indicaciones visibles de una sesión segura en curso. Por el contrario, cuando un usuario abre un sitio web no seguro (es decir, uno que no está protegido con un certificado SSL válido), el mecanismo de seguridad del navegador muestra una advertencia al usuario, avisándole activamente de que el sitio no es seguro y que terceras partes podrían interceptar datos sensibles. Al encontrarse con un mensaje de advertencia, la mayoría de usuarios rehusarán ingresar datos en un formulario.

<div class="center"><div class="floatnone">[![Advertencia del certificado SSL](/assets/images/2014/06/SSL_Cert_Process_SSLFailure.png)](/assets/images/2014/06/SSL_Cert_Process_SSLFailure.png)</div></div> Después de decidir que desea utilizar una comunicación codificada con los usuarios, el objetivo sería que se pueda acceder a un sitio web seguro sin activar ninguna advertencia. Una URL implementada correctamente está formada de esta manera: `https://newsletter.yourdomain.com/u/register.php?CID=12345678&f=12345`  

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/2014/04/Icon_BeCareful.png)](/assets/images/2014/04/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">Como alternativa, el vínculo anterior se puede convertir en HTTP "normal" al eliminar la S en la URL, pero en ese caso correría el riesgo de que los datos personales de los usuarios pudiesen ser robados.</td></tr></tbody></table>  

### <span class="mw-headline" id="42f3487a224b929bb5bbe9cf56fb8e9d">Obtención de un certificado<a name="bs-ue-jumpmark-b0f8140f34bed017c13c0c0a704552a4"></a></span>

<table cellpadding="1" class="wikitable" style="width: 100%; border: 1px solid #fff;"><tbody><tr><td scope="col" style="text-align: left; border: 1px solid #fff;" width="60px">[![Icon FurtherReading.png](/assets/images/2014/04/Icon_FurtherReading.png)](/assets/images/2014/04/Icon_FurtherReading.png)</td> <td scope="col" style="border: 1px solid #fff;">Esta sección asume que usted ya puede crear formularios en Suite. Si desea obtener mayor información, sírvase de leer *Suite Online Help*.</td></tr></tbody></table>  

<div class="center"><div class="floatnone">[![El proceso de certificación](/assets/images/2014/06/SSL_Cert_Process_Process.png)](/assets/images/2014/06/SSL_Cert_Process_Process.png)</div></div> Para obtener un certificado, proceda de la siguiente manera:

- Genere un archivo de Solicitud de Firma de Certificado (CSR, por sus siglas en inglés) para el dominio que esté utilizando. Este archivo contiene información acerca del dominio (“quién es usted”). A continuación vea información adicional sobre los archivos CSR.
- Diríjase a una Autoridad de Certificación (CA, por sus siglas en inglés) y compre un certificado. Los certificados están disponibles con diferentes períodos contractuales y para diferentes sistemas operativos. Es importante que usted se asegure de elegir el más apropiado entre los siguientes: - Certificado simple para un dominio solamente, es decir, “newsletter.sudominio.com“
- Certificado comodín para todos los subdominios de segundo nivel por debajo de “*.sudominio.com”, que le permite incluir formularios de registro así como tiendas Web.
 
<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Recuerde que:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">El certificado debe coincidir con el sistema operativo del servidor, que en el caso de emarsys, es Linux.</td></tr></tbody></table>  

- Una vez que haya recibido el certificado de la CA, envíe los dos siguientes archivos a Emarsys: - Archivo de clave privado (.key)
- Archivo de certificado (.crt)
- Emarsys instalará el certificado y lo vinculará al dominio (por ej. formulario de registro de newsletter).

  

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/2014/04/Icon_BeCareful.png)](/assets/images/2014/04/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">¡No debe instalarse certificados durante la ejecución de campañas!</td></tr></tbody></table>  

#### <span class="mw-headline" id="996dfd3d4120446cc7039fe60143d7e8">Archivos CSR<a name="bs-ue-jumpmark-8bcc940cd28491fdf2eef73f8c5f7820"></a></span>

 Una Solicitud de Firma de Certificado (CSR) es un mensaje codificado que contiene toda su información (nombre de organización, ubicación, país, etc.) y que usted debe proveer a la hora de comprar un certificado a una Autoridad de Certificación (CA). La CA utiliza esta información para crear el certificado SSL que se vincula al dominio para el que generó la CSR, lo que hace posible la conexión SSL. Si necesita ayuda para obtener información acerca de su dominio, puede utilizar el protocolo Whois con el que podrá encontrar toda la información relevante del dominio. Como el archivo de CSR se vincula al dominio, debe crearse en el servidor Web que aloja su dominio. Podría ser necesario que usted contacte con una persona que tenga acceso a este servidor para que le genere el archivo CSR.  

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/2014/04/Icon_BeCareful.png)](/assets/images/2014/04/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">- ¡Si su dominio es sólo de reenvío (Registro tipo A), debe generarse el archivo CSR en el servidor web que actualmente aloja el sitio web!
- Si usted tiene una entrada CNAME, elimínela antes de instalar el certificado.
 
</td></tr></tbody></table>  

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Recuerde que:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Es importante que todos los datos en un archivo CSR coincidan exactamente con la información utilizada cuando se solicita un certificado. De no ser así, el proceso de certificación podría fracasar, o el certificado no podría no funcionarpara el dominio que solicitó.</td></tr></tbody></table>  

#### <span class="mw-headline" id="672004e9c4394aa2b0ac74577b67fe9b">Autoridades de certificación recomendadas<a name="bs-ue-jumpmark-73634ff4f853bbffded00f4beb4bf377"></a></span>

 Emarsys recomienda las siguientes Autoridades de Certificación.

- Symantec (anteriormente VeriSign): <http://www.symantec.com/en/uk/ssl-certificates>
- Trustwave: <https://ssl.trustwave.com/>
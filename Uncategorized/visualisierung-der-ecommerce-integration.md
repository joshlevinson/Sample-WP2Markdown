---
title: 'Visualisierung der eCommerce-Integration'
subject: ''
old_url: 'http://emarsys.dev/old/visualisierung-der-ecommerce-integration/'
---

#### Visualisierung der Standard-eCommerce-Integration

 Nachfolgend finden Sie ein Beispiel dafür, wie das Standard-eCommerce-Tracking bei Ihnen aussehen könnte.

1. Der ausgewählte Tracking-Code wird in Ihren Online-Shop eingebettet.
2. Der Kontakt klickt auf den nachverfolgbaren Link, den er per E-Mail erhalten hat.
3. Emarsys eMarketing Suite leitet den Kontakt zu Ihrem Online-Shop weiter und fügt der Ziel-URL einen Parameter hinzu, den sogenannten `emst`-Parameter.
4. Der Webshop erkennt den `emst`-Parameter und speichert die Kontaktaktivität mithilfe eines Cookies oder einer Sitzung, die beispielsweise bis zu 30 Tage gültig sind.
5. Nachdem eine Bestellung erfolgreich getätigt wurde, wird die Seite **Danke** abgerufen, sofern ein Cookie oder eine Sitzung mit dem Parameter `emst` erkannt wird.
6. Greift ein Kontakt auf die Seite **Bestellbestätigung** zu, nicht aber auf die Seite **Danke**, wird keine `orderID` generiert und das Ereignis wird als abgebrochener Warenkorb markiert.
 
[![Visualisierung der Standard-eCommerce-Integration](/assets/images/2014/04/Ecommerce_tracking_04-1.png)](/assets/images/2014/04/Ecommerce_tracking_04-1.png)
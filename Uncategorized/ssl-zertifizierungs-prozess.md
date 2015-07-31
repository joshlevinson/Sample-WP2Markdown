---
title: 'SSL Zertifizierungs-Prozess'
subject: ''
old_url: 'http://emarsys.dev/old/ssl-zertifizierungs-prozess/'
---

Einleitung### Was ist SSL?


----------------------------

 Der Begriff Secure Socket Layer (SSL) beschreibt ein Protokoll zur sicheren Datenüber-tragung in Computernetzwerken. Für die klare Identifizierung der Kommunikationspartner werden sogenannte SSL-Zertifikate eingesetzt. Emarsys verwendet SSL-Zertifikate zur Verschlüsselung des Zugriffs auf unsere Dienste und auf die Link-Domains unserer Kunden.

<div class="center"><div class="floatnone">[![SSL_Cert_Process_address bar](/assets/images/2014/06/SSL_Cert_Process_address-bar.png)](/assets/images/2014/06/SSL_Cert_Process_address-bar.png)</div></div>#### Praktisches Beispiel

 Eine mögliche Anwendung für SSL-Zertifikate wäre die Verwendung eines Authentifizie-rungsformulars. In solchen Fällen geben die Benutzer persönliche Daten ein, daher hat die Sicherheit hier oberste Priorität. Für Formulare mit persönlichen Daten und alle eCommerce-Anwendungen sollte immer eine verschlüsselte Datenverbindung verwendet werden. Dasselbe gilt auch für die Bestätigungsseiten bei Registrierungen, Abmeldungsseiten und alle anderen wichtigen Webressourcen Ihrer eMarketing-Aktivitäten. Ihre Kunden müssen immer das Gefühl haben, dass Sie sich in einer sicheren Online-Umgebung befinden. SSL-Zertifikate ermöglichen eine sichere und verschlüsselte Verbindung zwischen Webbrowser und Webserver. Ein "Handshake"-Prozess, der die Sitzung herstellt, findet hinter den Kulissen statt. Dazu schickt der Webbrowser eine verschlüsselte Datei von Ihrer Website, die dann mit einem privaten Schlüssel auf dem Server verglichen wird. Nachdem eine sichere Verbindung hergestellt wurde, wird diese durch ein kleines Schlosssymbol in der Adressleiste des Browsers und das vorangestellte "https" ("s" steht für "secure") in der URL dargestellt. Dies sind die beiden einzigen sichtbaren Hinweise für eine aktive sichere Verbindung. Im Gegensatz dazu wird beim Öffnen einer ungesicherten Website (d. h. einer Seite, die nicht mit einem gültigen SSL-Zertifikat geschützt ist) durch den Sicherheitsmechanismus des Browsers eine Warnung ausgegeben, die den Benutzer daran erinnern soll, dass sensible Daten unter Umständen von Dritten abgefangen werden könnten. Durch die Konfrontation mit einer solchen Meldung geben die meisten Nutzer nur widerwillig ihre Daten in ein Formular ein.

<div class="center"><div class="floatnone">[![SSL-Zertifikatswarnung](/assets/images/2014/06/SSL_Cert_Process_SSLFailure.png)](/assets/images/2014/06/SSL_Cert_Process_SSLFailure.png)</div></div> Wenn Sie sich für eine verschlüsselte Kommunikation mit Ihren Benutzern entschieden haben, besteht das Ziel nun darin, dass auf eine sichere Website zugegriffen werden kann, ohne dass Warnungen ausgelöst werden. Eine korrekt implementierte URL würde so aussehen: `https://newsletter.yourdomain.com/u/register.php?CID=12345678&f=12345`  

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/2014/04/Icon_BeCareful.png)](/assets/images/2014/04/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">Als Alternative könnte der oben genannte Link in "normales" HTTP konvertiert werden, indem das 's' in der URL entfernt wird - in diesem Fall würden Sie aber den eventuellen Diebstahl von Daten riskieren.</td></tr></tbody></table>  

### <span class="mw-headline" id="130578b926c218b6903137cc65ef22cd">Erhalt eines Zertifikats<a name="bs-ue-jumpmark-66de0d16ecd36d15582671212e5bf5a1"></a></span>

<table cellpadding="1" class="wikitable" style="width: 100%; border: 1px solid #fff;"><tbody><tr><td scope="col" style="text-align: left; border: 1px solid #fff;" width="60px">[![Icon FurtherReading.png](/assets/images/2014/04/Icon_FurtherReading.png)](/assets/images/2014/04/Icon_FurtherReading.png)</td> <td scope="col" style="border: 1px solid #fff;">Diesem Abschnitt liegt die Annahme zugrunde, dass Sie bereits mit der Erstellung von Formularen in der Suite vertraut sind. Weitere Informationen finden Sie in der *Online-Hilfe zur Suite*.</td></tr></tbody></table>  

<div class="center"><div class="floatnone">[![Der Zertifizierungsvorgang](/assets/images/2014/06/SSL_Cert_Process_Process.png)](/assets/images/2014/06/SSL_Cert_Process_Process.png)</div></div> Um ein Zertifikat zu erhalten, gehen Sie folgendermaßen vor:

- Erstellen Sie eine Certificate Signing Request (CSR)-Datei für die Domain, die Sie verwenden. Diese Datei enthält Informationen über die Domain ("wer sind Sie"). Nachfolgend finden Sie weitere Informationen über CSR-Dateien.
- Gehen Sie zu einer Zertifizierungsstelle (engl. Certification Authority; CA) und kaufen Sie ein Zertifikat. Zertifikate sind mit verschiedenen Vertragslaufzeiten und für verschiedene Betriebssysteme erhältlich. Es ist wichtig, dass Sie aus den folgenden Optionen die für Sie am besten geeignete auswählen: - Einzelzertifikat für nur eine Domain, wie z. B. "newsletter.ihredomain.com"
- Wildcard-Zertifikat für alle First-Level-Subdomains unterhalb von "*.ihredomain.com", wodurch Registrierungsformulare und Webshops abgedeckt werden können.
 
<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Bitte beachten Sie:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Das Zertifikat muss dem Betriebssystem des Servers entsprechen, was im Fall von emarsys die Auswahl eines Zertifikats für ein Linux-Betriebssystem bedeutet.</td></tr></tbody></table>  

- Nachdem Sie das Zertifikat von der CA erhalten haben, senden Sie die folgenden zwei Dateien an Emarsys: - private Schlüsseldatei (.key)
- Zertifikatsdatei (.crt)
- Emarsys wird dann das Zertifikat installieren und dieses mit der Domain verknüpfen (z. B. dem Newsletter-Registrierungsformular).

  

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/2014/04/Icon_BeCareful.png)](/assets/images/2014/04/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">Die Zertifikate dürfen nicht während der Ausführung von Kampagnen installiert werden!</td></tr></tbody></table>  

#### <span class="mw-headline" id="fa13719a691a0f0edff5fd410802a2d6">CSR-Dateien<a name="bs-ue-jumpmark-0119e6c6b23a5643d5cf0947e824fb20"></a></span>

 Ein Certificate Signing Request (CSR) ist eine verschlüsselte Dateneinheit, die alle Informationen (Name des Unternehmens, Standort, Land usw.) enthält, die Sie für den Kauf eines Zertifikats von einer Zertifizierungsstelle (Certification Authority, CA) benötigen. Die CA nutzt diese Informationen für die Erstellung des SSL-Zertifikats, das dann mit der Domain verknüpft wird, für die Sie den CSR erstellt haben, wodurch die SSL-Verbindung dann schlussendlich möglich wird. Benötigen Sie bei der Erfassung der Informationen über Ihre Domain Unterstützung, können Sie diese relevanten Domaininformationen auf einfache Weise über das Whois-Protokoll herausfinden. Neben der Verknüpfung der CSR-Datei mit Ihrer Domain muss diese auch auf dem Webserver erstellt werden, auf dem Ihre Domain gehostet wird. Unter Umständen muss eine Person mit Zugriff auf diesen Server kontaktiert werden, um die CSR-Datei für Sie zu erstellen.  

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/2014/04/Icon_BeCareful.png)](/assets/images/2014/04/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">- Handelt es sich bei Ihrer Domain nur um eine Weiterleitungsadresse (A-Record), muss die CSR-Datei auf dem Webserver erstellt werden, der die eigentliche Website hostet!
- Wenn Sie einen CNAME-Eintrag haben, muss dieser vor der Installation des Zertifikats entfernt werden.
 
</td></tr></tbody></table>  

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Bitte beachten Sie:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Es ist sehr wichtig, dass alle Daten in einer CSR-Datei exakt mit den Informationen übereinstimmen, die Sie bei der Beantragung des Zertifikats angegeben haben. Ist dies nicht der Fall, kann der Zertifizierungsvorgang fehlschlagen oder das Zertifikat funktioniert eventuell nicht für die gewünschte Domain.</td></tr></tbody></table>  

#### <span class="mw-headline" id="96d0d668d722e539acbb56470e47c002">Empfohlene Zertifizierungsstellen<a name="bs-ue-jumpmark-76d3d4ed93fb7796b8dab7f832159131"></a></span>

 Emarsys empfiehlt die folgenden Zertifizierungsstellen:

- Symantec (ehemals VeriSign): <http://www.symantec.com/en/uk/ssl-certificates>
- Trustwave: <https://ssl.trustwave.com/>
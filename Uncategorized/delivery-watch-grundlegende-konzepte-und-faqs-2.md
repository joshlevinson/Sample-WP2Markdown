---
title: 'Delivery Watch - Grundlegende Konzepte und FAQs'
subject: ''
old_url: 'http://emarsys.dev/old/delivery-watch-grundlegende-konzepte-und-faqs-2/'
---

Einführung
----------

Als das E-Mail-Marketing seinen weltweiten Siegeszug antrat, wurde eines schon sehr bald deutlich: Optimierter Content und eine höhere Versandgeschwindigkeit allein reichen nicht aus, um die Kampagnen-Zustellraten (Deliverability) entscheidend zu verbessern und für eine höhere Durchdringung zu sorgen. E-Mail ist von Natur aus eine unsichere Methode des Informationstransfers über das Internet; daraus ergibt sich auf der einen Seite der Wunsch, die Menge der tatsächlichen Inbox-Zustellungen einschätzen zu können, und auf der anderen Seite das Bedürfnis, die Sender zu authentifizieren.

Das Delivery Watch Toolkit wurde entwickelt, um die potenziellen Zustellprobleme einer beliebigen Kampagne zu erkennen und zu analysieren; damit trägt es entscheidend zur Qualität von Kampagnen bei. Dafür bewertet das Toolkit verschiedene Aspekte der Kampagne, um jene Schwachstellen zu identifizieren, die einen negativen Einfluss auf die Zustellbarkeit haben und damit die Reputation des Senders beschädigen können.

Delivery Watch überprüft sämtliche Aspekte einer Kampagne während des Sendevorgangs und hilft so, die Zustellraten zu maximieren; dabei kommen folgende Module zum Einsatz:

- Kampagnen-Modul (Campaign Module)
- Spamfilter-Modul (Spamfilter Module)
- Monitoring-Modul (Monitoring Module – Blacklist, Mailserver-Konfiguration, Mail-Authentifizierung)
- Analyse-Modul (Analysis Module)

Alle diese Module wurden entwickelt, um jeweils ganz bestimmte Aspekte der Kampagne zu testen; dabei werden sowohl die Kampagne selbst als auch der Sender analysiert, um herauszufinden, ob und inwieweit sie unseriöse Praktiken einsetzen (Spamming, Spoofing, etc.) Darauf basierend können potenzielle Konfigurationsprobleme oder Reputationsrisiken behandelt und so die Zustellbarkeit einer Kampagne entscheidend verbessert werden.

Das Delivery Watch Toolkit
--------------------------

Das Delivery Watch Toolkit ist eine integrierte Lösung, die eine Reihe automatisierter Monitoring-Dienste für den komplexen Bereich der E-Mail-Deliverability – der Zustellbarkeit von E-Mails – anbietet; damit kann es das Reputation-Building eines Unternehmens ganz wesentlich unterstützen. Delivery Watch evaluiert den Content einer E-Mail anhand verschiedener Mechanismen, welche die Player der Branche – große E-Mail-Provider, aber auch Einzelpersonen – verwenden, um die Einhaltung bestimmter Qualitätskriterien zu sichern bzw. zu erzwingen. Dazu gehören u.a. das Black- bzw. Whitelisting und die domainbasierte Reputationsbewertung.

Die vier Hauptmodule des Toolkits ermöglichen die Evaluierung individueller Kampagnen anhand einer Reihe von Kriterien, die direkten Einfluss auf die Zustellbarkeit haben.

<table border="0" class="wikitable" style="width: 100%;"><thead><tr><th>Modulname</th> <th>Leistung</th> </tr></thead><tbody><tr><td>Kampagnen-Modul</td> <td>Testet die generelle ISP-Zustellbarkeit; mittels eigens eingerichteter aktiver Mailboxen bei allen großen E-Mail-Providern können die jeweiligen Inbox-Zustellraten ermittelt werden.</td> </tr><tr><td>Spamfilter-Modul</td> <td>Testet Content gegen alle gebräuchlichen Spamfilter; es werden Plug-ins auf Serverseite, Plug-ins auf Client-Seite und externe cloudbasierte Dienste kombiniert, um herauszufinden, wie die Kampagne kategorisiert wird.</td> </tr><tr><td>Monitoring-Modul</td> <td>Testet die Konfiguration und Reputation des sendenden Mailservers; dafür werden verschiedene Mail-Authentifizierungs-Checks, Blacklists und gebräuchliche No-Use-Praktiken beobachtet.</td> </tr><tr><td>Analyse-Modul</td> <td>Bietet aufschlussreiche Analysen zu einer Kampagne, basierend auf den Testergebnissen der anderen Module.</td></tr></tbody></table>### <span class="mw-headline" id="9715acaef741980371fc641d87d40c5f">Kampagnen-Modul<a name="bs-ue-jumpmark-3feb0807b3fcce00cfcb07b0f7af126e"></a></span>

Das Kampagnen-Modul bietet einen ISP Tracking Service; dabei wird die Zustellbarkeit einer E-Mail-Kampagne gegen verschiedene große und internationale ISPs getestet. Dazu verwendet der Dienst Test-Mailboxen, die beim jeweiligen ISP eingerichtet wurden. Die Ergebnisse dieser Mailbox-Tests können sodann dazu verwendet werden, die Inbox-Zustellraten für den jeweiligen ISP zu errechnen.

Diese Test-Mailboxen werden als **Seedlist** bezeichnet. Delivery Watch überwacht das Zustellergebnis für Testkampagnen, indem es für jeden ISP die Attribute "pass", "spam" oder "blocked/missing" vergibt. Die Seedlist wird nach Regionen gruppiert (Nordamerika, DACH etc.). Delivery Watch zeigt die Ergebnisse per Region an; Sie können detaillierte Ergebnisse je nach Land bis hin zu Ergebnissen für individuelle ISP-Mailboxen abrufen.

Der Tracking-Vorgang wird gestartet, sobald eine Kopie der Kampagnen-Mail („Trigger-Mail“ genannt) an eine Mailbox von Delivery Watch gesendet wird, die auch Teil der Seedlist ist. Anhand der Trigger-Mail weiß Delivery Watch, dass eine neue Kampagne gesendet wurde und auf die Verarbeitung wartet. Der ISP Tracking Service vergleicht den Content der Trigger-Mail mit ihren Gegenstücken in den Seedlist-Mailboxen.

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**

 </th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Zwei Kampagnen gelten als identisch (*identical*), wenn sie den gleichen Inhalt haben und innerhalb von 24 Stunden einlangen; sie gelten jedoch als verschieden (*different*), wenn zwischen ihrem jeweiligen Einlangen mehr als 24 Stunden liegen, auch wenn sie gleichen Inhalts sind.

 </td></tr></tbody></table>  
 Dieses Verhalten kann vermieden werden, indem jeder Kampagne ein eindeutiger Header hinzugefügt wird; in der Folge können Kampagnen anhand dieses Headers eindeutig identifiziert/zugeordnet werden.

Die URL für das Kampagnen-Modul: [[1]](https://www.deliverywatch.net/campaign/listCampaigns.do)

### <span class="mw-headline" id="b564c734c40b449cade3be390462e6fc">Spamfilter-Modul<a name="bs-ue-jumpmark-8b9b39b64840798abe401ce2ddf1f15c"></a></span>

Mit dem Spamfilter-Modul kann die Zustellbarkeit einer E-Mail-Kampagne gegen eine Auswahl der gebräuchlichsten Spamfilter getestet werden. Dabei identifiziert das Modul potenzielle Probleme für die Kampagne. Zu diesem Zweck verwendet das Modul eine interne Delivery Watch Mailbox, die die Trigger-Mail an die Spamfilter-Umgebung weiterleitet, wo die Kampagne anhand verfügbarer Anti-Spam-Technologien getestet wird.

Eine Kopie der E-Mail-Kampagne wird an die Mailbox gesendet, welche sodann den Spamfilter-Test initiiert; die Ergebnisse werden sowohl für die einzelnen Spamfilter als auch zusammenfassend präsentiert. Jeder Spamfilter kennzeichnet den Inhalt entweder als "Inbox", "Spam" oder "Pending" – gemeinsam mit einem Überblick über die Spamfilter-Ergebnisse für die unterstützten Anti-Spam-Technologien. Die URL für das Spamfilter-Modul: [[2]](https://www.deliverywatch.net/spamfilter/listReports.do)

### <span class="mw-headline" id="9396c088c2c196b3d9d493b4e9b5f2fa">Monitoring-Modul<a name="bs-ue-jumpmark-c79a5f62115812b06a578a37862fd69c"></a></span>

Das Monitoring-Modul dient den Kunden von Delivery Watch dazu, die Konfiguration und Reputation der von ihnen verwendeten Mailserver zu optimieren. Zu diesem Zweck verfügt das Monitoring-Modul über drei Untermodule:

- Blacklist-Modul (Blacklist Module)
- Modul zur Mailserver-Konfiguration (Mailserver Configuration Module)
- Modul zur Mail-Authentifizierung (Mail Authentication Module)

Für alle E-Mail-Kampagnen, die zum Zwecke des ISP Tracking an Delivery Watch gesendet werden (dies geschieht im Kampagnen-Modul), wertet das Monitoring-Modul die Header aus und vergleicht diese mit den DNS-Informationen.

#### <span class="mw-headline" id="e8a8a5c30a8b01795e4d67c91d5b8ab1">Blacklist-Modul<a name="bs-ue-jumpmark-098a902cca87d6eaff56e2f86468cb8e"></a></span>

Das Blacklist-Modul stellt sicher, dass die IP-Adresse des Senders bzw. die Return-Path Domain nicht in der Blacklist aufscheinen; dazu werden die wichtigsten und gebräuchlichsten Blacklists periodisch überprüft. Mittels DNS Query wird der Status eines Mailservers entweder als "OK" oder "Fault" ermittelt; darüber hinaus besteht die Möglichkeit, detailliertere Analyse anzuzeigen und so herauszufinden, welcher Grund für den Fault-Status ausschlaggebend war, d.h., warum sich der Mailserver auf einer Blacklist findet.

Die URL für das Blacklist-Modul:[[3]](https://www.deliverywatch.net/blacklist/listServers.do)

#### <span class="mw-headline" id="540e73f51c45a3453c971d6c937aaa72">Modul zur Mailserver-Konfiguration<a name="bs-ue-jumpmark-2eef611359ac4e96d266faf59ac36e46"></a></span>

Das Modul zur Mailserver-Konfiguration führt fünf verschiedene Arten von Konfigurations-Checks aus. Unter anderem verifiziert es jene Informationen im Header der Kampagnen-Mail, die sich auf den sendenden Mailserver beziehen. Folgende Aspekte werden im Rahmen dieses Checks überprüft und bestätigt:

- Dass ein gültiger DNS-Eintrag besteht.
- Dass der Domain-Name korrekt ist.
- Dass der Sender kein "Open Relay" ist.
- Dass die Sender-IP-Adresse nicht Teil eines IP-Bereichs des Typs "Dial-in" ist
- Dass die IP-Adresse des Senders nicht Teil eines bekannten dynamischen IP-Bereichs ist

Falls alle fünf Checks erfolgreich sind, ist der Status "OK". Sollte aber nur einer der Checks negativ ausfallen, ergibt sich ein Gesamtstatus "Fault". Sie können detaillierte Ergebnisse anzeigen und so herausfinden, welcher Check fehlgeschlagen ist; auch eine ausführliche Beschreibung der Ergebnisse aller Konfigurations-Checks für die entsprechende Mailserver-IP-Adresse ist so abrufbar.

##### <span class="mw-headline" id="181b80565d44092a3166cbcfcd28f6cd">Bestätigung, dass ein gültiger DNS-Eintrag besteht<a name="bs-ue-jumpmark-27f2861c51db61555b2f5d1a1fd99985"></a></span>

Die IP-Adresse des Mailservers, der die Kampagne sendet, wird dem Header der E-Mail selbst entnommen und dann mit dem DNS-Eintrag für den Mailserver verglichen. Dieser Check bestätigt die Existenz eines gültigen DNS-Eintrags für den Server und fungiert auch als Konsistenz-Check, um sicherzustellen, dass die Kampagne denselben Ursprung hat. Jede Inkonsistenz zwischen DNS-Eintrag und der im Header enthaltenen Informationen kann zu einer Verringerung der Inbox-Zustellraten führen.

##### <span class="mw-headline" id="a052ce7d58ce5433f9593175822cf491">Bestätigung, dass der Domain-Name korrekt ist<a name="bs-ue-jumpmark-842572de16764d26a57bb2529f63bc5b"></a></span>

Bei der Überprüfung des Kampagnen-Headers hinsichtlich gültiger DNS wird auch der Domain-Name des Mailservers identifiziert. Der Domain-Name aus dem DNS-Eintrag wird mit dem Domain-Namen im Header verglichen, um sicherzustellen, dass beide übereinstimmen. Jede Diskrepanz zwischen der Domain-Informationen im DNS-Eintrag und jenen im Header kann zu einer Verringerung der Inbox-Zustellraten führen.

##### <span class="mw-headline" id="e9cfa9883c185286a96e031843e64149">Bestätigung, dass der Sender kein "Open Relay" ist<a name="bs-ue-jumpmark-4dcacd93abd04a21cc3d336103652e03"></a></span>

Ein so genannter "Open Relay" ist ein Mailserver, für den keine Authentifizierung erforderlich ist bzw. der anderen Hosts keinerlei Einschränkungen auferlegt (z. B. IP-Einschränkungen), wenn diese E-Mails über ihn senden wollen. Open Relays gelten allgemein als eine potenzielle Quelle für Spam-Nachrichten, und wenn ein Mailserver als solcher identifiziert wurde, ist eine mögliche Konsequenz, dass sich die Inbox-Zustellraten verringern. Bei diesem Check wird einfach eine Testmail an den Server gesendet, um zu sehen, ob sie weitergesendet werden kann oder nicht.

##### <span class="mw-headline" id="14a4576a7f024d224796d0baf12212d0">Bestätigung, dass die Sender-IP-Adresse nicht Teil eines IP-Bereichs des Typs "Dial-in" ist<a name="bs-ue-jumpmark-66323077850d364edbd7a82924bcf68b"></a></span>

Der Header der E-Mail gibt auch Aufschluss über den IP-Bereich des Mailservers, der die Nachricht sendet; dieser wird sodann überprüft, um sicherzugehen, dass er kein "Dial in"- Bereich ist. "Dial in"-Bereiche sind anonymisiert, weil der ursprüngliche IP versteckt ist; die einzig sichtbare IP-Adresse ist jene des Dial-in-Bereichs selbst. Diese IP-Bereiche werden üblicherweise nicht für produktive Mailserver verwendet, da sie als eine potenzielle Spam-Quelle gelten. Wenn erkannt wird, dass ein Mailserver einen solchen IP-Bereich verwendet, kann das zu einer Verringerung der Inbox-Zustellraten führen.

##### <span class="mw-headline" id="544822847b9538d300f2a8539499c1a4">Bestätigung, dass die Sender-IP-Adresse nicht Teil eines bekannten dynamischen IP-Bereichs ist<a name="bs-ue-jumpmark-fa01e2820d7aed9fbd31fd8c69eff8ee"></a></span>

Der IP-Bereich des Mailservers aus dem E-Mail-Header wird überprüft, um sicherzugehen, dass ein statischer IP-Adressenbereich verwendet wird, und nicht einer, der für die Ausgabe dynamischer IPs bekannt ist. Wenn erkannt wird, dass ein Mailserver derartige IP-Adressen verwendet, kann das zu einer Verringerung der Inbox-Zustellraten führen.

Die URL für das Modul zur Mailserver-Konfiguration:[[4]](https://www.deliverywatch.net/compliance/displayServers.do)

#### <span class="mw-headline" id="1bbb88f466cb3f2e1c49792f240d4503">Modul der Mail-Authentifizierung<a name="bs-ue-jumpmark-e31627b816273fc386dcfcffae33aea0"></a></span>

Das Modul der Mail-Authentifizierung überprüft und stellt sicher, dass die IP-Adresse des Mailservers, welche aus dem Header gelesen wird, autorisiert ist, im Auftrag jenes Domain-Namens zu senden, der im Return-Path Header angegeben ist. Der Check wird mithilfe des Sender Policy Framework (SPF) durchgeführt; dieses kann eine Senderadresse als gefälscht identifizieren. Der Check hat vier mögliche Ergebnisse:

<table class="wikitable"><thead><tr><th>Status</th> <th>Erklärung</th> </tr></thead><tbody><tr><td>Pass</td> <td>Der Sender ist autorisiert, im Auftrag jenes Domain-Namens zu senden, der im Return-Path des Kampagnen-Mail-Headers angeführt ist.</td> </tr><tr><td>Neutral</td> <td>Über den Autorisierungsstatus des Senders kann keine Aussage getroffen werden; die Nachricht sollte vom Server akzeptiert werden.</td> </tr><tr><td>Soft-Fail</td> <td>Der Sender ist nicht autorisiert, im Auftrag jenes Domain-Namens zu senden, der im Return-Path des Kampagnen-Mail-Headers angeführt ist; der Empfänger sollte dies jedoch großzügig handhaben. Dieses Ergebnis soll dem Debugging dienen.</td> </tr><tr><td>Fail</td> <td>Der Sender ist nicht autorisiert, im Auftrag jenes Domain-Namens zu senden, der im Return-Path des Kampagnen-Mail-Headers angeführt ist.</td></tr></tbody></table>Das Modul der Mail-Authentifizierung gibt nur dann ein "OK" zurück, wenn das Ergebnis des SPF-Checks ein "Pass" ist; für alle anderen Ergebnisse des SPF-Checks wird ein "Fault" zurückgegeben. Sie können eine ausführliche Beschreibung der SPF-Ergebnisse für die entsprechende Kampagne abrufen.

Die URL zum Modul der Mail-Authentifizierung:[[5]](https://www.deliverywatch.net/serverChecks/displayMailAuth.do)

### <span class="mw-headline" id="9a401363f41893d9578f4a0a3b0cc5d5">Analyse-Modul<a name="bs-ue-jumpmark-96a0b5ffd22d8c323e4d1141b4180237"></a></span>

Das Analyse-Modul besteht aus 19 Berichtstypen, die eine Reihe detaillierter statistischer Informationen zur Inbox-Zustellrate einer Kampagne bieten; diese basieren auf charakteristischen Parametern wie E-Mail-Größe, Content-Typ, Sendefrequenz und vielen anderen mehr.

<div class="center"><div class="floatnone">[![Sample Analytics Module report](/assets/images/2014/07/DeliveryWatch_Concepts_and_FAQ_-_Page_07_Image_0002.png)](/assets/images/2014/07/DeliveryWatch_Concepts_and_FAQ_-_Page_07_Image_0002.png)</div></div>Das Analyse-Modul zeigt die Kampagneninformationen immer in zwei Spalten an: die Durchschnittswerte für den Account bzw. die Account-Kampagnen vs. die globalen Durchschnittswerte. Die Parameter des Berichts können angepasst werden, um andere Ergebnisse einzuschließen, z. B. den Zeitraum der Analyse, die Branche und viele mehr.

Die URL für das Analyse-Modul:[[6]](https://www.deliverywatch.net/analytics/selectReport.do)

<span class="mw-headline" id="b5baf3cf9e60e37511f6e09c1b1f0870">Wie Sie mit Delivery Watch arbeiten<a name="bs-ue-jumpmark-d6126487fe3f315ab1737b498333cc2a"></a></span>
------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Delivery Watch soll den Kunden von emarsys helfen, ihre Zustellraten zu verbessern; zu diesem Zweck werden für die Kunden Accounts eingerichtet. Größere Kunden haben ihre eigenen Accounts, während für kleinere Kunden die entsprechenden Informationen an die Delivery Watch Account Manager gehen. Unabhängig vom jeweiligen Account ist das Monitoring üblicherweise Sache des Account Managers.

<table class="wikitable"><thead><tr><th>Art des Kunden</th> <th>Delivery Watch Account</th> </tr></thead><tbody><tr><td>A  
 Key  
 Gold</td> <td>- Für die Kunden wird ein eigener Account eingerichtet
- Falls erforderlich, können die Kunden auch mehrere Accounts haben
 
</td> </tr><tr><td>B  
 C</td> <td>- Es wird der persönliche Account des Account Managers verwendet
 
</td></tr></tbody></table>### <span class="mw-headline" id="daa9f704ff3ee6c389339bf348bcfd37">Delivery Watch Account einrichten<a name="bs-ue-jumpmark-5f347d72e5ef3671cd955b3955be577f"></a></span>

Um das Support-Angebot von Delivery Watch zu nutzen, muss zuerst ein Account eingerichtet werden; dazu sind folgende Schritte erforderlich:

1. Der Account Director oder Head of Client Services stimmt dem Antrag auf Einrichten eines Delivery Watch Accounts zu.
2. Der entsprechende Antrag (Account Setup Request) wird mit folgenden Informationen an den Delivery Watch Support gesendet: - Name des Kunden
- Art des Kunden (Customer Type)
- Name des Account Managers/Executive

Es ist die Aufgabe der Account Managers oder Account Executives, die Zustellraten eines Kunden mittels Delivery Watch zu überwachen. Wenn ein Kunde seinen Vertrag mit emarsys kündigt, ist es die Aufgabe des Account Managers, diese Information an den Delivery Watch Support weiterzugeben, damit der Account geschlossen werden kann.

Falls Kunden (z. B. A, Gold, Key) Zugriff auf ihren eigenen Delivery Watch Account erhalten haben, muss der Account Manager den Administratorzugriff beibehalten; Kunden erhalten ausschließlich Zugriff auf Benutzerebene. Detaillierte Informationen zu der entsprechenden Vorgehensweise sind in einer eigenen Anleitung dokumentiert, die entweder über den 2nd Level Support oder den Delivery Watch Support selbst bezogen werden kann.

### <span class="mw-headline" id="9dc43480502d6f025723c47b44c6320a">Delivery Watch Support<a name="bs-ue-jumpmark-3032cd50acf0506ad33bb4d9d2419b1e"></a></span>

Für emarsys-Kunden agiert der Account Manager als erste Anlaufstelle bezüglich Delivery Watch Support; alle anderen Kunden kontaktieren den Delivery Watch Support direkt.

Es ist immer empfehlenswert, vor einer Kontaktaufnahme mit dem Support die verfügbare Dokumentation zu Rate zu ziehen. Wenn es Ihnen nicht möglich ist, ein Problem selbst zu beheben, eskalieren Sie es bitte an den Delivery Watch Support ; achten Sie darauf, so viele Informationen wie möglich hinzuzufügen, einschließlich des Account-Namens und Ihres Unternehmensstandorts.

Delivery Watch hat für emarsys einen eigenen E-Mail Support Service für Kunden von Delivery Watch eingerichtet: [[7]](mailto:support@deliverywatch.com).

### <span class="mw-headline" id="a4aeae3593c2f8a3e946fa268920961d">Web Service-API (WS-API) verwenden<a name="bs-ue-jumpmark-8dfe12d4fd650cbe10aa746b3cb79877"></a></span>

Einige der Module von Delivery Watch sind über das Web Service-API (WS-API) verfügbar, das es Drittanwendungen ermöglicht, Tests durchzuführen und die Ergebnisse auf ihren GUIs anzuzeigen. Derzeit sind nur das Kampagnenmodul und das Spamfilter-Modul über WS-API verfügbar.

<span class="mw-headline" id="dd6796f8460bbafef6a2c4b22afe08a2">Problembehandlung und FAQs<a name="bs-ue-jumpmark-fc6bbeeab003b715f619317fe713057b"></a></span>
---------------------------------------------------------------------------------------------------------------------------------------------------------------

Der folgende Abschnitt beantwortet eine Reihe häufig gestellter Fragen und gibt Tipps, wie erkannte Probleme zu behandeln sind.

### <span class="mw-headline" id="26aac453ef1d88d9084f64bf25b6b4cc">Kampagne wird in Delivery Watch nicht angezeigt<a name="bs-ue-jumpmark-2a39038b91ac6237d778bd30d74081b9"></a></span>

Delivery Watch registriert eine neue Kampagne, sobald eine Kampagnen-E-Mail an die Trigger-Mailbox geliefert wird; diese wird ganz unten in der Seedlist als `cdw*@deliverywatch.com` angezeigt. Vergewissern Sie sich, dass diese Adresse in der Empfängerliste der fraglichen Kampagne enthalten ist, und fügen Sie sie gegebenenfalls einfach hinzu.

Falls das Problem anhält, wenden Sie sich bitte an den Support.

### <span class="mw-headline" id="1df24c8650b0d43ed6f9a33c1fde6f07">Kampagnenergebnisse fehlen<a name="bs-ue-jumpmark-228d7614e24b7e2f8f4719c13348710e"></a></span>

Die Kampagne wurde vom System erfolgreich registriert, aber ein großer Teil davon wurde als fehlend gekennzeichnet. Der häufigste Grund dafür, dass Ergebnisse als fehlend angezeigt werden, ist, dass der E-Mail-Content nicht in der Mailbox verfügbar war, als das System diesen abgefragt hat.

Falls 100 % der Kampagnen für alle (oder einzelne Anbieter) fehlen, kann die Ursache darin liegen, dass die entsprechenden Adressen nicht Teil der Seedlist sind und daher auch nicht an sie gesendet wurde.

1. Überprüfen Sie die Protokolldateien, um sicherzugehen, dass die Empfänger die E-Mail mittels SMTP akzeptiert haben.
2. Aktualisieren Sie Ihre Seedlist für die nächste Kampagne.

Das ist das häufigste Problem, dem sich die Benutzer des Systems gegenübersehen.

Ein weiterer Grund kann sein, dass das System die Ergebnisse nicht abfragen kann, obwohl die E-Mails erfolgreich zugestellt wurden. So verhindern zum Beispiel POP3-Anbieter, dass andere Ordner als der Posteingang angezeigt werden; wenn die Nachricht in den Spam-Ordner geliefert wurde, kann sie nicht angezeigt werden.

Eine weitere mögliche Erklärung dafür, dass eine große Zahl an Ergebnissen fehlt, sind technische Probleme aufseiten der ISPs (z. B. ein Systemausfall), die Delivery Watch daran hindern, die Ergebnisse aus den Mailboxen abzurufen.

Für detailliertere Informationen wenden Sie sich bitte an die Deliverability-Abteilung oder den Delivery Watch Support.

### <span class="mw-headline" id="55d1feac2e05117f059f37518da5f53f">Was ausstehende Spamfilter-Ergebnisse bedeuten können<a name="bs-ue-jumpmark-204abaa7f5af77931d7c673faae47760"></a></span>

Ein Spamfilter-Check dauert üblicherweise 5-10 Minuten. Falls Ergebnisse nach der Maximaldauer von 10 Minuten immer noch ausstehen, deutet das darauf hin, dass es ein Problem mit dem System gibt. Der häufigste Grund dafür ist, dass ein Spamfilter beschädigt ist; dieser Umstand sollte dem Delivery Watch Support so rasch wie möglich mitgeteilt werden.

### <span class="mw-headline" id="6c1bf5a62d6e1438c95560a55f76c2b2">Wie mit Authentifizierungswarnungen umzugehen ist<a name="bs-ue-jumpmark-ca092baac6f0e7340c0a84383b6ff9fc"></a></span>

Falls Sie eine Authentifizierungswarnung erhalten, kontaktieren Sie bitte die Deliverability-Abteilung ([[8]](mailto:deliv@emarsys.com)), deren Aufgabe es ist, sicherzustellen, dass die Kundenauthentifizierungen korrekt eingerichtet und ausgeführt werden. Ihr 2<sup>nd</sup> Level Support vor Ort hilft Ihnen gerne bzw. eskaliert das Problem bei Bedarf an das Deliverability-Team.

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**

 </th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Die Authentifizierungs-Checks können nicht deaktiviert werden. Sie wurden bewusst eingerichtet, um die Content-Qualität sicherzustellen und die Zustellbarkeit der E-Mails zu verbessern.

 </td></tr></tbody></table>### <span class="mw-headline" id="812b5abf09a4377cae9b7d3bec084414">Es wurden mehrere Kampagnen gesendet, aber auf dem Dashboard wird nur eine Kampagne angezeigt<a name="bs-ue-jumpmark-ee9303f8553260e9a4762603681f0861"></a></span>

Das Kampagnen-Modul verwendet einen speziellen Mechanismus, um duplizierte Kampagnen herauszufiltern; damit wird verhindert, dass die monatlichen Limits irrtümlich aufgebraucht werden. Duplizierter Content, d.h. Nachrichten, die irrtümlich oder aufgrund eines fehlerhaften Setups gesendet wurden, werden durch diesen Mechanismus herausgefiltert; dabei wird der Content (Header + Body) überprüft; wenn die Übereinstimmung mit dem Content einer anderen Kampagne 91 % oder mehr beträgt, wird er als identisch gekennzeichnet.

Ein Content, der als identisch gilt und innerhalb von 24 Stunden nach Registrierung der ursprünglichen Kampagne bei Delivery Watch gesendet wird, wird als duplizierter Content klassifiziert und nicht auf dem Dashboard angezeigt.

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**

 </th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Aus technischen Gründen haben derzeit nur Mitarbeiter des Delivery Watch Support Zugriff auf die Mailboxen von deliverywatch.com.

 </td></tr></tbody></table>### <span class="mw-headline" id="4cf3250299f85e20beb5831ff6ede3bb">Fehlerberichte senden<a name="bs-ue-jumpmark-94cc809a0eb9b2769aff3e1c4d55ad0c"></a></span>

Falls Sie Fehler melden wollen oder Vorschläge zur Verbesserung haben (z. B. in Bezug auf Formatierungen, veraltete Informationen etc.), wenden Sie sich bitte an den Delivery Watch Support. Sie helfen uns, wenn Sie so viele Informationen wie möglich anfügen; bitte senden Sie Ihre Anfrage an folgende Support-Adresse: [[9]](mailto:support@deliverywatch.com).
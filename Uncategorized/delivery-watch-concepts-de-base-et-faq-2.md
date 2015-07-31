---
title: 'Delivery Watch - Concepts de base et FAQ'
subject: ''
old_url: 'http://emarsys.dev/old/delivery-watch-concepts-de-base-et-faq-2/'
---

<div class="bodyContent">I am here to prevent the first-page-empty bug!

Introduction
------------

Lorsque l’email marketing a fait son apparition, il est rapidement devenu évident qu’envoyer des contenus enrichis plus rapidement, ne suffirait pas en soi, pour améliorer la délivrabilité de la campagne et pour augmenter le taux de pénétration de la campagne. L’e-mail de par sa nature, n'est pas un moyen sécurisé pour l’envoi d’informations sur Internet.Par conséquent, le besoin d'estimer le taux de remise en boîte de réception et d'évaluer l'authentification de l'expéditeur est apparu.

Delivery Watch est une boite à outils conçue pour analyser et traiter tout éventuel problème de délivrabilité pour toute campagne d'e-mails envoyée, garantissant ainsi la qualité d'une campagne. La boite à outils se charge d'évaluer plusieurs aspects de la campagne afin d'identifier les éventuels problèmes pouvant compromettre la délivrabilité et par la suite, la réputation de l'expéditeur.

Delivery Watch vérifie tous les aspects d'une campagne lors de l'envoi afin d'optimiser les taux de délivrabilité à l'aide des modules suivants :

- Module de campagne
- Module de filtre anti-spam
- Module de Monitoring (Liste noire, configuration du serveur de messagerie, authentification de l’e-mail)
- Module d'analyse

Chaque module est conçu pour tester un aspect particulier de la campagne. Il analyse à la fois la campagne et l'expéditeur afin d'identifier les points faibles les plus souvent relevés (par ex. : les courriers indésirables, l'usurpation, etc.). En proposant ce service, tout éventuel problème de configuration ou de réputation peut être signalé et traité en vue d'optimiser la délivrabilité d'une campagne.

La boite à outils Delivery Watch
--------------------------------

La boite à outils Delivery Watch est une solution intégrée proposant des services de monitoring automatisés, destinés aux environnements complexes de délivrabilité d'e-mails et par conséquent de construction de réputation. Elle y parvient en évaluant activement le contenu par rapport aux divers mécanismes d'application des règlements actuellement utilisés par de nombreux acteurs, d’importants fournisseurs d’e-mail jusqu'aux particuliers utilisant des mesures anti-spam telles que la white/blacklist, la notation de la réputation basée sur un domaine, etc.

Les quatre modules principaux de la boite à outils permettent d'évaluer le comportement de chaque campagne et de le comparer à divers aspects influençant la délivrabilité.

 <table border="0" class="wikitable" style="width: 100%;"><thead><tr><th>Nom du module</th> <th>Champ d'application</th> </tr></thead><tbody><tr><td>Module de campagne</td> <td>Teste la délivrabilité générale des FAI en maintenant plusieurs boîtes de réceptions actives avec tous les principaux fournisseurs d’e-mail afin d'estimer les taux de remise en boîte de réception respectifs.</td> </tr><tr><td>Module de filtre anti-spam</td> <td>Teste le contenu en fonction de tous les principaux filtres anti-spam et en utilisant un mélange de plug-ins serveur, de plug-ins client et de services externes de Cloud, afin d'évaluer la classe à laquelle appartient la campagne.</td> </tr><tr><td>Module de monitoriing</td> <td>Vérifie la configuration et la réputation du serveur de messagerie d'envoi en contrôlant les diverses vérifications d'authentification d’e-mail, les listes noires et les pratiques inutiles standard.</td> </tr><tr><td>Module d'analyse</td> <td>Fournit une analyse pertinente du contenu de la campagne en fonction de tests réalisés par les autres modules.</td></tr></tbody></table>### <span class="mw-headline" id="4cbd6cfc7c6dd46a94a0704f0ec1c529">Le module de campagne<a name="bs-ue-jumpmark-23f21021f241013a68a2f49345c3400c"></a></span>

Le module de campagne fournit un service de suivi de FAI qui fonctionne en testant la délivrabilité d'une campagne d'e-mails en fonction des principaux FAI mondiaux, à l'aide d'une série de boîtes de réception tests configurées avec chaque FAI. Les résultats obtenus via ces boîtes de réception pour la campagne peuvent ensuite être utilisés pour calculer les taux de remise en boîte de réception des FAI d'après ces résultats.

Ces boîtes de réception tests sont référencées dans la **seedlist** (liste d'adresses pièges), et Delivery Watch surveille les résultats de délivrabilité des campagnes tests en les répartissant dans des catégories : « autorisé », « spam » ou « bloqué/manquant » pour chaque FAI. La seedlist est divisée par région (Amérique du Nord, Europe germanophone, etc.) ; Delivery Watch affiche les résultats par région. Vous pouvez descendre dans la hiérarchie de ces résultats : d'un pays jusqu'aux boîtes de réception individuelles de FAI.

Le processus de suivi commence lorsqu'une copie du message de la campagne (désigné par le terme « e-mail de déclenchement ») est envoyée vers une boîte de réception de Delivery Watch, qui fait également partie de la seedlist. L'e-mail de déclenchement signale à Delivery Watch qu'une nouvelle campagne a été envoyée et qu'elle est en attente de traitement. Le service de suivi de FAI compare le contenu de l'e-mail de déclenchement avec ses homologues provenant des boîtes de réception de la seedlist.

 <table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Notez que :**

 </th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">deux campagnes sont considérées *identiques* si le contenu est le même et s'il est acheminé dans un délai de 24 heures, mais sont considérées *différentes* si le délai de leur acheminement est supérieur à 24 heures, même si le contenu est identique.

 </td></tr></tbody></table>  
 Il est possible d'éviter cela en garantissant l'ajout d’un en-tête unique à chaque campagne, ce qui permet par la suite d'associer une campagne en utilisant son en-tête comme identifiant.

URL du module de campagne : [[1]](https://www.deliverywatch.net/campaign/listCampaigns.do)

### <span class="mw-headline" id="de5c0d4cce7cfca31accab07f373c365">Le module de filtre anti-spam<a name="bs-ue-jumpmark-ec92687f9fd9bb563906e74314fc942c"></a></span>

Le module de filtre anti-spam permet de tester la délivrabilité d'une campagne d'e-mails en fonction d'une sélection de filtres anti-spam disponibles les plus utilisés. En procédant ainsi, le module identifie tout éventuel problème inhérent à la campagne. Ce module utilise une boîte aux lettres interne de Delivery Watch qui transfère l'e-mail de déclenchement vers l'environnement du filtre anti-spam, qui teste la campagne en fonction des technologies anti-spam disponibles.

Une copie de la campagne d'e-mails est envoyée vers la boîte aux lettres qui effectue ensuite le test du filtre anti-spam et présente les résultats par filtre anti-spam ainsi qu'un résumé global. Chaque filtre anti-spam signalera le contenu en tant que « Boîte de réception », « Spam » ou « En attente » ; il fournira aussi un résultat global pour le filtre anti-spam selon les technologies prises en charge. URL du module de filtre anti-spam : [[2]](https://www.deliverywatch.net/spamfilter/listReports.do)

### <span class="mw-headline" id="1a44882a0ae6a0cb6b3dacda33d7e15e">Le module de monitoring<a name="bs-ue-jumpmark-e30889704eaa3a864e8fe979e856dffd"></a></span>

Le module de monitoring est conçu pour optimiser la configuration et la réputation des serveurs de messagerie utilisés par les clients de Delivery Watch lors de l'envoi de leurs campagnes. Pour ce faire, le module de monitoring comporte trois sous-modules :

- Module de liste noire
- Module de configuration du serveur de messagerie
- Module d'authentification d’email

Les en-têtes sont automatiquement examinés et comparés aux informations DNS par le module de surveillance pour toute campagne d'e-mails envoyée à Delivery Watch pour le suivi de FAI (module de campagne).

#### <span class="mw-headline" id="5edc96f812402db6e6cc0844eca87856">Le module de liste noire<a name="bs-ue-jumpmark-fa5b77fa84cef6250e49958fa3d884fb"></a></span>

Le module de liste noire garantit que l'adresse IP des expéditeurs ou que le domaine Return-Path n'apparaisse pas dans une liste noire en effectuant des vérifications périodiques par rapport à certaines listes noires les plus importantes et connues. En utilisant une requête DNS, le statut d'un serveur de messagerie est retourné: « OK » ou « Erreur », avec la possibilité d'étudier la raison pour laquelle l'erreur sous-jacente s'est produite (raison de l'apparition sur liste noire).

URL du module de liste noire : [[3]](https://www.deliverywatch.net/blacklist/listServers.do)

#### <span class="mw-headline" id="a60a6e54868455277eff85e256d40dca">Le module de configuration du serveur de messagerie<a name="bs-ue-jumpmark-335dc69a91644a75d39df5757e0483b3"></a></span>

Le module de configuration du serveur de messagerie effectue cinq types de vérification de configuration. Il vérifie, entre autres, les informations contenues dans l'en-tête de l'e-mail de la campagne concernant le serveur de messagerie d'envoi. Les points suivants sont traités dans le cadre de cette vérification :

- Confirmer qu'une entrée DNS valide existe
- Vérification de l'exactitude du nom de domaine
- Confirmer que l'expéditeur n'est pas un « relais ouvert »
- Confirmation que l'adresse IP de l'expéditeur n'est pas comprise dans une plage d'adresses IP d'accès entrant
- Confirmation que l'adresse IP de l'expéditeur n'est pas comprise dans une plage d'adresses IP dynamiques connue

Si l'ensemble de ces cinq vérifications sont réussies, le statut est alors « OK », mais si l'une de ces vérifications échoue, le statut général pour la configuration du serveur de messagerie sera « Erreur ». Vous pouvez descendre dans la hiérarchie des résultats pour découvrir quelle vérification a échoué, ainsi que pour obtenir une description plus parlante des résultats de l'ensemble des vérifications de configuration exécutées pour l'adresse IP du serveur de messagerie respectif.

##### <span class="mw-headline" id="6e55b11b022a19036a0d3a780e011784">Confirmer qu'une entrée DNS valide existe<a name="bs-ue-jumpmark-0210253c78f68660d246d957488634f2"></a></span>

L'adresse IP du serveur de messagerie utilisée pour envoyer la campagne provient de l'en-tête de l'e-mail en lui-même, et est ensuite comparée à l'entrée DNS du serveur de messagerie. Cette vérification confirme l'existence d'une entrée DNS valide pour le serveur et joue également le rôle de contrôle de la cohérence afin de garantir que la campagne est envoyée à partir d'une même origine. Toute incohérence détectée entre l'entrée DNS et les informations contenues dans l'en-tête entraîne une diminution potentielle au niveau des taux de remise en boîte de réception.

##### <span class="mw-headline" id="9578d8104647f7f110e6a85e1a1f585c">Vérifier que le nom de domaine est correct<a name="bs-ue-jumpmark-321d886d6b0fd57d70de8ae148dcba7c"></a></span>

Lorsque l'en-tête de la campagne est examiné pour une confirmation de la présence d'un DNS valide, le nom de domaine du serveur de messagerie est également identifié. Le nom de domaine de l'entrée DNS est comparé au nom de domaine apparaissant dans l'en-tête pour s'assurer qu'ils correspondent. Toute divergence entre les informations d'entrée de domaine de l'entrée DNS et les informations contenues dans l'en-tête entraîne une diminution potentielle au niveau des taux de remise en boîte de réception.

##### <span class="mw-headline" id="482000e80efd6cb69d64749e2a796191">Confirmer que l'expéditeur n'est pas un « relais ouvert »<a name="bs-ue-jumpmark-08c8ade784edb8dbd623b12a2194480e"></a></span>

Le dénommé « relais ouvert » est un serveur de messagerie qui ne requiert aucune authentification et qui n'a aucune restriction (par ex. : les restrictions IP) pour autoriser les autres hôtes à envoyer des e-mails par son intermédiaire. Les relais ouverts sont, en règle générale, considérés comme une source potentielle de spam, et si un serveur de messagerie est signalé comme tel, cela entraînera alors une diminution des taux de remise en boîte de réception. Une fois cette vérification effectuée, un message test est envoyé au serveur pour vérifier s'il peut être transféré.

##### <span class="mw-headline" id="25bddf0539420921ca16b4f633aa4f0e">Confirmer que l'adresse IP de l'expéditeur n'est pas comprise dans une plage d'adresses IP d'accès entrant<a name="bs-ue-jumpmark-2c1a46c578d5caa22d6cc1ebd065f39b"></a></span>

L'en-tête de l'e-mail révèle également l'adresse IP du serveur de messagerie qui envoie le message, qui est ensuite vérifiée pour s'assurer qu'elle ne figure pas dans une plage d'adresses IP d'accès entrant. Les plages d'adresses IP d'accès entrant sont rendues anonymes car l'adresse IP d'origine est masquée ; la seule adresse IP visible se trouve dans la plage d'accès entrant. Ces plages d'adresses IP ne sont généralement pas utilisées pour les serveurs de messagerie de production étant donné qu'elles sont considérées comme source potentielle de spam. Tout serveur de messagerie signalé comme utilisant une telle adresse IP entraîne une potentielle diminution des taux de remise en boîte de réception.

##### <span class="mw-headline" id="9ada4ea53a92909b6e2388ece85b64db">Confirmer que l'adresse IP de l'expéditeur n'est pas comprise dans une plage d'adresses IP dynamiques connue<a name="bs-ue-jumpmark-bdf3f5a1fdf85ecd26864ccc4a595dd4"></a></span>

L'adresse IP du serveur de messagerie provenant de l'en-tête de l'e-mail est vérifiée pour confirmer l'utilisation d'une plage d'adresses IP statiques, plutôt qu'une plage connue pour émettre des adresses IP dynamiques. Tout serveur de messagerie signalé comme utilisant une telle adresse IP entraîne une potentielle diminution des taux de remise en boîte de réception.

URL du module de configuration du serveur de messagerie : [[4]](https://www.deliverywatch.net/compliance/displayServers.do)

#### <span class="mw-headline" id="801069ca2e357cc4551f4f5d01ff2398">Le module d'authentification d’e-mail<a name="bs-ue-jumpmark-7fb71122e1bc4b74cc32f478e97bd521"></a></span>

Le module d'authentification d’e-mail vérifie et s'assure que l'adresse IP du serveur de messagerie provenant de l'en-tête est autorisée à envoyer pour le compte du nom de domaine qui est listé dans l'en-tête Return-Path. La vérification s'effectue grâce à la norme Sender Policy Framework (SPF) qui permet d'identifier si l'adresse d'un expéditeur est falsifiée. Cette vérification aboutit à quatre résultats possibles :

 <table class="wikitable"><thead><tr><th>Statut</th> <th>Explication</th> </tr></thead><tbody><tr><td>Autorisé</td> <td>L'expéditeur est autorisé à envoyer pour le compte du nom de domaine contenu dans le Return-Path de l'en-tête de l’e-mail de la campagne.</td> </tr><tr><td>Neutre</td> <td>Rien ne peut être dit sur le statut d'autorisation de l'expéditeur, le message devrait être accepté par le serveur.</td> </tr><tr><td>Suspect</td> <td>L'expéditeur n'est pas autorisé à envoyer pour le compte du nom de domaine contenu dans le Return-Path de l'en-tête de l’e-mail de la campagne, mais cette erreur devrait être majoritairement gérée par le destinataire. Ce résultat est utilisé à des fins de débogage.</td> </tr><tr><td>Interdit</td> <td>L'expéditeur n'est pas autorisé à envoyer pour le compte du nom de domaine contenu dans le Return-Path de l'en-tête de l’e-mail de la campagne.</td></tr></tbody></table>Le module d'authentification de l’e-mail retournera un simple « OK » si le résultat de la vérification SPF est Autorisé. Pour les autres résultats de la vérification SPF, le résultat sera « Erreur ». Vous pouvez accéder à une description plus parlante des résultats de la vérification SPF pour la campagne en question.

URL du module d'authentification de courrier électronique : [[5]](https://www.deliverywatch.net/serverChecks/displayMailAuth.do)

### <span class="mw-headline" id="a618841ea08b5806344e98dd3c20fb03">Le module d'analyse<a name="bs-ue-jumpmark-603f96876b4ca690b1a7f40b745bcd03"></a></span>

Le module d'analyse implique 19 rapports conçus pour fournir des informations statistiques détaillées sur le taux de remise en boîte de réception pour la campagne, en fonction de caractéristiques telles que la taille de l'e-mail, le type de contenu, la fréquence d'envoi, etc.

<div class="center"><div class="floatnone">[![Sample Analytics Module report](/assets/images/2014/07/DeliveryWatch_Concepts_and_FAQ_-_Page_07_Image_0002.png)](/assets/images/2014/07/DeliveryWatch_Concepts_and_FAQ_-_Page_07_Image_0002.png)</div> </div>Le module d'analyse affiche toujours les informations de la campagne dans deux colonnes : la moyenne de la campagne client par rapport à la moyenne globale. Les paramètres du rapport peuvent être ajustés afin d'afficher les résultats, notamment la période à couvrir, le secteur d'activité, etc.

URL du module d'analyse : [[6]](https://www.deliverywatch.net/analytics/selectReport.do)

<span class="mw-headline" id="87acb06a7d4d033f882c12ab6245e4f0">Utilisation de Delivery Watch<a name="bs-ue-jumpmark-b7aba0dba001cd9f193c70f99f5c2252"></a></span>
------------------------------------------------------------------------------------------------------------------------------------------------------------------

Delivery Watch est conçu pour fournir une assistance aux clients d'emarsys souhaitant améliorer leur taux de délivrabilité et fonctionne grâce à l'utilisation d'un compte dédié à chaque client. Les clients les plus importants possèdent leurs propres comptes Delivery Watch, alors que le contenu des autres clients sera envoyé vers le compte Delivery Watch de leurs gestionnaires de comptes. Quel que soit le compte utilisé, la surveillance est généralement effectuée par le gestionnaire de comptes.

 <table class="wikitable"><thead><tr><th>Type de client</th> <th>Compte Delivery Watch</th> </tr></thead><tbody><tr><td>A  
 Clé  
 Gold</td> <td>- Configuration du compte dédié au client
- L'attribution de plusieurs comptes est possible, le cas échéant
 
</td> </tr><tr><td>B  
 C</td> <td>- Compte personnel des gestionnaires de comptes utilisé
 
</td></tr></tbody></table>### <span class="mw-headline" id="bb60c757f76eb5ef6cca7434b78f5533">Configuration d'un compte Delivery Watch<a name="bs-ue-jumpmark-a07bac03df6afcf79ced047a68149fec"></a></span>

Pour fournir une assistance technique via Delivery Watch, un compte doit être tout d'abord créé en employant les étapes suivantes :

1. Le responsable des comptes clé ou le responsable clientèle approuve la demande de configuration de compte Delivery Watch.
2. La demande de configuration de compte est envoyée à l'assistance technique de Delivery Watch avec les informations suivantes : - Nom de client
- Type de client
- Nom du gestionnaire/chargé de comptes

Les gestionnaires de comptes ou les responsables de comptes sont chargés de surveiller les résultats de délivrabilité du client dans Delivery Watch. Si un client met fin au contrat qui le lie à emarsys, le gestionnaire de comptes doit le signaler à l'assistance technique de Delivery Watch de manière à pouvoir clôturer le compte.

Si les clients étaient autorisés à accéder à leur compte Delivery Watch (par ex. : Gold, clé), le gestionnaire de compte doit mettre à jour les informations d'accès administrateur et ne fournir aux clients qu'un accès au niveau Utilisateur. Vous trouverez plus d'informations sur la manière de procéder dans un document distinct disponible auprès de l'assistance technique de 2<sup>nd</sup> niveau ou auprès de l'assistance technique de Delivery Watch elle-même.

### <span class="mw-headline" id="43c116d9546c33bcd8124ea77c5f9d38">Fournir le support de Delivery Watch<a name="bs-ue-jumpmark-b764e88aa13db1a7a46d2252d4122482"></a></span>

Pour le support de Delivery Watch, le gestionnaire de comptes constitue le premier point de contact avec les clients d'emarsys ; tous les autres clients contactent directement l'assistance technique de Delivery Watch.

Avant de contacter l'assistance technique, il est toujours bon de vérifier la documentation disponible avant de signaler des problèmes ou d'émettre une demande. Si vous êtes dans l'incapacité de résoudre le problème vous-même, veuillez-vous adresser à l'assistance technique de Delivery Watch et vous munir d'autant d'informations que possible, notamment du nom de compte et de l'emplacement du bureau.

Delivery Watch fournit à emarsys un service d'assistance par e-mail dédié pour tous les clients de Delivery Watch à l'adresse : [[7]](mailto:support@deliverywatch.com).

### <span class="mw-headline" id="73b49c8e060af30374989e06919da189">Utilisation de l'API de service web (Web Service-API, WS-API)<a name="bs-ue-jumpmark-cee20e3932966b8cb848c9e9b2f5a05f"></a></span>

Vous pouvez accéder à certains modules de Delivery Watch via une API de service web (WS-API), ce qui permet aux applications tierces d'effectuer des tests et d'afficher les résultats dans leur interface utilisateur graphique. Pour le moment, seuls le module de campagne et les modules de filtres anti-spam sont accessibles via la WS-API.

<span class="mw-headline" id="0c490fcc43d9a7a82b32a08b819d2681">Dépannage et FAQ<a name="bs-ue-jumpmark-eea75fe75d180e188fa6e54cbae63746"></a></span>
-----------------------------------------------------------------------------------------------------------------------------------------------------

La section suivante inclut plusieurs questions fréquemment posées, les problèmes les plus courants et fournit des directives quant à leur traitement.

### <span class="mw-headline" id="8a171b8d05ae5234cd982e419e503973">La campagne n'apparaît pas dans Delivery Watch<a name="bs-ue-jumpmark-c9de2090e40307d03e612cad9a9c17d6"></a></span>

Delivery Watch enregistre une nouvelle campagne dès qu'un e-mail de campagne est envoyé vers la boîte aux lettres de déclenchement (affichée en bas de la seedlist sous la forme `cdw*@deliverywatch.com`). Assurez-vous que cette adresse est incluse dans la liste de destinataires de la campagne en question ; dans le cas contraire, il vous suffit de l'ajouter.

Si le problème persiste, veuillez contacter l'assistance technique.

### <span class="mw-headline" id="42cbab3390970856b4f0732d7a2c556c">Les résultats de la campagne n'apparaissent pas dans la barre<a name="bs-ue-jumpmark-886c8698b8487747e9c7a9eed1eef66a"></a></span>

La campagne a été correctement enregistrée par le système, mais une grande partie est signalée comme manquante. Le plus souvent, les résultats apparaissent comme manquants simplement car le contenu n'était pas présent dans la boîte aux lettres lorsque le système l'a recherché.

Si 100 % du contenu de toutes les campagnes est manquant (ou pour des fournisseurs en particulier), il se peut que l'adresse n'apparaisse pas dans la seedlist et qu'elle n'ait pas été envoyée.

1. Vérifiez l'envoi des fichiers journaux pour vous assurer que les destinataires ont accepté l'e-mail via SMTP
2. Mettez à jour votre seedlist conformément à la campagne suivante

Il s'agit du problème le plus fréquent auquel sont confrontés les utilisateurs de ce système.

Dans le cas contraire, il pourrait s'agir du système qui est incapable de rechercher les résultats, même si les e-mails ont été correctement envoyés, par ex. : si les fournisseurs POP3 empêchent la consultation des dossiers autres que ceux contenus dans la boîte de réception et donc si le message est arrivé dans les courriers indésirables, il ne pourra pas être consulté.

L'autre raison à l'origine d'un grand nombre de résultats manquants tient au fait que les problèmes techniques rencontrés par les FAI empêchent Delivery Watch d'extraire les résultats des boîtes aux lettres, par ex. : temps mort.

Pour obtenir une explication plus détaillée, contactez le département de délivrabilité ou l'assistance technique de Delivery Watch.

### <span class="mw-headline" id="d49f38b54bbf8e5333dd96fc613d7c83">Qu'attendre des résultats des filtres anti-spam en attente ?<a name="bs-ue-jumpmark-0ad4201d23c967c1b8e70c03479418be"></a></span>

La vérification d'un filtre anti-spam prend généralement entre 5 et 10 minutes. Si les résultats sont toujours en attente après 10 minutes (durée maximale), cela indique donc que le système rencontre peut-être un problème. Le plus souvent, un filtre anti-spam a été corrompu, ce qui doit être signalé à l'assistance technique de Delivery Watch dès que possible.

### <span class="mw-headline" id="e6e44c4b5006231b9fffd744a753ff88">Que faire des avertissements d'authentification ?<a name="bs-ue-jumpmark-f235eaec99f50b0ac19390e7ea790551"></a></span>

Si vous recevez un avertissement d'authentification, contactez le département de délivrabilité (deliv@emarsys.com) chargé de confirmer que les configurations d'authentification du client ont été correctement effectuées. Veuillez contacter votre assistance technique locale de 2<sup>nd</sup> niveau qui peut vous aider ou transmettre le problème à l'équipe de délivrabilité en fonction des besoins.

 <table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**

 </th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">vous ne pouvez pas désactiver ces vérifications d'authentification étant donné qu'elles sont volontairement présentes afin de garantir la qualité du contenu et d'améliorer la délivrabilité.

 </td></tr></tbody></table>### <span class="mw-headline" id="eab7392c087d18ef59a9e981dd979938">Plusieurs campagnes envoyées, mais seule une campagne est visible sur le tableau de bord<a name="bs-ue-jumpmark-8df6ac3044c85265f876e9f0e149ccbf"></a></span>

Le module de campagne utilise un mécanisme spécifique pour éliminer les doubles campagnes afin d'éviter d'atteindre par erreur les limites mensuelles. Le contenu en double, par ex. les messages envoyés par erreur ou en raison d'une configuration inappropriée, est filtré par ce mécanisme qui vérifie le contenu (en-tête + corps) qu'il signale comme identique lorsqu'il y a 91 % ou plus de correspondance entre ce contenu et une campagne existante.

Tout contenu qui est signalé comme identique et envoyé dans les 24 heures après l'enregistrement de la campagne avec Delivery Watch est classé comme contenu en double, et n'est pas inclus dans le tableau de bord. Pour chaque double détecté par Delivery Watch, une notification par e-mail est automatiquement envoyée à l'adresse électronique de l'administrateur.

 <table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Notez que :**

 </th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">pour des raisons techniques, toutes les boîtes aux lettres deliverywatch.com ne sont actuellement accessibles qu'aux membres de l'équipe d'assistance technique de Delivery Watch.

 </td></tr></tbody></table>### <span class="mw-headline" id="ceed970686d37961b6f9e47ae37edffc">Processus de rapports de bugs<a name="bs-ue-jumpmark-df5ed773603a43d6da0bba3e5822a677"></a></span>

Pour tout rapport de bugs ou toute suggestion d'amélioration (par ex. : les problèmes de formatage, les informations obsolètes, etc.), veuillez contacter l'assistance technique de Delivery Watch, et vous munir d'autant d'informations que possible en utilisant l'adresse de l'assistance technique : [[8]](mailto:support@deliverywatch.com).

</div>
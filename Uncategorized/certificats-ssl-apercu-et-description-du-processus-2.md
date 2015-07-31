---
title: 'Certificats SSL - Aperçu et description du processus'
subject: ''
old_url: 'http://emarsys.dev/old/certificats-ssl-apercu-et-description-du-processus-2/'
---

<span class="mw-headline" id="2ca34a8df2b368ba655f1ac4afc0d40a">Introduction<a name="bs-ue-jumpmark-350c22a515d738a6e80118e13133b4ae"></a></span>### <span class="mw-headline" id="5d90e81c3f5b4af2180c7af584f2a915">Qu'est-ce que le protocole SSL ?<a name="bs-ue-jumpmark-b4430ccd730712999538a242fd81602e"></a></span>


----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

 Le terme Secure Socket Layer (SSL) est utilisé pour décrire un protocole visant à sécuriser les communications sur un réseau informatique et, afin d'identifier clairement les partenaires de communication, nous utilisons ce que l'on appelle des certificats SSL. Emarsys utilise des certificats SSL pour crypter l'accès à ses services ainsi qu'aux domaines liés de nos clients.

<div class="center"><div class="floatnone">[![connexion sécurisée indiquée par le navigateur Internet](/assets/images/2014/07/SSL_Cert_Process_address_bar.png)](/assets/images/2014/07/SSL_Cert_Process_address_bar.png)</div></div>#### <span class="mw-headline" id="2d4fe715aa0654a0cc25753a0a62d23a">Exemple pratique<a name="bs-ue-jumpmark-5953e305d0c2acdd1c153e41b499e3f0"></a></span>

 L'utilisation d'un formulaire d'authentification constitue une éventuelle application des certificats SSL. Dans ce cas, les utilisateurs saisissent des données personnelles, c'est pourquoi la sécurité est essentielle. Tous les formulaires contenant des données personnelles et des applications d'e-commerce doivent toujours utiliser des communications cryptées. Il en va de même pour les pages de confirmation d'inscription et de désinscription ou pour toute autre ressource Web au coeur de vos activités eMarketing : vos clients doivent toujours avoir le sentiment d'évoluer dans un environnement en ligne sécurisé. Les certificats SSL permettent au navigateur Web et au serveur Web d'établir une connexion sécurisée et cryptée. Un processus de « poignée de main » permettant d'établir la session opère en arrière-plan. Pour ce faire, le navigateur Web envoie depuis votre site Web un échantillon de fichier crypté qui sera ensuite comparé à une clé privée sur votre serveur. Une fois la connexion établie, celle-ci est désignée par une petite icône représentant un cadenas dans la barre d'adresse du navigateur et par le préfixe « https » (le « s » correspondant à « sécurisé ») de l'URL qui constituent les seules indications visibles qu'une session sécurisée est en cours. En revanche, lorsqu'un utilisateur accède à un site Web non sécurisé (par exemple, un site non protégé par un certificat SSL valide), le mécanisme de sécurité du navigateur déclenche un avertissement à l'utilisateur, lui rappelant que le site n'est pas sécurisé et que des données sensibles sont susceptibles d'être interceptées par des tiers. Confrontés à un tel avertissement, la plupart des utilisateurs hésiteront à saisir des données dans un formulaire.

<div class="center"><div class="floatnone">[![avertissement de certificat SSL](/assets/images/2014/06/SSL_Cert_Process_SSLFailure.png)](/assets/images/2014/06/SSL_Cert_Process_SSLFailure.png)</div></div> Une fois que vous avez décidé d'opter pour l'utilisation du cryptage pour communiquer avec les utilisateurs, l'objectif est qu'un site Web soit accessible sans déclencher d'avertissement. Une URL correctement exécutée devrait ressembler à ceci : `https://newsletter.yourdomain.com/u/register.php?CID=12345678&f=12345`  

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/2014/04/Icon_BeCareful.png)](/assets/images/2014/04/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">Alternativement, le lien ci-dessus peut également être converti en HTTP « normal » en retirant le S dans l'URL, mais dans ce cas, les données personnelles des utilisateurs risquent d'être subtilisées.</td></tr></tbody></table>  

### <span class="mw-headline" id="eb85aa59fd7f2f58d4ab0e5cafd324f9">Obtenir un certificat<a name="bs-ue-jumpmark-7a0ecffb5848b45c016c04961239c0d3"></a></span>

<table cellpadding="1" class="wikitable" style="width: 100%; border: 1px solid #fff;"><tbody><tr><td scope="col" style="text-align: left; border: 1px solid #fff;" width="60px">[![Icon FurtherReading.png](/assets/images/2014/04/Icon_FurtherReading.png)](/assets/images/2014/04/Icon_FurtherReading.png)</td> <td scope="col" style="border: 1px solid #fff;">Cette section part du principe que vous êtes déjà familier avec la création de formulaires dans Suite. Pour obtenir des informations supplémentaires, veuillez vous référer à la section *Aide en ligne de Suite*.</td></tr></tbody></table>  

<div class="center"><div class="floatnone">[![le processus de certification](/assets/images/2014/06/SSL_Cert_Process_Process.png)](/assets/images/2014/06/SSL_Cert_Process_Process.png)</div></div> Pour obtenir un certificat, procédez comme suit :

- Créez un fichier de demande de signature de certificat (CSR) pour le domaine que vous utilisez. Ce fichier contient des informations relatives au domaine (« whois »). Voir ci-dessous pour obtenir des informations supplémentaires sur les fichiers CSR.
- Adressez-vous à une autorité de certification (AC) et achetez un certificat.Les certificats sont disponibles pour différentes durées de contrat et pour divers systèmes d'exploitation. Il est important que vous vous assuriez de choisir le certificat le plus approprié parmi les certificats suivants : - Certificat unique pour un seul sous-domaine, par exemple « newsletter.votredomaine.com ».
- Certificat de caractères génériques pour tous les sous-domaines de premier niveau ci-dessous « *.votredomaine.com » qui vous permet de couvrir des formulaires d'inscription ainsi que des boutiques en ligne.
 
<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">le certificat doit correspondre au système d'exploitation du serveur, ce qui, dans le cas d'Emarsys, signifie sélectionner un certificat pour un système d'exploitation sous Linux.</td></tr></tbody></table>  

- Une fois que vous avez reçu le certificat de la part de l'AC, envoyez les deux fichiers suivants à Emarsys : - Fichier de clé privée (.key)
- Fichier de certificat (.crt)
- Emarsys installera ensuite le certificat et le liera au domaine (par exemple, formulaire d'inscription à une newsletter).

  

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/2014/04/Icon_BeCareful.png)](/assets/images/2014/04/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">Les certificats ne doivent pas être installés lorsque des campagnes sont en cours !</td></tr></tbody></table>  

#### <span class="mw-headline" id="8249e4a6f6cb1f70677eaf2aeddfbfa3">Fichiers CSR<a name="bs-ue-jumpmark-60964139397994ba1eca187a8f895401"></a></span>

 Une demande de signature de certificat (CSR) est un ensemble de données contenant toutes vos informations (nom de l'organisation, localisation, pays, etc.) dont vous avez besoin lorsque vous achetez un certificat auprès d'une autorité de certification (AC). L'AC utilise ces informations afin de créer le certificat SSL qui est ensuite lié au domaine pour lequel vous avez créé le CSR. C'est cette action qui rend la connexion SSL possible. Si vous avez besoin d'aide pour obtenir des informations concernant votre domaine, vous pouvez simplement utiliser le protocole Whois pour découvrir toutes les informations de domaine essentielles. Le fichier CSR étant lié au domaine, il doit être créé sur le serveur Web hébergeant votre domaine. Vous devrez peut-être contacter une personne ayant accès à ce serveur pour qu'elle vous crée le fichier CSR.  

<table cellpadding="1" class="wikitable" style="width: 100%; border: 0px;"><tbody><tr><td scope="col" style="text-align: left; border: 0px solid #999; vertical-align: top;" width="60px">[![Icon BeCareful.png](/assets/images/2014/04/Icon_BeCareful.png)](/assets/images/2014/04/Icon_BeCareful.png)</td> <td scope="col" style="border: 0px solid #999; vertical-align: top; color: #555555;">- Si votre domaine est simplement un domaine de transfert (A-Record), le fichier CSR doit être créé sur le serveur Web qui héberge le site Web
- Si vous disposez d'une entrée CNAME, supprimez-la avant d'installer le certificat.
 
</td></tr></tbody></table>  

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Please Note:**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Il est important que toutes les données contenues dans un fichier CSR correspondent exactement aux informations utilisées lors de l'application d'un certificat. Dans le cas contraire, le processus de certification pourrait échouer ou le certificat ne fonctionnera pas pour le domaine auquel il est destiné.</td></tr></tbody></table>  

#### <span class="mw-headline" id="566c1565124639a3bdbf151ef2592e20">Autorités de certification recommandées<a name="bs-ue-jumpmark-96abbab398ee68e916a3546acc747efc"></a></span>

 Emarsys recommande les autorités de certification suivantes :

- Symantec (anciennement VeriSign):<http://www.symantec.com/en/uk/ssl-certificates>
- Trustwave:<https://ssl.trustwave.com/>
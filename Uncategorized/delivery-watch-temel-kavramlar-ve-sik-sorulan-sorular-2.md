---
title: 'Delivery Watch - Temel Kavramlar ve Sık Sorulan Sorular'
subject: ''
old_url: 'http://emarsys.dev/old/delivery-watch-temel-kavramlar-ve-sik-sorulan-sorular-2/'
---

Giriş
-----

E-posta pazarlama ilk çıktığında sadece daha iyi içeriği daha hızlı bir şekilde göndermenin tek başına kampanya iletilebilirliğini geliştirmek ve kampanya penetrasyon oranını arttırmak için yeterli olmadığı kısa sürede belli oldu. E-posta, doğası gereği, internet üzerinden bilgi göndermenin güvenli bir yolu değil; bunun sonucunda da gelen kutusuna iletilme oranını tahmin etme ve gönderici kimliğini doğrulama ihtiyacı ortaya çıktı.

Delivery Watch, herhangi bir e-posta kampanyasının gönderilmesinde meydana gelebilecek her türlü potansiyel iletilebilirlik sorununu analiz etme ve ele alma, dolayısıyla da kampanyanın kalitesini sağlama amacıyla geliştirilen bir araç setidir. Bu araç seti, iletilebilirlik ve dolayısıyla göndericinin itibarı üzerinde olumsuz etki yaratabilecek potansiyel sorunları tespit etmek için kampanyanın çeşitli yönlerini değerlendirerek çalışır.

Delivery Watch, iletilebilirlik oranlarını maksimize etmek için aşağıdaki modülleri kullanarak gönderim sırasında bir kampanyayı tüm yönleriyle test eder:

- Kampanya Modülü (Campaign Module)
- Spam Filtresi Modülü (Spamfilter Module)
- İzleme Modülü: Kara Liste, Mail Sunucu Konfigürasyonu, Mail Doğrulama (Monitoring Module: Blacklist, Mailserver Config, Mail Authentication)
- Analiz Modülü (Analysis Module)

Her modül, kampanyanın spesifik bir yönünü test etmek için tasarlanmış olup en sık suiistimal edilen zayıflıkları (örneğin spamming, spoofing, vs.) belirlemek için gerek kampanya, gerekse göndericiyi analiz eder. Bu hizmetten yararlanılarak, bir kampanyanın iletilebilirliğini maksimize etme amacıyla her türlü olası konfigürasyon veya itibar sorunları işaretlenebilir ve ele alınabilir.

<span class="mw-headline" id="fceb08789a991784429b8e0ba7af765c">Delivery Watch Araç Seti<a name="bs-ue-jumpmark-c11f64dd71b244ebe9ed353687ea9a0d"></a></span>
-------------------------------------------------------------------------------------------------------------------------------------------------------------

Delivery Watch araç seti, e-posta iletilebilirliğinin karmaşık manzarası karşısında itibar yaratmak için otomatize edilmiş izleme servisleri sunan entegre bir çözümdür. Politikaları uygulayan en büyük e-posta sağlayıcılardan kara liste/güvenilir gönderici listeleri, domain bazlı itibar puanı, vs. gibi anti-spam önlemleri kullanan kişilere kadar çeşitli oyunculara göre içeriği aktif olarak değerlendirir.

Araç setinin dört ana modülü, her kampanyanın davranışını iletilebilirliği etkileyen çeşitli kriterlere göre ölçer.

<table border="0" class="wikitable" style="width: 100%;"><thead><tr><th>Modülün Adı</th> <th>Kapsamı</th> </tr></thead><tbody><tr><td>Kampanya Modülü</td> <td>Bilinen tüm tanınmış e-posta sağlayıcılarında belli bir sayıda aktif posta kutusu bulundurup, ilgili gelen kutularına iletilme oranlarını tespit ederek genel ISP iletilebilirliğini test eder.</td> </tr><tr><td>Spam Filtresi Modülü</td> <td>Kampanyanın nasıl kategorize edileceğini değerlendirmek için sunucu ve istemci tarafında çeşitli eklentiler (plug-in) ve harici bulut bazlı hizmetlerin bir kombinasyonunu kullanarak içeriği tüm önemli spam filtrelerine karşı test eder.</td> </tr><tr><td>İzleme Modülü</td> <td>Çeşitli e-posta doğrulama kontrollerini, kara listeleri ve “standart kullanmama” uygulamalarını izleyerek e-postayı gönderen sunucunun konfigürasyonunu ve itibarını test eder.</td> </tr><tr><td>Analiz Modülü</td> <td>Diğer modüllerin gerçekleştirdiği testler bazında kampanyanın içeriğini analiz ederek bilgi verir.</td></tr></tbody></table>### <span class="mw-headline" id="407c40a6041b25deadf7a9f58ab5f074">Kampanya Modülü<a name="bs-ue-jumpmark-97944223ca1a830dbf6831cb1063cdea"></a></span>

Kampanya Modülü, bir e-posta kampanyasının iletilebilirliğini her ISP’de kurulu olan bir dizi posta kutusunu kullanarak dünya çapında çeşitli büyük ISP’ler bazında test ederek çalışan bir ISP takip hizmeti sunar. Kampanyanın bu posta kutularından elde edilen sonuçları, daha sonra ISP’ler için test sonuçları bazında gelen kutusu iletilebilirlik oranlarını hesaplamak için kullanılabilir.

Test için kullanılan bu posta kutularına **seedlist** adı verilir; Delivery Watch, test kampanyalarının iletilebilirlik sonuçlarını izler ve kampanyayı her ISP için “pass”, “spam” veya “blocked/missing” (“geçer”, “spam”, “bloke edilmiş/eksik”) olarak kategorize eder. Bu ‘seedlist’ bölgelere göre (Kuzey Amerika, Almanca konuşulan ülkeler, vb.) gruplanır. Delivery Watch tarafından bölgelere göre görüntülenen bu listede ayrı ISP posta kutuları ve ülke bazında ayrıntılı inceleme yapabilirsiniz.

İzleme süreci, kampanya mesajının bir kopyası (“tetikleyici e-posta”) seedlist’in bir parçası da olan bir Delivery Watch posta kutusuna gönderildiğinde başlar. Tetikleyici e-posta, Delivery Watch’a yeni bir kampanyanın gönderildiğini ve proses edilmeyi beklediğini söyler. ISP izleme hizmeti, tetikleyici e-postanın içeriğini seedlist’teki posta kutularındaki benzerleriyle karşılaştırır.

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Lütfen Dikkat:**

 </th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">İçeriği aynı olan ve 24 saat içinde ulaşan iki kampanya, *eşit* kabul edilir; buna karşın içerikleri aynı olsa bile aralarında 24 saatten fazla olursa *farklı* kabul edilirler.

 </td></tr></tbody></table>  
 Her kampanyaya özgün bir başlık verilerek bu davranıştan kaçınmak mümkündür; böylece başlığı belirleyici olarak kullanıp kampanya eşleştirmesi yapılabilir.

Kampanya Modülü linki: [[1]](https://www.deliverywatch.net/campaign/listCampaigns.do)

### <span class="mw-headline" id="80012b90d3bd96eea6a96a7b4930b69c">Spam Filtresi Modülü<a name="bs-ue-jumpmark-e606348d57182fbc04b99b5b6038c0b9"></a></span>

Spam Filtresi Modülü, bir e-posta kampanyasının iletilebilirliğinin mevcut en yaygın spam filtrelerine göre test edilmesini sağlar. Modül, bu şekilde kampanyayla ilgili herhangi bir potansiyel sorunu tespit edebilir. Bu modül, tetikleyici mesajı spam filtresi ortamına yönlendiren ve kampanyayı mevcut anti spam teknolojileri bazında test eden dahili bir Delivery Watch posta kutusu kullanır.

E-posta kampanyasının bir kopyası, posta kutusuna gönderilir; bu işlem spam filtresi testini başlatır ve gerek spam filtresi bazında sonucu gerekse genel bir özet sunar. Her spam filtresi, içeriği “Gelen Kutusu”, “Spam” veya “Beklemede” şeklinde işaretler ve bunun yanı sıra desteklenen anti spam teknolojileri için genel bir spam filtresi sonucu sunar. Spam Filtresi Modülü linki: [[2]](https://www.deliverywatch.net/spamfilter/listReports.do)

### <span class="mw-headline" id="8f88d6b3daec49ec0b35a2935409ef17">İzleme Modülü<a name="bs-ue-jumpmark-10892d9c83e3874d70f2d9dcdd7cad61"></a></span>

İzleme modülü, Delivery Watch müşterilerinin kampanyalarını gönderirken kullandığı mail sunucularının konfigürasyonunu ve itibarını optimize etmek için tasarlanmıştır. İzleme Modülü bunu başarmak için üç alt modülden oluşur:

- Kara Liste Modülü (Blacklist Module)
- Mail Sunucusu Konfigürasyon Modülü (Mailserver Configuration Module)
- Mail Doğrulama Modülü (Mail Authentication Module)

ISP İzleme (Kampanya Modülü) için Delivery Watch’a gönderilen her türlü e-posta kampanyasının başlığı, İzleme Modülü tarafından otomatik olarak incelenir ve DNS bilgileriyle kıyaslanır.

#### <span class="mw-headline" id="3a7f919c68183a693fb06023b9cee0b8">Kara Liste Modülü<a name="bs-ue-jumpmark-6448388acbbfcba812d3869d9344719d"></a></span>

Kara Liste Modülü, en saygın ve önemli kara listeler bazında periyodik kontroller gerçekleştirerek göndericinin IP adresinin veya Return-Path domainin herhangi bir kara listede görülmediğini kontrol eder. Bir DNS sorgulaması kullanılarak mail sunucunun durumu ya “OK” ya da “Hata” olarak getirilir; burada altta yatan sebebi, örneğin neden kara listeye alındığını, derinlemesine görme seçeneği de bulunmaktadır.

Kara Liste Modülü linki: [[3]](https://www.deliverywatch.net/blacklist/listServers.do)

#### <span class="mw-headline" id="b9740e7a04996d7f31130f202a9e5bd3">Mail Sunucusu Konfigürasyon Modülü<a name="bs-ue-jumpmark-66ddfd3f85c4162a1bfcf0546c2c7267"></a></span>

Mail Sunucusu Konfigürasyon Modülü, beş tür konfigürasyon kontrolü gerçekleştirilir. Diğerlerinin yanı sıra, gönderen mail sunucusuyla ilgili kampanya e-postasının başlığındaki bilgileri de doğrular:

- Geçerli bir DNS kaydının varlığını teyit etme
- Domain adının doğruluğunu teyit etme
- Göndericinin bir “Open Relay” olmadığını onaylama
- Göndericinin IP adresinin bir Dial-In IP aralığında olmadığını teyit etme
- Göndericinin IP adresinin bilinen dinamik bir IP aralığında olmadığını teyit etme

Bu beş kontrolün tümü başarıyla sonuçlanırsa, durum “OK” olur; ancak bu kontrollerden herhangi biri başarısız olursa, Mail Sunucusu Konfigürasyonu için genel durum “Hata” olacaktır. Hangi kontrolün başarısız olduğunu detaylı olarak görebilir, ilgili mail sunucusunun IP adresi için yapılan konfigürasyon kontrollerinin açıklamalarını inceleyebilirsiniz.

##### <span class="mw-headline" id="6d38227fb1045ebb5117c2a6de170a87">Geçerli bir DNS kaydının varlığını teyit etme<a name="bs-ue-jumpmark-5f34276489344f654ab1240f5976e703"></a></span>

Kampanya gönderimi için kullanılan mail sunucusunun IP adresi e-postanın başlığından alınır ve ardından mail sunucusu için DNS kaydı ile karşılaştırılır. Bu kontrol, sunucu için geçerli bir DNS kaydının varlığını teyit eder ve aynı zamanda kampanyanın aynı kaynaktan gönderildiğinden emin olmak için bir tutarlılık kontrolü gibi hareket eder. DNS kaydı ile başlığın içerdiği bilgiler arasındaki herhangi bir tutarsızlık, gelen kutusuna iletilebilirlik oranlarında düşme potansiyeli yaratır.

##### <span class="mw-headline" id="7c349b172026f075154da99348ec31fa">Domain adının doğruluğunu teyit etme<a name="bs-ue-jumpmark-07c30bb2eddd562fa90bb715f49cd015"></a></span>

Geçerli bir DNS kaydının varlığını teyit etmek için kampanyanın başlığı incelendiğinde mail sunucusunun domain adı da tespit edilir. DNS kaydındaki domain adı, başlıktaki domain adıyla aynı olduğunu kontrol etmek üzere karşılaştırılır. DNS kaydı ile başlığın içerdiği bilgiler arasındaki herhangi bir tutarsızlık, gelen kutusuna iletilebilirlik oranlarında düşme potansiyeli yaratır.

##### <span class="mw-headline" id="d933c8ca93c06067f98696eae5e36bde">Göndericinin bir “Open Relay” olmadığını onaylama<a name="bs-ue-jumpmark-ce4dfe480c934de3c3fa5b5e9b8425c8"></a></span>

'Open Relay', herhangi bir doğrulama gerektirmeyen veya diğer host’ların onun üzerinden e-posta göndermesi konusunda herhangi bir sınırlama (örneğin IP sınırlaması) olmayan bir mail sunucusudur. Open Relay’ler genellikle olası bir spam kaynağı olarak değerlendirilir ve bir mail sunucusu bu şekilde işaretlenirse, gelen kutusuna iletilebilirlik oranlarında düşme potansiyeli yaratır. Bu kontrol yapıldığında yönlendirilip yönlendirilemediğini görmek için sunucuya bir deneme mesajı gönderilir.

##### <span class="mw-headline" id="26946dd547488824ab8d64b39b7bd739">Göndericinin IP adresinin bir Dial-In IP aralığında olmadığını teyit etme<a name="bs-ue-jumpmark-69240f43681e118fd39bef7530f90e53"></a></span>

E-postanın başlığı, aynı zamanda mesajı gönderen mail sunucusunun IP adresini de açığa çıkarır; bir Dial In IP aralığında olmadığı kontrol edilir. Dial-In IP aralıkları anonimdir çünkü kaynak IP adresi gizlenmiştir ve görünen tek IP adresi dial in aralığındadır. Bu IP aralıkları genelde üretim mail sunucular için kullanılmaz çünkü olası bir spam kaynağı olarak değerlendirilirler. Bu tür bir IP adresi kullandığı işaretlenen herhangi bir mail sunucusu, gelen kutusuna iletilebilirlik oranlarında düşme potansiyeli yaratır.

##### <span class="mw-headline" id="39c66591e98fea3aaf95c53e2b16734b">Göndericinin IP adresinin bilinen dinamik bir IP aralığında olmadığını teyit etme<a name="bs-ue-jumpmark-523266d72bdd566f5455d60dba7c71ab"></a></span>

E-posta başlığındaki mail sunucusunun IP adresi, dinamik IP adresleri ürettiği bilinenlerden ziyade statik bir IP adresi aralığı kullandığından emin olmak için kontrol edilir. Bu tür bir IP adresi kullandığı işaretlenen herhangi bir mail sunucusu, gelen kutusuna iletilebilirlik oranlarında düşme potansiyeli yaratır.

Mail Sunucusu Konfigürasyon Modülü linki: [[4]](https://www.deliverywatch.net/compliance/displayServers.do)

#### <span class="mw-headline" id="4378b4571257db1ec1fedb908b670cfc">Mail Doğrulama Modülü<a name="bs-ue-jumpmark-d5d89f27444d3054235e6527326a4189"></a></span>

Mail Doğrulama Modülü, başlıktan alınan mail sunucusunun IP adresinin Return-Path başlığında yer alan domain adına gönderim yapmaya yetkili olduğunu kontrol eder. Bu kontrol, gönderici adresinin sahte olup olmadığını kontrol eden SPF (Sender Policy Framework – Gönderici Politikaları Çerçevesi) kullanılarak gerçekleştirilir. Bu kontrolün dört sonucu olabilir:

<table class="wikitable"><thead><tr><th>Durum</th> <th>Açıklama</th> </tr></thead><tbody><tr><td>Geçer (Pass)</td> <td>Gönderici, kampanya mesajının başlığındaki Return-Path’in içerdiği domain adına gönderim yapmaya yetkilidir.</td> </tr><tr><td>Nötr (Neutral)</td> <td>Göndericinin yetki durumu hakkında herhangi bir şey söylenemez, mesaj sunucu tarafından kabul edilmelidir.</td> </tr><tr><td>Yumuşak Hata (Soft-Fail)</td> <td>Gönderici, kampanya mesajının başlığındaki Return-Path’in içerdiği domain adına gönderim yapmaya yetkili değildir, fakat alıcı bu hatayı toleranslı olarak değerlendirmelidir. Bu sonuç, hatalardan arındırma amaçlıdır.</td> </tr><tr><td>Hata (Fail)</td> <td>Gönderici, kampanya mesajının başlığındaki Return-Path’in içerdiği domain adına gönderim yapmaya yetkili değildir.</td></tr></tbody></table>Mail Doğrulama Modülü, yalnızca SPF kontrolü sonucu Geçer is “OK” verecektir; SPF kontrolündeki diğer sonuçlarda durum “Hata” olacaktır. İlgili kampanya için SPF kontrolünün sonuçlarını detaylı olarak görebilir, açıklamaları inceleyebilirsiniz.

Mail Doğrulama Modülü linki: [[5]](https://www.deliverywatch.net/serverChecks/displayMailAuth.do)

### <span class="mw-headline" id="a638d363b103e2a33b111dc91b871e58">Analytics Modülü<a name="bs-ue-jumpmark-9f39684153ddd2c23253337a81f17893"></a></span>

Analytics Modülü, e-posta büyüklüğü, içerik türü, gönderim sıklığı gibi özellikleri baz alarak kampanyanın gelen kutusuna iletilebilirliği hakkında ayrıntılı istatistiki bilgiler sunmak üzere tasarlanmış 19 rapordan oluşmaktadır.

<div class="center"><div class="floatnone">[![Örnek Analytics Modülü raporu](/assets/images/2014/07/DeliveryWatch_Concepts_and_FAQ_-_Page_07_Image_0002.png)](/assets/images/2014/07/DeliveryWatch_Concepts_and_FAQ_-_Page_07_Image_0002.png)</div></div>Analytics Modülü, kampanya bilgilerini her zaman hesabın kampanya ortalaması ve küresel ortalama olmak üzere iki sütun halinde sunar. Raporun parametreleri, hangi zaman aralığının dikkate alınacağı, sektör gibi faktörleri içerecek şekilde ayarlanabilir.

Analytics Modülü linki: [[6]](https://www.deliverywatch.net/analytics/selectReport.do)

<span class="mw-headline" id="52d9c400f3071692ad275e352ab52ec8">Delivery Watch ile çalışma<a name="bs-ue-jumpmark-1a93ca10c91e5abaa78bc04934da38c9"></a></span>
---------------------------------------------------------------------------------------------------------------------------------------------------------------

Delivery Watch, iletilebilirlik oranlarını iyileştirmek isteyen emarsys müşterilerine destek vermek için tasarlanmıştır ve her müşteriye ayrılan bir hesabı kullanarak çalışır. Daha büyük müşterilere kendi Delivery Watch hesapları verilirken, diğerlerinin içeriği müşteri yöneticilerinin Delivery Watch hesaplarına gönderilir. Hangi tür hesap olursa olsun, izleme genellikle müşteri yöneticisi tarafından yürütülür.

<table class="wikitable"><thead><tr><th>Müşteri Türü</th> <th>Delivery Watch Hesabı</th> </tr></thead><tbody><tr><td>A  
 Key  
 Gold</td> <td>- Müşteri için ayrı bir hesap kurulumu yapılır
- İhtiyaç olması halinde birden fazla hesap kurulabilir
 
</td> </tr><tr><td>B  
 C</td> <td>- Müşteri yöneticilerinin kendi hesapları kullanılır
 
</td></tr></tbody></table>### <span class="mw-headline" id="a7f539608da01d6efd2dc15115925fd8">Delivery Watch hesabının kurulumu<a name="bs-ue-jumpmark-b8218b845597392b2fc7d6de30e49283"></a></span>

Delivery Watch kullanılarak destek verilebilmesi için önce aşağıdaki adımlar takip edilerek bir hesap yaratılması gerekir:

1. Müşteri Direktörü veya Müşteri Hizmetleri Yöneticisi hesap kurulum talebini onaylar.
2. Hesap kurulum talebi aşağıdaki bilgilerle beraber Delivery Watch destek birimine iletilir: - Müşteri Adı
- Müşteri Türü
- Müşteri Yöneticisinin Adı

Müşteri temsilcileri veya yöneticileri, müşterinin iletilebilirlik sonuçlarını Delivery Watch’ta takip etmekten sorumludur. Bir müşteri Emarsys ile sözleşmesini sona erdirirse, hesabın kapatılması için müşteri yöneticisinin bu durumu Delivery Watch destek birimine bildirmesi gerekir.

Müşterilere (örneğin A, Gold, Key) Delivery Watch hesapları için erişim verildiyse, müşteri yöneticisinin admin seviyesinde erişimi olmalı ve müşterinin sadece kullanıcı seviyesinde erişimi olmalıdır. Bunun nasıl yapılacağını açıklayan daha ayrıntılı bir doküman ikinci seviye destek veya Delivery Watch destekten sağlanabilir.

### <span class="mw-headline" id="d56dd774652fa6772279c33fd9d86676">Delivery Watch Desteğinin Sağlanması<a name="bs-ue-jumpmark-546838c4235076e4fcf1f8042fba19f2"></a></span>

Delivery Watch desteği açısından müşteri yöneticisi, emarsys müşterileri için ilk temas noktası olarak hareket eder; diğer tüm müşteriler doğrudan Delivery Watch ile iletişime geçer.

Destek birimiyle iletişime geçmeden önce sorularınızı veya sorunlarınızı ele alan dokümanların olup olmadığını kontrol etmek yararlı olabilir. Sorunu kendi başınıza çözemediğiniz takdirde hesap adı ve ofis konumu da dahil olmak üzere mümkün olduğunca fazla bilgiyle Delivery Watch desteğe başvurun.

Delivery Watch, Emarsys’e tüm Delivery Watch müşterileri için özel e-postayla destek hizmeti sunmaktadır: [[7]](mailto:support@deliverywatch.com).

### <span class="mw-headline" id="fcc310d15e03d7696e74984e1b4e4fd8">Web Service-API (WS-API) kullanımı<a name="bs-ue-jumpmark-4856220f9ffea06a69b29f473dd93a57"></a></span>

Delivery Watch modüllerinin bazıları bir Web Service-API (WS-API) kullanılarak erişilebilir. WS-API, üçüncü parti aplikasyonların kendi testlerini yapmasına ve sonuçları kendi genel kullanıcı ara yüzlerinde görüntülemesine olanak verir. Hali hazırda sadece Kampanya Modülü ve Spam Filtresi Modüllerine WS-API aracılığıyla erişilebilmektedir.

<span class="mw-headline" id="e8f54901c5b25e4a2ccbc6ffda68191e">Sorun Giderme ve SSS<a name="bs-ue-jumpmark-3b9c18b8b539572b5aee6cdc2fae8348"></a></span>
---------------------------------------------------------------------------------------------------------------------------------------------------------

Bu bölümde sık sorulan bazı sorularla yaygın karşılaşılan bazı sorunlar ele alınmakta ve bunların çözülmesine yönelik öneriler sunulmaktadır.

### <span class="mw-headline" id="2dad3c0c8028539432e4dbafc918321a">Kampanya Delivery Watch’ta görünmüyor<a name="bs-ue-jumpmark-4ba70924e9e671ecba3e436f35580c61"></a></span>

Bir kampanyanın e-postası tetikleyen posta kutusuna iletildiği anda Delivery Watch kampanyayı kaydeder (seedlist’in altında `cdw*@deliverywatch.com` şeklinde gösterilir). Bu adresin ilgili kampanyanın alıcı listesinde yer aldığından emin olun; eksikse ekleyin.

Sorun çözülmezse destek ile iletişime geçin.

### <span class="mw-headline" id="547fd6ba9506c3a082760f441b55ebd9">Kampanya sonuçları çubukta yer almıyor<a name="bs-ue-jumpmark-5df7346ac69f054c6a895a19a84b36ce"></a></span>

Kampanya sisteme başarıyla kaydedildiği halde büyük bir kısmı eksik olarak işaretlenmiş. Sonuçların eksik olarak işaretlenmesinin en yaygın nedenlerinden biri, sistem sorgulama yaptığında içeriğin posta kutusunda olmamasıdır.

Kampanyaların % 100’ü tümü (veya belli sağlayıcılar) için eksikse, bu takdirde sebebi adreslerin seedlist’te olmaması ve dolayısıyla gönderilmemesi olabilir.

1. Alıcıların e-postayı SMTP kullanarak kabul ettiğinden emin olmak için gönderim log dosyalarını kontrol edin.
2. Sonraki kampanyada seedlist’inizi buna göre güncelleyin.

Kullanıcıların sistemde en sık karşılaştığı sorun budur.

Alternatif olarak e-postlar başarıyla iletilmesine rağmen, sistem sonuçları sorgulayamamış olabilir; örneğin POP3 sağlayıcılar gelen kutusu dışındaki klasörlerin görüntülenmesini engelleyebilir ve dolayısıyla mesaj spam klasörüne gittiyse görüntülenemez.

Çok sayıda sonucun eksik olmasının bir başka nedeni, ISP’lerin Delivery Watch’ın posta kutularından sonuç almasını engelleyen teknik sorunlar ve arızalar yaşaması olabilir.

Daha detaylı açıklama için İletilebilirlik birimi veya Delivery Watch destek ile iletişime geçebilirsiniz.

### <span class="mw-headline" id="b91f138ad8e8b00014a7ea6ded8970a3">Beklemede olan Spam Filtresi sonuçları hakkında<a name="bs-ue-jumpmark-efafbe215fc53d202a739b91d5b658a9"></a></span>

Bir spam filtresi kontrolü yaklaşık 5-10 dakika sürer. 10 dakika (maksimum süre) geçtiği halde sonuçlar hala beklemede ise sistemde bir sorun olabileceğine işaret eder. Bunun olmasının en yaygın nedeni, bir spam filtresinin bozulmuş olmasıdır ve mümkün olduğunca kısa zamanda Delivery Watch desteğe bildirilmesi gerekir.

### <span class="mw-headline" id="1030b58aae57874ce9cdd79f1a52c576">Doğrulama uyarıları için ne yapmalı<a name="bs-ue-jumpmark-9e1ab0e39174db3cd34899a544659b47"></a></span>

Bir doğrulama uyarısı alırsanız, müşteri doğrulama kurulumlarının doğru şekilde yapılmasını sağlamakla yükümlü İletilebilirlik birimi ([[8]](mailto:deliv@emarsys.com)) ile iletişim kurun. Yardımcı olması için ikinci seviye destek veya gerekiyorsa İletilebilirlik ekibiyle görüşün.

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Lütfen Dikkat:**

 </th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">İçeriğin kalitesini sağlamak ve iletilebilirliği artırmak için bilerek uygulanan doğrulama kontrollerini kapatamazsınız.

 </td></tr></tbody></table>### <span class="mw-headline" id="71f4e0152fedf69d952d3b0b71e09b4b">Birden fazla kampanya gönderildiği halde sadece biri konsolda görünüyor<a name="bs-ue-jumpmark-30b6f5843f04fcc66d1ead20c788118c"></a></span>

Kampanya modülü, aynı kampanyaları filtrelemek ve aylık limitlerin yanlışlıkla tüketilmesine engel olmak için spesifik bir mekanizma kullanır. Yanlışlıkla veya hatalı kurulum nedeniyle gönderilen aynı içerik bu mekanizma tarafından filtrelenir; bu içerikle mevcut bir kampanya arasında başlık ve gövde olarak % 91 ve daha fazla aynı içerik varsa, aynı olarak işaretlenir.

Aynı olarak işaretlenen ve ilk kampanyanın Delivery Watch tarafından kaydedilmesinden sonraki 24 saat içinde gönderilen her türlü içerik aynı olarak sınıflandırılır ve konsolda gösterilmez. Delivery Watch tarafından aynı olduğu tespit edilen her içerik için admin e-posta adresine bir bildirim mesajı gönderilir.

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**Lütfen Dikkat:**

 </th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">Teknik nedenlerle tüm deliverywatch.com posta kutularına halen sadece Delivery Watch destek ekibi üyeleri erişebilmektedir.

 </td></tr></tbody></table>### <span class="mw-headline" id="2a4811cb4d6762ef6227d33d53a337db">Hata bildirme süreci<a name="bs-ue-jumpmark-822f52d62f8d3a5b096c13091deca695"></a></span>

Herhangi bir hata bildirmek veya iyileştirme önerilerinde (örneğin biçimlendirme sorunları, geçerliliği kalmamış bilgiler, vs.) bulunmak için lütfen mümkün olduğunca fazla bilgiyle donanmış olarak Delivery Watch destek ile şu adresten iletişim kurun: [[9]](mailto:support@deliverywatch.com).
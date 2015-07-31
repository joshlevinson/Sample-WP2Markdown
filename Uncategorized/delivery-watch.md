---
title: 'Delivery Watch - 基本概念和常见问题'
subject: ''
old_url: 'http://emarsys.dev/old/delivery-watch/'
---

介绍
--

 当电子邮件营销首次出现时，随即明朗的是：以较快的速度发送改进的内容本身不足以提高活动送达率和活动渗透率。就其性质而言，电子邮件通过互联网发送信息，是不太牢靠的，因此，人们对评估收件箱送达率以及发件者的身份的需求出现了。 Delivery Watch是一个工具包，设计用来分析和解决指定电子邮件活动发送过程中可能出现的递交问题，从而保证活动质量。此工具包通过评估活动的若干方面，从而识别对于送达率以及发送者的声誉具有负面影响的潜在问题。 在发送过程中，Delivery Watch检测活动的所有方面，并通过使用下列模块帮助实现送达率的最大化：

- 活动模块（Campaign Module）
- 垃圾邮件过滤器模块（Spamfilter Module）
- 监测模块（Monitoring Module）（黑名单、邮件服务器配置、邮件验证（Blacklist、MailserverConfig、Mail Authentication））
- 分析模块（Analysis Module）

 每个模块均设计用于检测电邮活动的某个特定方面，同时分析电邮活动和发件者，对最容易被利用的弱点（如垃圾邮件、诈骗活动等等）进行识别。通过提供这种服务，可对任何潜在的配置事项或者声誉事项进行标记和定位，从而有助于电邮活动送达率的最大化。

Delivery Watch工具包
-----------------

 Delivery Watchtool-kit是一个集成的解决方案，为复杂的邮件递交性以及由此建立的声誉提供自动化的监测服务。该服务对当前各种参与者所用的一系列策略强化机制进行积极评估，包括大型电子邮件提供商到个人，这些用户会使用黑白名单以及以域名为基础的声誉评分等机制。 工具包的四种主要核心模块能够利用影响送达率的不同要素，从而对不同电邮活动的行为进行评估。

<table border="0" class="wikitable" style="width: 100%;"><thead><tr><th>模块名称</th> <th>适用范围</th> </tr></thead><tbody><tr><td>Campaign Module 电邮活动模块</td> <td>通过维持大量活跃邮箱，对所有主要邮件提供商的普通ISP递交能力进行检测，从而对各自收件箱的送达率进行评估。</td> </tr><tr><td>Spamfilter Module 垃圾邮件过滤器</td> <td>使用服务器侧插件、客户端侧插件和外部云服务的混合体，以所有主要的垃圾过滤器为基础对内容进行检测，以便评估它们是如何分类电邮活动的。</td> </tr><tr><td>Monitoring Module 监测模块</td> <td>通过监测各种邮件身份检查、黑名单和标准的无效实践，对邮件发送服务器的配置及声誉进行检测。</td> </tr><tr><td>Analysis Module 分析模块</td> <td>基于其他模块完成的测试，提供有深刻见解的电邮活动内容分析。</td></tr></tbody></table>### 电邮活动模块

 电邮活动模块提供ISP跟踪服务，此服务的机制通过在每个ISP上建立的一系列测试邮件箱，从而对世界上各种主要ISP的电邮活动邮箱的递交能力进行检测。这些电邮活动邮箱可以测试结论为基础来计算预期的收件箱送达率。 这些测试邮件箱被称为种子列表（seedlist），Delivery Watch通过把每个ISP的结果分类为“合格”、“垃圾”或“拦截/丢失”，从而对电邮活动递交能力进行监测。该种子列表可以按地区分组（北美、DACH等等），因此Delivery Watch按地区显示结果，这样您就能够按国家分类细化到每一个ISP邮箱。 当一份电邮活动邮件（称为“触发器邮件”）被发送到Delivery Watch邮箱时，跟踪过程被启动，该过程是种子列表的一部分。触发器邮件通知Delivery Watch：已经发送了一个新的电邮活动并等待处理。随后，ISP跟踪服务会对触发器中的内容与来自种子列表邮箱内的相应部分进行比较。

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**请注意：**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">如果内容相同并且在24小时内到达，则两个电邮活动被视为同一活动，但是如果它们24小时以后到达，即使内容是相同的，也会被认定为不同。</td></tr></tbody></table> 通过确保把唯一的标头添加到每个电邮活动中，您有可能避免这种现象，然后把标头做为标识符对电邮活动的进行匹配。 Campaign模块URL: [[1]](https://www.deliverywatch.net/campaign/listCampaigns.do)

### <span class="mw-headline" id="2907590b7b86ea1cc3973f0f16c730f0">垃圾邮件过滤模块<a name="bs-ue-jumpmark-850758109f0801aa4fd99ca7477ec3c8"></a></span>

 垃圾邮件过滤（Spamfilter）模块通过使用一系列最广泛使用的垃圾邮件过滤器，从而对电邮活动的递交能力进行监测。这种方法使得模块能够识别电邮活动中的潜在问题。这个模块使用内部的Delivery Watch邮箱，该邮箱将触发器邮件提交给垃圾邮件过滤器环境，并在此环境中测试可用的反垃圾邮件技术。 当一份电邮活动发送到邮箱中，邮箱启动垃圾邮件过滤器进行检测，同时提交垃圾邮件过滤器结果以及结果的整体汇总。每个垃圾邮件过滤将把内容标记为“收件箱”、“垃圾箱”或“待定”，以及支持反垃圾邮件技术的整体垃圾邮件过滤器结果。 Spamfilter 模块 URL: [[2]](https://www.deliverywatch.net/spamfilter/listReports.do)

### 监测模块

 当发送他们的电邮活动时，Monitoring模块设计用来帮助优化Delivery Watch客户所用的邮件服务器配置和声誉。为了实现这一目标，Monitoring模块内包含了三个子模块。

- Blacklist（黑名单）模块
- Mailserver Configuration （邮件服务器配置）模块
- Mail Authentication （邮件验证）模块

 任何发送到Delivery Watch用于ISP跟踪（Campaign模块）的电邮活动都将自动接受标头检查，并且通过Monitoring模块与DNS信息进行对比。

#### 黑名单模块

 通过针对一些最为突出和重要的黑名单进行定期的检查，黑名单模块确保了发件人的IP地址或者Return-Path返回域名不会出现在黑名单上。通过使用DNS查询，邮件服务器的状态返回为“正常”或“错误”，同时还具有追踪发现潜在错误原因的功能选项，例如被列入黑名单的原因。 黑名单模块 URL: [[3]](https://www.deliverywatch.net/blacklist/listServers.do)

#### 电邮服务器配置模块

 电邮服务器模块进行五种类型的配置检查。其中的一项功能是校验与发送邮件服务器相关的电邮活动标头内的信息。下面是检查的一部分项目：

- 确认存在有效的DNS条目
- 检验域名是否正确
- 确认发件人不是“开放转发”
- 确认发件人的IP地址不是处于拨入范围内
- 确认发件人的IP地址并非处于已知的动态IP范围

 如果所有这些检查成功，则状态为“正常”，如果任何一项失败，则电邮服务器的整体状态为“错误”。您可以进行追踪发现检查项发生错误的更多细节以及各自邮件服务器IP地址上运行的所有配置检查结果的详细说明。

##### 确认存在有效的DNS条目

 用于发送电邮活动的邮件服务器IP地址是从邮件标头自身提取的，然后与邮件服务器的DNS条目进行比较。这种检查确认了服务器中有效DNS条目的存在，并且执行一致性检查以确保电邮活动是从同样的来源发送的。如果在DNS条目和标头的信息之间检测到不一致性，则可能会导致收件箱送达率降低。

##### 检验域名是正确的

 当执行电邮活动标头检查用于确认是否存在有效的DNS时，邮件服务器的域名也被确认。同时还会将DNS条目的域名与标头中的域名进行对比，确定是否匹配。如果DNS条目中的域名条目信息与标头信息不一致，则可能会导致收件箱送达率降低。

##### 确认发件人不是“开放转发”

 所谓的“开发转发”是指不需要任何验证，或者不限制其他主机经由它发送邮件（例如IP限制）的邮件服务器。开放转发通常被认为是垃圾邮件的可能来源，如果一台邮件服务器被标记为开放转发，那么其潜在的结果是收件箱送达率降低。当进行这种检查时，它简单地向服务器发送检测邮件，看它是转发还是不转发。

##### 确认发件者的IP地址不是拨入范围

 电子邮件的标头还提示了发送信息的邮件服务器IP地址，然后进行检查，确定它没有处于拨入IP范围内。由于其始发IP是隐藏的，所以拨入IP范围是匿名的，并且只有可见的IP地址是来自拨入范围。这些IP范围通常不会用于生成邮件服务器，因为它们被视为垃圾邮件的潜在来源。被标记为使用此IP地址的邮件服务器均可能出现收件箱送达率降低的情况。

##### 确认发件人的IP地址不是已知的动态IP范围

 来自邮件标头的邮件服务器IP经过检查，确认它不是用于发布动态 IP的服务器，而是使用了静态IP地址的服务器。被标记使用这种IP地址的邮件服务器可能会导致收件箱送达率降低。 电邮服务器配置模块 URL:[[4]](https://www.deliverywatch.net/compliance/displayServers.do)

#### 邮件授权模块

 邮件授权模块检查并确认源自标头的邮件服务器IP地址能够代表列在返回路径标头内的域名，而且是经过授权后才发送的。这种检查是通过使用Sender Policy Framework （SPF）完成的，这种框架帮助识别某发件人地址是否虚假，这里有四种可能的检查结果。

<table class="wikitable"><thead><tr><th>状态</th> <th>说明</th> </tr></thead><tbody><tr><td>Pass 合格</td> <td>发件者经过了授权，并代表含在电邮活动标头返回路径内的域名发送邮件。</td> </tr><tr><td>Neutral 中性</td> <td>关于发件人的授权状态没有交待，信息应该被服务器接收。</td> </tr><tr><td>Soft-Fail 软故障</td> <td>发件者被授权并代表包含在电邮活动标头返回路径内的域名执行邮件的发送，但是接收者应该放宽处理这种故障。该结果是用于测试目的。</td> </tr><tr><td>Fail 故障</td> <td>发件者没有受到含在电邮活动标头返回路径内的域名授权和代表来执行邮件的发送。</td></tr></tbody></table> 如果SPF检查结果显示合格，邮件授权模块将只返回“良好”。SPF检查中其他结果将为“错误”。你可以跟踪寻找讨论电邮活动SPF检查的详细描述。 Mail Auth Module URL：[[5]](https://www.deliverywatch.net/serverChecks/displayMailAuth.do)

### 分析模块

 分析模块是由19份报表组成，根据邮件大小、内容类型和发送频率等，设计用来提供有关电邮活动提交率详细的统计信息。

<div class="center"><div class="floatnone">[![样本分析模块报告](/assets/images/2014/07/DeliveryWatch_Concepts_and_FAQ_-_Page_07_Image_0002.png)](/assets/images/2014/07/DeliveryWatch_Concepts_and_FAQ_-_Page_07_Image_0002.png)</div></div> 分析模块仅在两列内显示活动信息：即客户电邮活动平均值和全球平均值的比较。报表的参数可以进行调整，显示时间范围覆盖的结果以及行业领域等等。 分析模块 URL:[[6]](https://www.deliverywatch.net/analytics/selectReport.do)

Delivery Watch 的操作
------------------

 Delivery Watch设计用来帮助正在寻求提高其送达率的emarsys客户，同时为每个客户提供了一个专用账户。向大型客户提供了其自己的Delivery Watch账户，而其他较小的用户则把内容发送到他们的账户经理Delivery Watch的账户中。不论账户的类型如何，一般都是由账户经理打理。

<table class="wikitable"><thead><tr><th>客户类型</th> <th>Delivery Watch账户</th> </tr></thead><tbody><tr><td>A 级Key 关键级Gold 黄金级</td> <td>- 为客户设立专用账户
- 必要时可拥有多个账户
 
</td> </tr><tr><td>B 级C</td> <td>- 使用账户经理的个人账户
 
</td></tr></tbody></table>### 建立一个Delivery Watch账户

 为了提供Delivery Watch应用上的支持，必须首先根据下列步骤创建账户：

1. 账户主管或者客户服务主任批准Delivery Watch账户建立申请。
2. 账户建立请求发送到Delivery Watch支持人员，同时附带下列信息： - 客户姓名
- 客户类型
- 账户经理/主管的名称

 账户经理或账户主管负责监测客户在Delivery Watch中的递交结果。如果某客户终止了与Emarsys的合同，账户经理必须把信息报告给Delivery Watch支持人员，以便关闭账户。 如果已经为客户开通了Delivery Watch账户（例如A级、黄金和关键级账户），则账户经理必须保持管理员权限，并只向客户提供用户级权限。相关做法的更多细节信息参见另外的文档，此文档可从第二级支持人员获得，也可以从Delivery Watch支持人员获取。

### 提供Delivery Watch支持

 在Delivery Watch支持方面，账户经理是Emarsys客户的第一个联系人；其他所有客户可直接联络Delivery Watch支持人员。 在联系支持人员之前，如果你有任何疑问或者问题，请先阅读可用的文档。如果你无法自己解决问题，请与Delivery Watch支持人员联系，以获得尽可能多的信息，包括账户名称和办公地址。 Delivery Watch向Emarsys的所有Delivery Watch客户提供了专门的电子邮件支持服务，邮箱为[[7]](mailto:support@deliverywatch.com).

### 使用网页服务API(WS-API)

 某些Delivery Watch模块可以使用网页服务API（WS-API）进行访问，这种服务可以让第三方应用程序承担检测任务，并在其GUI内显示结果。目前，只有电邮活动模块和垃圾邮件过滤模块可通过WS-API访问。

故障解决及常见问题解答
-----------

 下列部分包括了一些频繁提出的问题和一般的问题，并且提供了它们的处理指南。

### 在Delivery Watch 中没有显示出电邮活动

 一封活动邮件提交给触发器邮箱后 (显示在种子列表的底部，`cdw*@deliverywatch.com`) ，Delivery Watch立即注册一个新电邮活动。确定此地址包含在有问题的活动的收件人名单中，如果没有，简单地添加即可。 如果问题还存在，请联络支持人员。

### 在状态条上没有电邮活动结果

 电邮活动已经被系统成功注册，但是大部分被标记为丢失。结果显示为丢失的最为常见的原因是：当系统查询时，内容没有出现在邮箱中。 如果所有人（或者特定的提供者）的电邮活动全部丢失，那么原因可能是种子列表中丢失了地址，而且还没有发送出去。

1. 检查发送日志，确保收件人使用SMTP收到了邮件。
2. 在下一次电邮活动中，相应地更新你的种子列表。

 这是此系统最为常见的用户问题。 或者，即便邮件已经成功地递交，可能系统无法查询结果，例如POP3提供商阻止查看收件箱以外的文件夹，因此如果信息已经进入了垃圾邮件文件夹，那么不可能看到它。 大量丢失结果的另一个原因是，ISP发现Delivery Watch被阻止从邮箱中提取结果的技术问题，比如故障停机。 更多详细说明请联络递交部或者Delivery Watch支持人员。

### 预期的未决SpamFilter结果是什么

 垃圾邮件检查通常需要五到十分钟时间。如果在十分钟之后（最长时间）仍没有结果，则意味着系统可能出现了问题。这种情况最常见的原因是垃圾邮件过滤器已经损坏，应尽快向Delivery Watch支持人员报告。

### 如何处理验证警告

 如果你收到了验证警告，请联络递交部 ([[8]](mailto:deliv@emarsys.com))，他们负责客户验证步骤的正确完成。请联络可提供帮助的本地二级支持人员，必要时升级到求助递交组。

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**请注意：**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">您不能关闭这些验证检查，因为它们是用来帮助确认内容质量并提高送达率的。</td></tr></tbody></table>### 已发送了多个活动，但是只有一个在控制面板上可见

 电邮活动模块使用了特定的机制过滤出重复的电邮活动，有助于防止因错误导致每月限度用尽的情况。因错误或由于不适当的建立而发送的信息等重复内容是通过下面机制进行过滤的：当此内容与现有电邮活动相比时匹配率不低于91%时，此机制将其标记为“相同”，并对内容（标头和正文）进行检查。 被标记为“相同”并且在Delivery Watch上初始电邮活动注册后24小时内发送的任何内容被分类为重复内容，并且不会显示在控制面板中。对于Delivery Watch检测出的任何重复内容，将会触发一封通知邮件，并发送到管理员邮件地址。

<table border="0" cellpadding="1" class="wikitable" style="width: 100%; border-width: 0px; border-style: solid;"><thead><tr><th style="text-align: left; border-color: #fff; background-color: #fff; color: #eb5a19;">**请注意：**</th> </tr></thead><tbody><tr><td style="text-align: left; border-color: #fff; background-color: #fff; color: #555555;">由于技术原因，当前所有Delivery Watch.com邮箱仅供Delivery Watch支持组使用。</td></tr></tbody></table>### 故障报告程序

 对于任何故障报告或者改进建议，请联络Delivery Watch支持人员并提供尽可能多的信息，邮件请发到支持组邮箱：[[9]](mailto:support@deliverywatch.com)。
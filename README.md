# element4chinese
在大陆使用matrix进行端到端加密通信的friendly方案


![图片失效, 请联系作者](https://github.com/truthOnChina/images/raw/master/Screenshot_20210716-184534_Trebuchet.png "Philadelphia's Magic Gardens")


## 为什么是matrix协议?
>> 因为它可以让你和你的朋友**们**之间[端到端加密](https://zh.wikipedia.org/wiki/%E7%AB%AF%E5%88%B0%E7%AB%AF%E5%8A%A0%E5%AF%86)通信
>> #### 为什么要**端到端加密**?
>> - **端到端加密**大概是墙内长大的孩子们无法想象的技术——你和朋友之间的聊天记录只属于你们彼此, 甚至用来通信的服务器都无法知道你们相互之间说了什么
>> - **端到端加密**有什么好处呢? 可以把它理解为加密通信(*可以算军用级的了*), 通过matrix协议聊天不会被[审查](https://citizenlab.ca/2020/05/%e5%be%ae%e4%bf%a1%e7%9b%91%e6%8e%a7%e8%af%a0%e9%87%8a/ "多伦多大学的研究"), 这意味着你不可能被"微信官方"封号, 因为服务器都不知道你说过什么; 也不会出现“[一方发了敏感词, 另一边直接不显示](https://citizenlab.ca/2020/05/%e5%be%ae%e4%bf%a1%e7%9b%91%e6%8e%a7%e8%af%a0%e9%87%8a/ "多伦多大学的研究")”(*这在一些重要事件的讨论中可能是**致命**的, 因为你以为你说了对方也听到了, 但实际上对方的客户端根本没收到*), 因为(审查机制)连消息明文都获取不了, 也就无从过滤你的消息;

>> #### 为什么要对抗审查? 我是良民怕什么?
>> - 保护个人的隐私。注意，隐私不是秘密，隐私是我不想让全世界都知道的事情，而秘密是我不希望任何人知道的事情。**一个开放社会, 如果没有对弱势群体的隐私的保护, 就会造成强势群体对弱势群体的剥夺**, 正所谓“无隐私，不自由”。
>> - 如果当时李文亮医生与他的朋友们是在[使用matrix协议的端到端加密聊天软件](https://matrix.org/clients/ "最常用的客户端叫element")上讨论的话, 那么至少**暴力机关无法取证**, 也就无法定罪, 甚至只要他咬死不认, 那暴力机关都无法确定到底是不是他说的 —— 当然, 如果群组内认识他的人出卖他的身份, 或者输入法(讯飞/百度/微软)出卖了他的输入记录, 或者自己使用的设备(*如华为vivo小米iphone等国行机*)/操作系统(*不开源*)不安全, 那么还是会被取证, 只能说个人在组织/公司面前几乎永远都是弱势群体

> 不同于teleg的端到端加密, matrix支持群组内端到端加密, 而且是默认开启的

> 不同于*微信*, 你可以在(**理论上无限**)个设备同时登录你的帐号, 并且通过密语(*可以理解为密码*)**解密并察看自己之前的所有聊天记录**, 这也意味着你发出去的文字/图片/文件都不会像*微信*那样**莫明其妙**地丢失


## 选择一个matrix客户端

[这里](https://matrix.org/clients/ "最常用的客户端叫element")列出了官方推荐的所有客户端(都是**开源**的), 而且因为matrix的**服务端也是开源的**, 你甚至可以自己搭建一个matrix服务器(最大限度地避免中间人攻击); 本文中我们介绍的是Android客户端[Element](https://element.io "这也是目前支持者最多的客户端, 同时还有web网页版/ windows版/ MacOS版/ Linux版")的用法


## 首先我们在[fdroid](https://f-droid.org/repository/browse/?fdid=im.vector.app)下载Element的安装包(.apk);

*顺带一提, fdroid是一个非常棒的安卓应用商店, 虽然它并不能用于微信/支付宝/Chrome等不开源应用的下载安装和更新检查, 但它上面收录了绝大多数开源的安卓软件, 你可以在上面找到很多有意思的开源应用*


## 安装后打开, 我们就可以看到文首的这个页面

![图片失效, 请联系作者](https://github.com/truthOnChina/images/raw/master/Screenshot_20210716-184534_Trebuchet.png "Philadelphia's Magic Gardens")


## 点击 *开始吧* 按钮继续

Element默认的homeserver是matrix.org, 但不知道为什么这个域名在大陆无法访问(*可能是有不想让中国人民拥有言论自由和隐私权的反华势力派黑客阻断了我们对这个homeserver的访问*), 所以我们选第三项 **其他**
![图片失效, 请联系作者](https://github.com/truthOnChina/images/raw/master/Screenshot_20210716-184617_Element.png "Philadelphia's Magic Gardens")


## 将homeserver设为 **https://mozilla.modular.im/**
![图片失效, 请联系作者](https://github.com/truthOnChina/images/raw/master/Screenshot_20210716-184627_Trebuchet.png "Philadelphia's Magic Gardens")


## 点击 *使用单点登录* 按钮继续

![图片失效, 请联系作者](https://github.com/truthOnChina/images/raw/master/Screenshot_20210716-184640_Trebuchet.png "Philadelphia's Magic Gardens")


## 选择一个靠谱的浏览器打开oAuth页面, 推荐firefox或者iceraven

![图片失效, 请联系作者](https://github.com/truthOnChina/images/raw/master/Screenshot_20210716-184649_Android_system.png "Philadelphia's Magic Gardens")



## 推荐使用github帐号或firefox帐号登录, 因为这两个网站虽然在中国大陆境内比较卡(DNS污染), 但连还是连得上的

![图片失效, 请联系作者](https://github.com/truthOnChina/images/raw/master/Screenshot_20210716-184717_Firefox.png "Philadelphia's Magic Gardens")












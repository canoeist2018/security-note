# 区块链安全基础
- [区块链安全基础](#%E5%8C%BA%E5%9D%97%E9%93%BE%E5%AE%89%E5%85%A8%E5%9F%BA%E7%A1%80)
  - [区块链技术简介](#%E5%8C%BA%E5%9D%97%E9%93%BE%E6%8A%80%E6%9C%AF%E7%AE%80%E4%BB%8B)
    - [区块链技术的由来](#%E5%8C%BA%E5%9D%97%E9%93%BE%E6%8A%80%E6%9C%AF%E7%9A%84%E7%94%B1%E6%9D%A5)
    - [区块链的安全性技术](#%E5%8C%BA%E5%9D%97%E9%93%BE%E7%9A%84%E5%AE%89%E5%85%A8%E6%80%A7%E6%8A%80%E6%9C%AF)
  - [影响恶劣的区块链安全事件](#%E5%BD%B1%E5%93%8D%E6%81%B6%E5%8A%A3%E7%9A%84%E5%8C%BA%E5%9D%97%E9%93%BE%E5%AE%89%E5%85%A8%E4%BA%8B%E4%BB%B6)
    - [交易所](#%E4%BA%A4%E6%98%93%E6%89%80)

## 区块链技术简介

### 区块链技术的由来

区块链这项技术来自于比特币，我们一般称它为一种分布式的数据库。2008年11月1日，一个代名为中本聪的人在互联网上发布了《比特币白皮书：一种点对点的电子现金系统（Bitcoin: A Peer-to-Peer Electronic Cash System）》的论文，文中描述了一种通过点对点技术实现的现金支付系统。

而在论文中，中本聪描述的将交易打包成区块，然后以链式的方式存储起来的方式，在英文的论文中叫做 chain of blocks，这个也被翻译成区块链。而现在我们大家讲的 blockchain 这个新的英文单词，是在 2016 年出现的，当然翻译采用了同样的术语：区块链。

由此，大家可以知道，首先是出现了比特币这个产物，在运行多年之后，该技术被认为是可行的，才出现了区块链这样的术语，它是广大技术爱好者从比特币这样的经过验证的系统中提炼出来的。

- 2008.11 中本聪发表《比特币白皮书：一种点对点的电子现金系统》论文
- 2009.01 比特币上线，中本陪挖出创世区块
- 2010.05 使用一万个比特币购买了价值25美元的披萨
- 2010.09 世界上最早的矿池出现
- 2011.04 官方有历史记载的 0.3.21 版本上线，uPNP，聪
- 2013.02 比特币历史上的重要版本，0.8 版本上线，支持大规模交易
- 2015.08 全美已经有 16 万商家接受比特币交易
- 2016.09 Microsoft 的Project Bletchley Whitepaper 首次提到了 blockchain
- 2017.12 历史最高价，19783 美元

### 区块链的安全性技术

从最初中本聪设计的比特币，将其定位是一种电子现金系统，也就是一种金融系统。大家都知道和金融相关的东西是最需要考虑安全性的，这个安全性对于大家来说就是所持有的金融产品是有保障的，不能说没有没有，并且没有我的审批，任何人都不能使用。对于技术上来说，至少需要满足保密性，完整性和可用性这三个安全基础特性。而设计这样的一个金融系统，它是基于一个不需要中心机构，大众都可以参于的去中心化系统来说，是几乎是一个不可能完成的任务。

但这个艰巨的挑战，最终被中本聪设计出来的系统给解决了。他给的这个去中心化的设计方案，使用了分布式数据存储、点对点传输、共识机制、加密算法等技术，同时运用了大量的安全方面相关的技术。其中重要的安全技术包括：

- 非对称加密算法：ECDSA 椭圆曲线数字签名算法
- 哈希算法：SHA-256 RIPEMD-160
- 区块完整性：merkel tree
- 共识机制：PoW

整个系统的设计但没有对机密性进行要求，因此所有的数据都是公开的，所有的人都可以查看。那你不是应该担心所有人都知道你拥有多少资产，你又进行了哪些交易。而比特币采用匿名性解决这个问题，这个匿名性是通过交易的处理使用的是随机生成的比特币地址来达成的，通过这个随机生成的地址可以达到隐藏交易对象的特性。但这个匿名性是相对于比特币系统来说的，因为使用比特币系统人最终可能会同真实世界的人产生交易行为，如买卖物品、购买比特币等，在获取了大量的信息之后，从而最终被推断出这个比特币地址是你的。所以它只是一个半匿名系统，这个隐私特性是你需要了解到的。

我觉得共识机制才是比特币发明中的首创的最大的一个技术，其它的都是通过利用现有的技术来实现的。而共识技术最早可以追溯到防止垃圾邮件发送的机制，该机制是在发送邮件之件，让发件人进行垃圾运算，从而降低邮件发送的频率。而比特币采用的大量已有的技术加上少量的创新技术来构建一个安全的金融系统，也算一个非常大的创举了。

大家经常会听说一些有关区块链行业的重大安全事件，而这些安全事件的损失又是如此的之惨烈。那我们这里要谈论的就是这个如此之多的安全技术组成的系统是不是安全的？黑客是怎么样成功的攻击到区块链系统的？我们可以采取什么样的措施加强区块链的安全性。

## 影响恶劣的区块链安全事件

在区块链行业里，无论是币圈还是链圈，对安全事件非常敏感。不管是从什么哪里暴料出来的安全事件，都会引入大家的广泛观注。当然，首当其冲的就是影响范围广、金额庞大的交易所安全事件了。

### 交易所

1、Mt.Gox

2014年2月24日倒闭的 Mt.Gox 交易所，是当时最惨烈的破坏性事件，导致大量比特币玩家失去了对比特币的信心。成立于 2010 年的 Mt.Gox 抢占了加密货币发展的红利，曾经一度占到了全球比特币交易量的 70%，成为世界上最大的交易平台。从 2011 年开始，Mt.Gox 丢失或被盗了大约 850,000 个属于客户和该公司的比特币，价值在当时就超过了 4.5 亿美元。

2、Bitfinex

2016年8月2日，全球最大的交易所之一 Bitfinex 遭到黑客攻击，被盗取接近 12 万个比特币，损失金额超过 7200 万美元。当时，Bitfinex 采用了非常复杂的身份认证机制，同时也和安全合作伙伴 BitGo 一起进行了双因素身份验证。直到 2019 年，美国联邦执法机构归还了被盗的 27.7 个比特币。

3、币安

2019年5月8日，币安 BTC 热钱包里保存的 7074 枚比特币被盗，价值约 4000 万美元。在当天的零晨1点17分，通过 API 接口同一时间发起大量提币操作。据传，黑客使用了多种攻击手段，包括网络钓鱼、病毒等，并获取了大量用户的 API 密钥，谷歌双因素认证码以及其它信息。
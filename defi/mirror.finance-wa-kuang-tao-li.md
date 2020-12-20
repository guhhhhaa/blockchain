# mirror.finance挖矿套利

## 手把手教你年化200%以上的mirror.finance挖矿套利

1. **项目简介**

美国股票是全球非常有吸引力的资产类别，涌现出苹果、特斯拉等明星股票，但对于全球大部分人来说，进入价值36.3万亿美元市场的机会有限。特别是国人，参与美股的门槛很高，需要海外银行卡，交易所出金入金等，币圈如何参与美股呢？

12月4日，Mirror Protocol正式问世。它旨在“为全球散户投资者，提供一种更轻松地参与美国股票市场的方式。” mirror.finance主要做镜像资产，通过其稳定币抵押，生成各种锚定美股价格的美股代币。

这里铸造以及交易的美股代币,并不代表在现实中真实拥有该股票的所有权，仅仅只是锚定该资产的价格，所以叫mirror。美股代币的价格跟美股价格锚定，相当于变相拥有了美股股票。目前，mir上主要是一些谷歌、苹果之类的科技股。

在Mirror Protocol协议上，用户可以通过抵押其手中的TerraUSD来铸造美股代币。每铸造一枚美股代币，需要抵押美股价格的150%~200%的稳定币。比如某个美股价格100美元，则需要抵押150-200美元，来生成一枚其美股代币。如果该股票价格持续上涨，涨到150美元，用户的抵押资产将被清算，因此账号上应保有足够的ust资产。

1. **套利原理**

参与提供交易流动性，获取交易手续费和mir代币奖励。在交易所交易，交易所会提供一定的买单和卖单，保证市场的流动性。在去中心化平台，需要有用户来提供流动性，那提供流动性的人就能获得奖励。

截止12月16日，目前的年化率都在200%以上，值得去尝试。

![](https://docimg3.docs.qq.com/image/X9kcqLkt8ZwVnaHlSdvSOQ?w=2274&h=1580)

1. **操作步骤**

### 第1步： 安装和注册Terra station钱包

Terra station是一款谷歌插件，打开https://terra.mirror.finance/ ，点击左上角的connect。

![](https://docimg9.docs.qq.com/image/tv35ZJdFSN2VCROIGim03Q?w=2558&h=708)

点击下载安装，安装后，出现在谷歌浏览器上。

![](https://docimg7.docs.qq.com/image/l9JzArlti2-oFbPyNfW7lQ?w=2558&h=1242)

安装后，设置用户名密码，记录助记词，完成钱包的注册。

### 第2步：获取ust

获取ust有两种方式，一种是直接在库币交易所购买ust，还有一种是通过uniswap，用usdt换ust。个人推荐直接在交易所购买的方式，因为uniswap上操作，各种手续费比较多。

#### 方式1：通过库币购买ust

在[币安交易所](https://www.binancezh.pro/cn/register?ref=RU5CILPV)购买usdt，将usdt转入库币交易所 [www.kucoin.com](http://www.kucoin.com) 。库币支持usdt、btc、luna、eth的ust交易对，也可以将这些币转入库币兑换ust。

![](https://docimg8.docs.qq.com/image/Qh5fMwHYliVRedVYaQJltA?w=2558&h=1102)

#### 方式2：通过uniswap购买ust

使用这种方式，需要先安装狐狸钱包，下载地址：https://metamask.io/download.html。在[币安交易所](https://www.binancezh.pro/cn/register?ref=RU5CILPV)购买usdt，将usdt通过erc20的方式转入狐狸钱包。同时，狐狸钱包上的交易需要eth做手续费，需要同时转入一定数量的eth。

打开[https://app.uniswap.org/\#/swap](https://app.uniswap.org/#/swap)  ，链接狐狸钱包。

![](https://docimg1.docs.qq.com/image/IZGMUszxnlU9GEQmmC0WKg?w=2558&h=1188)

uniswap中，第一个通证选择usdt，第二个点击选择通证后，输入ust 的合约地址：0xa47c8bf37f92aBed4A126BDA807A7b7498661acD

![](https://docimg1.docs.qq.com/image/OkW81k9WC-l7S9wEVdnKkg?w=2548&h=1184)

![](https://docimg1.docs.qq.com/image/0ntDfRGNtgsN33ruEskxbg?w=878&h=1028)

输入需要兑换的usdt数量，点击兑换，这样狐狸钱包里的usdt就换成了ust。

![](https://docimg6.docs.qq.com/image/cyKXzi_04L8TiA8WSFM1ow?w=926&h=768)

狐狸钱包和terra钱包属于不同的网络，不能直接进行ust的转账。

点击[https://terra.mirror.finance/my](https://terra.mirror.finance/my) ，ust资产后面的actions点开send，填写terra station的地址，就能将ust转过来了。

![](https://docimg5.docs.qq.com/image/5lD1Jbf5i_gsoxiKVqpkng?w=546&h=542)

### 第3步：在terra链上，抵押ust生成美股代币

通过第2步，我们已经在terra上拥有了ust。接下来需要抵押ust生成美股代币。

打开，链接terra station钱包，填写需要抵押的ust数量。collateral ratio是抵押物价值与铸造价值之比的比例，选择200%，是指生成抵押品50%的美股代币，比如抵押100ust，生成价值50ust的美股代币。如果美股代币价格上涨到抵押品的价值，抵押品会被清算，因此，我们最好选200%的模式，提高容许的美股价格波动空间。

建议最好选择65%的ust去抵押，比如你有100u，就拿65u去抵押，抵押比例200%，生成32.5u的美股代币。后面提供流动性需要1:1美股代币和ust，账号上剩余的35u就可以参与提供流动性。

![](https://docimg7.docs.qq.com/image/ag4al2WgBGM0G74RJ6L-9A?w=2556&h=1568)

### 第4步：提供流动性，生成流动凭证

将美股代币+ust放进流动池子，生成流动凭证。提供流动性需要1:1美股代币和ust，选择好美股代币，输入数量，然后点击provide。

![](https://docimg5.docs.qq.com/image/L5w_Ntbc99zoJ0U1VbccVA?w=2558&h=1240)

输入terra station钱包密码，确认后就完成了。

![](https://docimg5.docs.qq.com/image/GpxWxyVBVVYp5UwhQe3KKQ?w=2558&h=1246)

![](https://docimg5.docs.qq.com/image/3ab6KwPe2X7U2oDtYaYFtw?w=1270&h=976)

### 第5步：stake流动凭证，开始挖矿

点击 [https://terra.mirror.finance/stake](https://terra.mirror.finance/stake) ，选择美股代币进行抵押，获取系统奖励。

![](https://docimg10.docs.qq.com/image/Pa7vUBSrh0Znj9nZcdeIGQ?w=2558&h=1484)

具体的收益数据可以在[https://terra.mirror.finance/my](https://terra.mirror.finance/my) 查看。


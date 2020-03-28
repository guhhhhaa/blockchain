# 【ICO】在不到一分钟的时间内创建ERC20令牌

{% embed url="https://medium.com/@vittominacori/create-an-erc20-token-in-less-than-a-minute-2a8751c4d6f4" %}

{% embed url="https://vittominacori.github.io/erc20-generator/" %}

## 在不到一分钟的时间内创建ERC20令牌

### 免费为标准，上限，最小，可刻录，可支付，ERC20令牌轻松部署智能合约。

[![&#x7EF4;&#x7EB3;&#x6258;](https://miro.medium.com/fit/c/96/96/1*Wy5OZ2xy6-z8hpbV6giF0w.jpeg)](https://medium.com/@vittominacori?source=post_page-----2a8751c4d6f4----------------------)[维纳托](https://medium.com/@vittominacori?source=post_page-----2a8751c4d6f4----------------------)跟随[2018年12月10日](https://medium.com/@vittominacori/create-an-erc20-token-in-less-than-a-minute-2a8751c4d6f4?source=post_page-----2a8751c4d6f4----------------------) · 5 分钟阅读

## 尝试生成器：[https](https://vittominacori.github.io/erc20-generator/) : [//vittominacori.github.io/erc20-generator](https://vittominacori.github.io/erc20-generator/) ![](https://miro.medium.com/max/1380/1*sPqrwRPa58HIbBjEu1ibcw.png)

## ICO <a id="2117"></a>

初始代币发行（ICO）已成为极为流行的筹集资金方式，同时又避免了法定融资的监管限制。2017年，ICO筹集了约65亿美元。他们今年已经筹集了超过20亿美元的资金。大多数ICO基于以太坊作为平台，更具体地说是基于以太坊的智能合约。ICO项目中的股票通常以ETH或BTC的价格出售，并以令牌（也称为ERC20令牌）的形式授予。  
因此，尽管我们习惯于查看和处理ERC20令牌，但很少有人确切地知道它们是什么，它们如何工作甚至是ERC20的含义。  
如果您想知道，ERC代表_以太坊请求评论_，而20是分配给该提案的数字。

## ERC20标准 <a id="0a56"></a>

> ERC20提供了传输令牌的基本功能，并允许令牌被批准，以便其他链上第三方可以使用它们。

这是标准的ERC20定义：

此外，还有一些可选的有用字段：

* 代币名称
* 符号
* 小数（通常为18）

但是，该系统并不完美。例如，如果您想在完成智能合约付款后采取行动，则应该打两次电话：在进行第二笔交易时，您应该首先`approve`允许`transferFrom`某些合约使用智能合约。使用这种方法，您需要向GAS支付两次费用。

注意：在我[之前的文章中，](https://medium.com/coinmonks/ethereum-payable-token-and-how-it-works-3bf3349a6a77)我已经解释了ERC20对转账的限制，以及如何将其扩展为现实的Payable令牌。为此，我构建了[ERC1363应付代币库](https://github.com/vittominacori/erc1363-payable-token)。

## 一般如何部署ERC20令牌？ <a id="0253"></a>

{% embed url="https://vittominacori.github.io/erc20-generator/" %}

{% embed url="https://medium.com/@vittominacori/create-an-erc20-token-in-less-than-a-minute-2a8751c4d6f4" %}

有许多库和工具可提供诸如ERC20和ERC721之类的标准实现，您可以按原样部署或扩展以满足您的需求，还有Solidity组件来构建自定义合同和更复杂的分散式系统。  
但是您需要学习Solidity，需要设置自己的环境和代码，并使用以太坊节点部署令牌。  
他们有很多技能和配置。

但是我希望看到人们思考如何将他们的项目分散化（如果区块链可以应用于他们的项目），而不是为节点不同步，智能合约是否安全以及其他许多与区块链相关的问题而烦恼

因此，我决定构建一个简单的**DApp，**使人们可以在不到一分钟的时间内部署其令牌！

> **是的，不到一分钟！**

自己尝试👇https [:](https://vittominacori.github.io/erc20-generator/) //vittominacori.github.io/erc20-generator  


您要做的就是填写一个简单的表格并使用[MetaMask](https://metamask.io/)完成交易。  
没有其他的。  
没有登录。  
没有设置。  
无需编码。  
不付款（不包括GAS）。

## 关于代码 <a id="c8cf"></a>

令牌将使用[OpenZeppelin](https://github.com/OpenZeppelin/openzeppelin-solidity)构建，[OpenZeppelin](https://github.com/OpenZeppelin/openzeppelin-solidity)是一个用于安全进行智能合约开发的开源库。智能合约已通过solc **v0.5.15 + commit.6a57276f**进行了编译，并使用[Truffle](https://github.com/trufflesuite/truffle)，以太**坊**的开发环境，测试框架和资产管道，旨在简化以太坊开发人员的生活。

## 您将部署什么？ <a id="33f8"></a>

**详细的ERC20令牌**：您的令牌将完全符合ERC20定义，并与世界各地的任何ERC20钱包兼容。  
它会有一个名称，一个符号和一个小数位数。

**Mintable Token**：您可以通过铸造令牌来生成令牌。  
只有具有_Minter_角色的人员（或智能合约）才能执行此操作，您还可以在地址中添加或删除Minter角色。

**上限令牌**：您不能超出定义的令牌上限。这样可以确保人们生成的令牌不会多于声明的令牌。

**可燃令牌**：您的令牌可以被燃烧。这意味着您可以选择通过销毁一些代币来减少循环供应。

**ERC1363应付令牌**：ERC1363是与ERC20兼容的令牌，可以对接收方合同进行回调，以通知令牌转移或令牌批准。它可用于创建代币应付众筹，出售代币服务，支付发票，进行订阅，将其用于特定用途以及许多其他目的。[发现更多](https://github.com/vittominacori/erc1363-payable-token)。

**令牌恢复**：它允许合同所有者恢复发送到合同中的任何ERC20令牌，以防出错。[发现更多](https://github.com/vittominacori/eth-token-recover)。

除非调用_enableTransfer_函数，_否则_令牌将不可转让。只有具有_操作员_角色的人（或智能合约）才能转让令牌。您也可以在地址中添加或删除操作员角色。

## 怎么运行的 <a id="8daf"></a>

通过访问DApp网站[https://vittominacori.github.io/erc20-generator，](https://vittominacori.github.io/erc20-generator)您将能够在不到一分钟的时间内部署令牌。

在要求的信息下方。![](https://miro.medium.com/max/60/1*PMcXv-XXfaPWVczczEhD3w.png?q=20)![](https://miro.medium.com/max/3992/1*PMcXv-XXfaPWVczczEhD3w.png)

输入您的首选令牌**名称**和**符号**。还要插入**小数点**（通常说是18）。

然后输入令牌**上限**（可用令牌的最大数量；最多可以生成此令牌数量）和令牌**初始余额**（要在您的钱包中生成令牌的初始数量）。

选择在部署期间**启用传输**，或稍后手动启用它。

您可以选择要将令牌部署到的**网络**。

在MetaMask弹出窗口中确认您的交易，然后等待令牌被部署。![](https://miro.medium.com/max/60/1*CLPpKLmC290UF16X9Vtclw.png?q=20)![](https://miro.medium.com/max/4008/1*CLPpKLmC290UF16X9Vtclw.png)

您将收到交易哈希和令牌地址，并且您的智能合约将自动部署在所选网络上。

您的令牌将出现像[这样](https://etherscan.io/token/0x883f896aae1b067f94e6e04e8cb168f871ba765b)和你的源代码将已核实Etherscan因为我部署的这一个每个复仇网络上。

在GitHub上浏览[Smart Contracts](https://github.com/vittominacori/erc20-generator)或[DApp](https://github.com/vittominacori/erc20-generator/tree/dapp)的源代码，以了解如何手动编写自己的令牌，或者简单地尝试[在此处](https://vittominacori.github.io/erc20-generator/)构建令牌。

对此有任何想法，请在此处评论，打开[问题](https://github.com/vittominacori/erc20-generator/issues)或通过[Twitter](https://twitter.com/vittominacori)或[LinkedIn](https://www.linkedin.com/in/vittoriominacori/)与我联系。

**345**

* [以太坊](https://medium.com/tag/ethereum)
* [智能合约](https://medium.com/tag/smart-contracts)
* [Erc20](https://medium.com/tag/erc20)
* [代币](https://medium.com/tag/token)
* [坚固性](https://medium.com/tag/solidity)

**345拍手**

[![&#x7EF4;&#x7EB3;&#x6258;](https://miro.medium.com/fit/c/160/160/1*Wy5OZ2xy6-z8hpbV6giF0w.jpeg)](https://medium.com/@vittominacori?source=follow_footer--------------------------follow_footer-)

撰写者

### [维纳托](https://medium.com/@vittominacori?source=follow_footer--------------------------follow_footer-)

跟随

**网络和区块链开发人员**


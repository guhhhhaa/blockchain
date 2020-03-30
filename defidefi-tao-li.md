# 【DeFi】DeFi套利

## 探索DeFi交易策略：DeFi套利

{% embed url="https://www.theblockcrypto.com/post/45750/exploring-defi-trading-strategies-arbitrage-in-defi" %}

通过[贡献者网络](https://www.theblockcrypto.com/author/the-block-contributor-network)

**2019年11月4日，美国东部时间下午5:25·阅读24分钟**

![](https://www.tbstat.com/wp/uploads/2019/05/grayscale-ethereum-1200x675.jpg)

**快速采取**

1. DeFi市场分散且效率低下，这是套利者发展策略的沃土。在本节中我们关注的DeFi中的两类套利策略是收益套利（利率和抵押）和跨DEX套利
2. DeFi基础架构具有新功能，例如基于原子批处理的交易处理，有可能启用新的交易策略，而在传统金融市场中却没有类似的交易
3. 对于套利者而言，收益率和跨DEX套利似乎都是短暂的机会，前者是因为Topo Finance等聚合器，而后者是因为它们对流动性和更广泛的以太坊产生负面影响而被DEX建设者彻底阻止

[Alex Obadia](https://twitter.com/ObadiaAlex)  领导[Cambrial Capital的](https://cambrial.com/)研究和平台工作，  [Cambrial Capital](https://cambrial.com/)是总部位于伦敦和柏林的加密[货币](https://cambrial.com/)基金。他还组织了伦敦DeFi峰会和伦敦零知识月度聚会。这纯粹是为了提供信息。这篇文章中的任何内容都不应被解释为投资建议。

#### 介绍

去中心化金融（DeFi）是大约一年前创建的一个术语，用于描述致力于构建新的透明，未经许可和可编程的金融基础结构的项目的动向。一年后，[该运动的规模，追随者和多样性不断增长，](https://medium.com/alethio/the-defi-series-monitoring-activities-user-community-growth-f274946d0ac9)被认为是下一波基于区块链的技术采用浪潮的有希望的短期催化剂。尽管DeFi增长了，但与集中化市场相比，其市场仍然效率低下且支离破碎。 

市场分散和效率低下对寻求alpha的交易员来说是音乐。这是Cambrial对这些机会的可投资性及其涉及的新颖考虑进行研究的产物。作为加密货币基金，我们对这些机会感兴趣，因为它们是持久，绝对，与传统市场无关，潜在的经风险调整收益的潜在来源。我们认为，这些收益与“传统”加密交易收益相比承受的风险不同，因此可以改善加密交易策略组合中的风险分散性。

这篇文章将研究DeFi中的套利机会，将其分为收益套利和交叉交易所套利。目的是提供1）对在此新基础架构上运行的某些策略的理解，包括它们所涉及的风险； 2）开始思考这些策略的持久性以及（重新）DeFi中的套利定义。假定您对DeFi有一定的了解，如果您不熟悉该主题，我们建议您阅读DeFi [简介](https://medium.com/macro-narratives-in-blockchain/the-next-fintech-global-open-finance-infrastructure-90ac093a411b)。

#### **套利**

套利（定义）： 

准同时购买或出售一项资产或类似资产，以从不同市场或不同形式的价格不平衡中获利。[（资源）](https://www.investopedia.com/terms/a/arbitrage.asp.)

DeFi市场的分散和效率低下意味着同一金融工具的价格在不同的DeFi场所（细分）之间会有所不同，并且会针对相同的市场变动（效率低下）做出不同的调整。换句话说，这些是套利交易的沃土。我们将DeFi套利策略分为两类：收益套利和交叉交易套利。

#### 1.收益套利

收益套利策略在不同的贷款产品之间（即利率套利）或在抵押资产之间执行。由于费率在整个空间中明显分散且相对没有竞争力，因此这些策略如今已可获利。容量（即可以投入多少钱）虽然很难估算，但仍取决于交易量和未偿还的可用代币。以下是由我们的假想交易员伯尼执行的三个套利交易示例，以及与之相关的风险：

例如1。跨资产单一平台利率套利

⇒在5月18日，我们的交易员伯尼正在使用[Compound V2](https://compound.finance/)，这是一个透明的，自主的货币市场，它使用户和应用程序可以轻松地赚取利息或借以太坊资产而无需依赖交易对手。 

⇒他注意到USDC的借贷实际年利率（7.8％pa）低于DAI的供给年利率（14.5％pa）。 

⇒假设伯尼已经拥有DAI。 

⇒伯尼以DAI抵押品借入了USDC稳定币。 

⇒然后，他将所说的USDC转换为DAI。

⇒最后，他借给新收购的DAI，年息差为6.7％。 

（数据源：[Loanscan](https://loanscan.io/)）

该机会的主要风险是其偶然性和可变利率债务产品可能带来不利的利率变化的可能性。其他风险包括必须包含在不平等中的可变交易成本（即天然气）（USDC借款APR &lt;DAI供应APR +交易成本），USDC / DAI和DAI / USD对的隐含市场风险（即挂钩偏差风险） ）和系统性风险（即复合智能合约的失败）。

![](https://www.tbstat.com/wp/uploads/2019/11/Screen-Shot-2019-11-07-at-17.21.27-800x384.png)

_**图表：**化合物V2的DAI贷款利率与USDC借款利率之间的价差_

**资料来源：** [币安研究](https://info.binance.com/en/research/marketresearch/img/issue19/Binance-Research-Defi-2-Arbitrage-and-Carry-Trade-Strategies.pdf)，[Loanscan](https://loanscan.io/)

可以想像这种策略的其他[缺点](https://defitutorials.substack.com/p/margin-trading-using-dydx-exchange)，例如跨资产跨平台利率套利（例如，在保证金交易平台[DyDx](https://defitutorials.substack.com/p/margin-trading-using-dydx-exchange)和Compound之间）和单资产跨平台利率套利。跨贷款平台执行交易会引发新的考虑，例如不同的利率变化机制。（即，化合物具有线性借入和超线性供给率曲线，而dYdX具有超线性借入和供给率曲线）。 

例如2。BlockFi / DyDx利率套利 ****

⇒ [DyDx](https://defitutorials.substack.com/p/margin-trading-using-dydx-exchange)是加密的资产，用户可以使用多达5倍的杠杆，借保证金交易和出借trustlessly一个开放的交易平台。[BlockFi](https://blockfi.com/)是一个托管借贷平台，允许用户借入和借出大型市值加密资产，例如比特币（BTC）或以太坊（ETH）。

⇒同样，假设伯尼已经拥有DAI或USDC。

⇒伯尼以DAI或USDC作为抵押品在DyDx上借入ETH（初始年利率为0.99％）。 

⇒然后，伯尼可以将那个ETH借给BlockFi，年利率3.3％

（来源：[币安研究](https://info.binance.com/en/research/marketresearch/img/issue19/Binance-Research-Defi-2-Arbitrage-and-Carry-Trade-Strategies.pdf)）

机会的风险包括上述可变利率变动风险（过去对于BlockFi而言变化非常快），DyDx的清算风险（也包括基础风险/社会损失风险，并取决于ETH的价格波动性） ，如果您没有立即找到借款人，BlockFi方面的智能合约风险和贷款匹配延迟就会出现。

例如3。下放收益套利 

⇒抵押可以使代币持有人在其代币上产生收益，以此作为对代币网络做出贡献的奖励。

⇒假设伯尼的代币X目前每年押注5％。 

⇒由于伯尼目前不需要使用代币X，因此他将其交换为另一资产，例如XTZ（Tezos），目前收益率更高，为7.1％。 

⇒当伯尼需要使用X令牌时，他将XTZ交换回X，从而获得了每年产生的2.1％的额外收益。

（数据来源：[Staked](https://staked.us/yields/)）

这个机会有五个主要风险： 

1）根据资产X的流动性概况和可用位置，资产交换可能会变得困难。对于长尾低流动性资产，取决于头寸规模，存在市场影响和滑点风险。

2）虽然可以放样资产，但有时可能会有一个锁定期，尽管放开二手市场（例如[Vest](https://vest.io/)），但简洁的交换仍然很困难， 

3）抵押收益以代币计价，这意味着您的抵押奖励取决于代币的网络通货膨胀率和美元贬值的可能性。

4）与之前的风险相似，伯尼在掉期至X之前将面临X / XTZ货币对的市场风险。伯尼可以对冲自己，以免受这种风险的影响。

5）有一些新的风险因素需要考虑，例如智能合约风险和大幅削减风险（即，不合理的押注将通过削减部分抵押金额来惩罚）。

![](https://www.tbstat.com/wp/uploads/2019/11/Screen-Shot-2019-11-07-at-17.21.40-658x450.png)

_按“份额”排序的可抵押资产表。“份额”表示考虑到网络的通货膨胀后剩余的以令牌为单位的收益。（来源：_[_https_](https://beta.stakingrewards.com/) _:_ [_//beta.stakingrewards.com/_](https://beta.stakingrewards.com/)_）_

尽管以上示例似乎易于复制，但我们认为收益套利的一个优势将来自对相关协议/平台的有效分配和严格的风险管理实践。对于利率套利，随着用户向贷款协议分配资金，贷款利率会动态变化。这意味着一次性分配的大量资金（今天约4万美元）将遭受大量的滑点成本。为了成功，需要正确执行订单，同时牢记您正在与之交互的每个借贷平台的汇率变动机制并有效地为美元分配美元，我们相信这是合法的优势。 

但是，随着[Topo Finance](https://medium.com/topo-finance/introducing-topo-finance-a-defi-services-platform-8b76c0aef0f6)等聚合服务的兴起，这种优势似乎并不十分持久。这些服务通过汇总和优化许多可用利率为用户提供DeFi中最好的借贷利率和借贷利率。尽管他们目前不提供跨资产贷款优化，但Topo Finance团队已表明这是他们的路线图。问题就变成了该边缘消失需要多长时间。 

上面的论点指出了一个较短的时间表，但值得记住的是，许多机构参与者会更愿意投资于运行这种策略的基金，而不是将钱投入零售产品。因此，答案可能不像我们上面提到的那样二进制，而是两者可能并存，至少在中期而言，以适应不同的资本池。 

从长远来看，像Topo Finance这样的服务正在通过有效地重新分配给用户价值（通常会产生套利者通常会抓住的收益）来缩小套利机会，同时收紧贷款利率和贷款协议之间的差距。这是DeFi可能成为零售区块链采用的催化剂的主要原因，因为它提供了优于传统金融基础设施的明显优势：公共的，机器可读的数据与开放的端点相结合，从而降低了进入门槛，最终实现了**更好的价值重新分配用户**。 

#### 2.跨交易所套利

从具有分散收益分布动态的收益套利交易机会继续，我们现在集中在分散式金融中的有限，稀缺和赢家通吃套利机会。此部分特别感兴趣的是去中心[化交易所](https://docs.ethhub.io/built-on-ethereum/decentralized-exchanges/what-are-decentralized-exchanges/)之间的交叉交易所套利，以及由此产生的天然气竞标大战交易机器人参与。在交叉DEX套利中，交易者通常会连续扫描去中心化交易所订单簿，以在不同交易之间顺序执行一系列交易目标是获得比最初更多的钱的场馆。以下是两个去中心化交易所[OasisDEX](https://eth2dai.com/market/WETH/DAI)（现在称为Eth2DAI）和[Uniswap](https://docs.ethhub.io/built-on-ethereum/decentralized-exchanges/pool-based/uniswap/)之间的三角套利交易的[示例](https://docs.ethhub.io/built-on-ethereum/decentralized-exchanges/pool-based/uniswap/)，以及DAI / MKR，MKR / WETH和WETH / DAI对，可带来1.6％的利润。 

![](https://lh6.googleusercontent.com/SN3pzrUyrig307Ev-9o4VATpO85OcU-xm0v6vb_tas577icS2f6U2v2YsDfZsy_KapYiBj1-VgkBq1PFOdtVji9FaW2da49ANwmJmcWuNQfZFdVEWIRMv6_C3j1IHNbSK_hzhW_g)

[_http://ethtx.info，_](http://ethtx.info/)_分析：0xa595a252a5324d520d17de440e71ba23c622dbdaf8a5f6a3d88c866b0fbdf88c。感谢OasisDEX开发此工具，并感谢Bartek 在伦敦DeFi Summit上的_[_精彩演讲_](https://youtu.be/mwkL7beq0m8)_中分享了该工具。_

这就是它变得有趣的地方！尽管以上内容看起来像其他任何三角套利交易，但传统的交叉交换套利都没有在该基础设施上进行根本上的两个新交易：基于原子批处理的交易和优先权天然气拍卖。

#### 2.1基于原子批处理的交易

由于[以太坊](https://ethereum.github.io/yellowpaper/paper.pdf)是一个图灵完备的智能合约系统（即允许对任意智能合约功能进行编码），并且智能合约以原子方式执行以图灵完整脚本语言编写的程序，因此人们可以在发送到智能合约的单个交易中对它们进行“编码”矿工将自动执行的任意数量的订单。 

这些订单可能具有任意复杂性，并且在执行交易时可能具有复杂的条件偏好。条件偏好的一个示例是，如果一个订单失败（即，一切都被取消，类似于传统的复杂订单类型，如“填充或杀死”），则原子批处理执行将抛出异常。有好几个人开始使用以太坊的这一功能，包括有一段时间的[Marble](https://medium.com/marbleorg/introducing-marble-a-smart-contract-bank-c9c438a12890)，该服务提供了快速借贷以进行外汇套利。“ 交易者可以从大理石\[智能合约\]银行借款，在DEX上购买代币，以更高的价格在另一个DEX上出售代币，偿还银行，并通过一次原子交易获得套利。”

![](https://lh4.googleusercontent.com/-cxBujD6YXyUb645ID33ZCnRL3_H82ftbARO4toZ3ehmaModl4u8ZSU-UnoZmgwW5v-qc-CJpIXIC8OjOrUKdTMiGttpfZn8AxdTY6LUCRcdLq3E72TM5T8s6oYZZn9meQ-lnB1q)

[_https://github.com/marbleprotocol/flash-lending_](https://github.com/marbleprotocol/flash-lending) _Marble的Flash Lender基本架构可用于在去中心化交易所执行套利交易。_

这很有趣，因为传统上，多腿套利的成功是概率性的，因为个别腿有失败的可能性（“腿部风险”）。虽然DeFi中多支路套利的成功率也是通过概率来衡量的，但这种不确定性现在源自被包括在以太坊区块中的可能性（并且不会被孤立），而不是由于单个支腿的成功而被执行原子地完全取消应该不起作用。 

您现在可以在单个以太坊交易中构建任意复杂的订单，而这在传统市场中是没有类似的。这暗示了在这个新世界中可以采取的策略类型。在旧世界中，一些复杂的多支路套利策略从来没有像现在这样，因为它们依赖于许多组件，每个组件都有失败的风险。由于这些因素，获胜率可能会急剧下降。在这个新的基础架构上将有多少种废弃的策略起作用，新的复杂的系统套利策略将是什么样？

值得注意的是，随着以太坊升级到[以太坊2.0，](https://docs.ethhub.io/ethereum-roadmap/ethereum-2.0/eth-2.0-phases/)此属性可能不再存在。简而言之，以太坊2.0网络将分为不同的部分（碎片）。在这个分片的世界中，您可能在两个分片之间执行套利策略的两个DEX位于两个不同的分片上，这也意味着两个不同的网络状态。尽管分片内的事务可以像以前一样发生，但分片之间的事务仍然可以发生，但是可以使用收据以异步方式进行。这让担心的企业家在DevCon 5期间依赖于此功能来提供其服务/产品，并促使Vitalik [发表了有关](https://ethresear.ch/t/cross-shard-defi-composability/6268)此功能[的帖子](https://ethresear.ch/t/cross-shard-defi-composability/6268)。 

回到以太坊的当前版本，交易者现在似乎可以执行任意复杂的无风险多支路套利交易，而不必担心传统的交易[对手交易对手信用风险](https://www.investopedia.com/terms/c/counterpartyrisk.asp)（因为他们在非托管场所操作）和绑腿风险（因为他们执行所有交易）他们的贸易分支“立刻”）。但是，需要考虑一些新颖的细微差别和风险： 

* 智能合约风险：您正在与之交互的智能合约中的错误使您的资金处于[过去发生的](https://consensys.github.io/smart-contract-best-practices/known_attacks/)风险。尽管很难评估这种风险，但是有一些方法可以将其最小化，例如购买智能合约保险，将自己限制为与经过审计并定期维护的智能合约进行交互。 
* 天然气支出：天然气支出过多会使交易无利可图的风险。您的交易具有的计算步骤越多，执行交易所需的费用就越多。如果优化不当，这会使整个交易无利可图，下一节将对此进行详细介绍。
* 清算风险：以太坊价格突然波动或使用的其他波动性抵押品消灭杠杆头寸的风险。在DeFi中使用杠杆的套利者与贷方/借款人以及超额抵押的贷款进行交互。尽管过帐额外的抵押品以避免清算通常可以独立于流动性来进行，但存在一个重要的风险，即在以太坊网络超负荷的情况下，您无法过帐额外的保证金并被清算。[最近发生在DeFi Saver。](https://medium.com/defi-saver/automatic-cdp-protection-faux-pas-analysis-updates-in-place-and-next-steps-e238e0d3114)
* 结构上的风险：如今，没有DeFi产品完全分散，[而是分散管理。](https://www.tokendaily.co/blog/becoming-decentralized-enough)这会影响您的资金安全，并使您面临包括甲骨文操纵风险（例如[，最近的Synthetix甲骨文攻击](https://www.theblockcrypto.com/linked/28748/synthetix-suffers-oracle-attack-potentially-looting-37-million-synthetic-ether)）和管理控制风险的风险，在这些风险中，您委托团队来构建使用的产品。

即使基础架构是透明的，并且任何人都可以使用它的信息，但如今这些风险很难量化，因此很难以交易定价。许多人在这些问题上都在努力工作，例如ConsenSys [最近发布了风险评分系统，](https://media.consensys.net/introducing-the-defi-score-an-open-source-methodology-to-evaluate-code-and-financial-risk-in-defi-6c8616de791c)以及[Nexus Mutual](https://www.nexusmutual.io/)已经开始评估智能合约承保范围以提供智能合约保险（例如，[为Uniswap](https://medium.com/nexus-mutual/understanding-risks-in-defi-1-uniswap-e5e790692635)保险）。在可以为智能合约提供保险并且可以更好地理解与之交易的风险的世界中，与集中交易平台相比，DeFi中的多方套利交易的风险降低了吗？ 

#### 2.2优先天然气拍卖（PGA）

由于套利机会稀少，而优胜者却能获得全部回报，交易者必须优化潜伏期才能有效竞争。相对于传统金融而言，延迟是关于连通性，计算速度优化和诸如共置主机之类的特殊权利的，而在这里，在基于以太坊的基础架构上，延迟与天然气支出和有效的区块链网络监控有关。 

提醒[一下](https://medium.com/@eric.conner/understanding-ethereum-gas-blocks-and-the-fee-market-d5e268bf0a0e)，[以太坊交易会消耗](https://medium.com/@eric.conner/understanding-ethereum-gas-blocks-and-the-fee-market-d5e268bf0a0e)类似于交易费的[汽油](https://medium.com/@eric.conner/understanding-ethereum-gas-blocks-and-the-fee-market-d5e268bf0a0e)，并分配给执行交易的矿工。花费的汽油越多，从内存池中选择要包含在下一个区块中并被确认的交易的机会就越大。将内存池视为确认交易之前的等候室。 

实际上，当交易机器人寻求套利机会时，会发生以下情况： 

* Bot＃1提交了以一定汽油价格包含多个子订单的交易，希望能够根据当前的汽油价格进行交易，这可以在EthGasStation等平台上看到。 
* 同时，机器人＃2可能也发现了相同的机会，或者可以在内存池中看到机器人＃1的交易。 
* 在这两种情况下，机器人＃2都会提交同一笔交易，但要收取稍高的汽油费，以确保矿工会首先选择该交易。 
* 同时，机器人＃1注意到有人试图“抢先”他们并“修改”其交易以包括更高的汽油费。＃1机器人可以有一种策略，希望每隔一段时间就天真地增加其汽油支出，以期获得竞争。
* ...

游戏持续进行，直到其中一个机器人“获胜”或机会变得无利可图（例如，通过降低价差获得汽油支出&gt;总利润），然后他们完全取消了出价，只支付了“取消汽油费”，少于执行费。 

有趣的是，Phil Daian等人在《[Flash Boys 2.0：去中心化交易中的前沿运行，交易重新排序和共识不稳定》一文中](https://arxiv.org/abs/1904.05234)发现，出价机器人通过“抢劫式”合作策略（例如，如果是一个机器人）彼此有机地协作以最大程度地获利。 “不当行为”，拍卖中的另一个人将立即将其出价提高到最大金额，从而消除拍卖的所有获利能力。坚持这样的合作策略所产生的预期收益大于偏离该策略所产生的预期收益。该论文正式描述了该策略，并继续证明对于两个参与者的拍卖存在合作纳什均衡，其中两个参与者都遵循上述严峻触发的合作策略！

您可以可视化在[frontrun.me](https://frontrun.me/)上进行的实时拍卖

![](https://lh3.googleusercontent.com/enYa1Llr4KOOJGEMvKrk_G5NH60emxbLVFDYOAEJGTbXRz1J-NOO91ta5ocUdghk2o6vtHpmYv4K0aOj1gR_J5zCwI9VwqK8RG-LFgQW6ML2BKW3W5ifulqzAAO32GJ8OdpTEcPx)

在以太坊网络上观察到的一个示例PGA。上方的图表显示了两个观察到的漫游器随时间变化的气体出价，而下方的表格则详细说明了每个漫游器所放置的前两个出价和两个挖掘的出价（中心）， 

该图摘自[Flash Boys 2.0 ](https://arxiv.org/abs/1904.05234)第5页[：去中心化交易中的前端运行，事务重新排序和共识不稳定](https://arxiv.org/abs/1904.05234)。尽管一个矿工将拍卖包括在下一个以太坊区块中，拍卖在4.94秒后结束，但机器人只有在该区块被开采并且新的以太坊网络状态传播后才会知道它。因此，他们继续竞标。 

因此，优化汽油支出是最明显的竞争方式。为此，交易员会缩减执行逻辑（因为使用更少的计算来表达同一组指令会减少获得相等结果的汽油支出），并使用[GasToken之类的](https://gastoken.io/)工具在价格较便宜时从本质上提早购买汽油，并在成本更高的情况下使用它，以使他们的交易的经济效益更高。想到GasToken的一种方法就像设置您的电锅炉，以便在非高峰时段加热水，以便您可以在高峰时段使用它。 

![](https://lh4.googleusercontent.com/fKOx3Nnj07MP-gM2a9ucBznGcgeKZPYcUqWhhNhYHlYcP5XGNFJmxmFMWvF2fNICIE44LjDATZtOmAMhddeqzzFZc9BR-Jm_p84Po-Wyt5Hlqj7ysJYW2WhemnbmmK5mz9ZvN-kG)

摘自[Flash Boys 2.0 ](https://arxiv.org/abs/1904.05234)第6页的“已部署的PGA测量基础结构体系结构[：去中心化交易中的前端运行，事务重新排序和共识不稳定”](https://arxiv.org/abs/1904.05234)

除了气体优化外，其他方面的交易者还将参与竞争基础设施（运行时间长且运行更灵活的节点，地理位置分散的节点以监控以太坊内存池）和数据分析功能，我们认为这都是优势所在。 

上面显示了一个基础架构的示例。值得注意的是，使用AWS部署这样的基础架构的成本每月只有五位数。因此，Flashboys 2.0中概述的当前投资机会规模似乎不值得基础架构成本，特别是考虑到Eth2.0八卦拓扑周围的不确定性可能使该基础架构无用。 

此外，除了基础架构之外，还有有效的区块链数据分析问题。虽然要获得内存池的全局图像并非易事，但要选择一个坐在那里的交易，查看触发它的地址及其交易历史，并模拟该交易（及其子交易），以验证它对您而言是一笔净利润是一项艰巨的任务。除此之外，以太坊参与PGA的时间限制为10到20秒（以太坊为传统HFT的微秒），您可以了解有效的数据处理和解析在这些策略中的重要性。尤其如此，因为目前不存在现成的监视工具，因此必须在内部进行开发。（来源：[Bartek Kiepuszweki（MakerDAO）的OasisDEX的过去，现在和未来](https://youtu.be/mwkL7beq0m8)）

要了解有关这些拍卖的更多信息，我建议阅读优秀论文Phil Daian等。以“ [Flash Boys 2.0：去中心化交易中的前沿运行，交易重新排序和共识不稳定”](https://arxiv.org/abs/1904.05234)为主题撰写此部分的标题为“优先气体拍卖（PGA）”。这些PGA令人着迷，因为它们正在改变套利交易者的操作方式并保持其与其他交易者相比的优势。在Cambrial，这很有趣，因为我们花时间与管理人员交谈并了解他们的策略优势。但是，与上一节中关于收益套利机会消失的观点类似，我们认为跨DEX的套利策略将不会保留更长的时间，主要是因为许多方法正在阻止它们，因为它们对DeFi和以太坊不利，但从更广泛的角度来看： 

1. 对以太坊共识安全不利：如Flashboys 2.0中所述，PGA机器人活动通过运行时强盗和基于费用的分叉攻击，为矿工提供了经济诱因，使矿工“过去曾是领先的交易者”。实际上，矿工承担了攻击链条以改写其历史并将自己置于获胜交易的另一端的代价。通过使矿工与以太坊生态系统的其余部分错位，破坏了以太坊的共识安全。更具体地说，您可以想象网络随着相同的块不断被挖掘而有效地停止。
2. 对以太坊带宽不利：GasToken之类的气体优化工具通过向'以太坊'区块填充'幽灵'交易而使以太坊网络膨胀，这通过不必要地提高交易费用对所有以太坊用户产生负面影响。
3. 对做市商不利：每当一个交易所发生突然的价格变动时，都会有一个过渡时期，在其他场所仍然存在错误定价（“过时”）限价订单。自动化交易机器人通过在做市商能够取消订单之前填写这些订单来利用这一优势。因此，与传统交易所相比，这些机器人迫使做市商更广泛地报价，以弥补其损失。这导致每个人的流动性价格更高。具有最近宣布的[气体限制的](https://blog.kyber.network/protocol-parameter-update-107a32a5fdd8) Kyber Network等项目以及与[协调员的](https://blog.0xproject.com/0x-roadmap-2019-part-5-introducing-coordinators-1406365ecbd) 0x等项目已开始采取措施来缓解此类问题。 

#### 3. DeFi中的广义采取策略

恭喜！上面第1部分和第2部分中的TL; DR指出，收益套利和交叉DEX套利策略对于交易者而言都是短暂的机会。前者是因为它传统上为交易者创造的价值正在重新分配给用户，后者是因为它已被完全阻止。那么自然而然的问题就变成了套利者，因为我们传统上知道他们甚至在这个新世界中也占有一席之地？

答案是肯定的，至少目前是这样，因为在某些金融协议中，需要套利者来确保协议的良好运作。一个示例是自动做市商Uniswap，该公司需要在Uniswap货币对池和其他去中心化交易所之间进行持续套利，以使所提供的利率与货币对资产的市场利率保持一致。但是，这种趋势似乎正在转变，并不一定指向套利者的消失，而是对DeFi的含义进行了重新定义。 

重新定义的一个例子是最近宣布的[Balancer](https://balancer.finance/whitepaper.html)：“ Balancer颠覆了指数基金的概念：您无需向投资组合经理支付费用来重新平衡您的投资组合，而是向交易员收取费用，交易员通过跟随套利机会来重新平衡您的投资组合。”

换句话说，套利者通常自己获得的价值部分地重新分配给了现在将享受独特的指数基金产品的用户。但是，尽管套利者被认为对系统有用，但他们的获利能力受到限制。

另一个例子是资产支持的稳定币[DAI](https://docs.ethhub.io/built-on-ethereum/open-finance/stablecoins/dai/)。当DAI低于所需抵押率时，DAI依靠套利者（保管人）清算CDP。这些清算机会对延迟敏感，因此Keepers相互进行优先天然气拍卖来填补这些机会。DAI已设置为从其当前的单抵押系统（即ETH）切换为多抵押DAI（MCD）。发生MCD时，默认情况下，MCD涉及的每个抵押品的清算将切换为英语拍卖。这意味着使用者之间的竞争将是他们内部系统的优化，而不是外部等待时间的游戏。 

![](https://lh4.googleusercontent.com/Rc4PmH5ayLpFgKKaktG0O0xylFwzjsp-V_gAdjAWOc_tFZmlEesa_32vpj4At5QtO8fm8Ql-WiUdKwCUA1EFt6RIi3RtDaikU5i8xuRx1SBiyONbJYaHCQCrLt6--k7hP3t682Ac)

[MKR.tools](https://mkr.tools/system/bites)  三个月的Maker CDP概述，其中每个圆圈代表已清算的CDP。中心是近400万美元的CDP 16619，它在9月24日被清算，当时ETH突然从200美元跌至165美元。这产生了约12万美元的清算利润。

其他DeFi协议也选择使用拍卖，例如使用荷兰式拍卖的令牌集重新平衡和Gnosis的去中心化交易所[DutchX](https://slow.trade/#/)。拍卖通过将竞争转移到价格（以及交易者的内部系统）而不是我们上面看到的网络延迟而引起了很多问题，从而为更健康的DeFi生态系统做出了贡献。最终这将更加公平，并允许更好地发现价格。这再次改变了套利者的定义，因为他拥有内部最佳系统的最佳人选，能够填补对他人无利的机会。我们在这里再次想知道在这样的系统中有限的获利能力将如何。 

这使我们质疑在DeFi中开发交易系统能赚多少钱。这是一个很难回答的问题，因为这些策略的能力和获利能力很难估计，尤其是考虑到上述内容过于简单，实际上，多个策略并行运行，通常具有协同关系。但是，这个问题对我们来说很重要，因为它决定了基金为维持成本而将探索的费用结构，以及当前的机会是否具有足够的吸引力，足以证明必要的团队和对基础设施进行运营的前期投资。

作为策略之间协同关系的一个例子，人们可以在DEX上的ETH / DAI对（流动性最高的货币对）上进行市场交易，同时还机会性地咬住Maker CDP，并避免DAI的任何挂钩偏差。这样，您的DAI库存将保持活动状态，您的做市基础设施也将用于咬MakerCDP +消除钉住的偏差，并且在价格突然贬值后大量清算可用时，您已经有足够的供应来咬CDP ETH。 

#### 结论

DeFi市场在与基于区块链的产品相关的总体交易量中仅占很小的比例。尽管要使交易量增长到有意义的数字还有很长的路要走，但我们已经看到该领域的增长令人鼓舞，并且对其新功能所带来的交易策略感到兴奋。 

但是，我们对上述怀疑策略的怀疑是平衡的，因为上述策略对于交易者而言是短暂的机会，并且隐含着比最初预期更大的风险。对于跨DEX套利和清算溢价之类的策略尤其如此，这些策略被协议构建者用作引导机制，但是当这些网络达到稳定状态时将成为纯粹的阻力。这就提出了一个问题，即这些策略是否可以保证交易者的利益和投资者的工作。

我们建立Cambrial的前提是“加密货币”是一种新的资产类别，并且类似于90年代后期对冲基金的兴起，在新的资产类别中诞生了新的交易机会和策略。这是我们的最佳选择，我们期待着随着这些策略的发展而对它们进行投资。

**致谢：** 

感谢 Cambrial的同事  [Ha](https://twitter.com/HaDuong_)，  [David](https://twitter.com/dfauchier)  和  [Edwar d](https://twitter.com/EdwardMNelson)在整个研究过程中给予的支持，并为此提供了宝贵的反馈意见。

也要感谢[Trent Elmore](https://twitter.com/TrentOfElmore)，[Tom Schmidt](https://twitter.com/tomhschmidt)，[Matteo Leibowitz](http://twitter.com/teo_leibowitz)和BCA小组聊天，以激发对话和反馈。

[cambrial.com](http://cambrial.com/)

[twitter.com/cambrialcapital](https://twitter.com/cambrialcapital)


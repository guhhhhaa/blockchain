# 了解DeFi中的风险：Uniswap

{% embed url="https://medium.com/nexus-mutual/understanding-risks-in-defi-1-uniswap-e5e790692635" %}

## 了解DeFi中的风险：＃1 Uniswap

[![&#x4F11;&#xB7;&#x5361;&#x666E;](https://miro.medium.com/fit/c/96/96/1*Y9Y4wt6PGH6Yq90OdQ_FSg.jpeg)](https://medium.com/@hugh_karp?source=post_page-----e5e790692635----------------------)[休·卡普](https://medium.com/@hugh_karp?source=post_page-----e5e790692635----------------------)跟随[2019年10月2日](https://medium.com/nexus-mutual/understanding-risks-in-defi-1-uniswap-e5e790692635?source=post_page-----e5e790692635----------------------) · 5 分钟阅读

\#DeFi开始获得真正的吸引力，这意味着越来越多的用户正在使用该空间的功能。我们认为了解风险非常重要，尤其是在智能合约仍处于试验阶段时。

为了解释所涉及的风险，我们基于高层框架编写了一系列文章-在很大程度上受已建立的风险管理技术的影响，并使其适应DeFi社区。

接下来将是一系列帖子，这些帖子使用我们提出的框架并将其应用于各种项目和兴趣点。我们很乐意听到您对正在进行的工作的看法和评论。

## 风险框架 <a id="e555"></a>

我们的框架以成熟的风险管理技术为基础，并使用高级定性方法进行评级。首先，我们将风险分为3个主要类别：

### 1.技术风险 <a id="3285"></a>

这就是智能合约无法按照开发人员的预期运行的风险。要编写无错误的代码非常困难，因此始终存在一定程度的技术风险。审计，广泛的测试，形式验证以及如何对合同进行“实战测试”都是可以降低技术风险的因素。

### 2.外部风险 <a id="2da4"></a>

这是外部信息影响智能合约的运行方式而损害其他用户的风险。例如，甲骨文可以提供恶意数据，管理员可以更改系统参数或可以采用治理程序。

### 3.经济激励失败风险 <a id="d0af"></a>

许多智能合约系统，特别是在DeFi领域，都依靠经济激励措施来鼓励网络参与者执行某些操作。这些激励措施可能无法鼓励正确的行为，或者不足以导致其他用户受到不利影响。例如，如果ETH价格下跌得太快，太快，MakerDAO智能合约中的激励措施_可能_过于激进，而DAI &lt;&gt;美元挂钩可能会破裂。

必须承认，这三类风险是特定智能合约的常规用法之外的。例如，如果您使用赌博应用程序，则很明显有可能因正常使用系统而蒙受损失。我们将重点放在这里更严重的风险上，而不是一切正常运行的标准使用中涉及的风险。

## 风险框架 <a id="dfc6"></a>

为了评估使用每个智能合约系统的风险，我们使用了一种标准的定性方法，可以对3种风险类别中的每一种进行评分。重要的是，评级是主观的，类别故意宽泛。目标不是暗示准确性，而是从概念上理解所涉及的风险级别。该框架将每个风险类别分为两个要素：

1. 可能性-事件发生的可能性，可能导致损失。
2. 结果-假设事件发生了，后果将是什么。

![](https://miro.medium.com/max/60/1*ZG2IfnIuK3NwKusMn5Tsig.png?q=20)![](https://miro.medium.com/max/2356/1*ZG2IfnIuK3NwKusMn5Tsig.png)风险管理框架

## 以Uniswap为例 <a id="cef9"></a>

在这一点上，通过一个特定的示例进行工作可能是最简单的。为此，我们将从Uniswap开始。

Uniswap是一种去中心化交易所，具有两种主要用户类型，首先是希望进行代币交易的用户，其次是向Uniswap池提供流动性以换取一部分交易费用的流动性提供者。

我们将从流动性提供者的角度进行分析，因为他们会长期承受这些风险。从交易者的角度可以完成类似的分析。

### 技术风险 <a id="d82d"></a>

**可能性：**与所有智能合约一样，Uniswap的智能合约也面临技术风险。合同相对简单，已经过[审核](https://medium.com/consensys-diligence/uniswap-audit-b90335ac007)，通过了[轻量级的正式验证](https://github.com/runtimeverification/verified-smart-contracts/tree/uniswap/uniswap)，并且还经过了相当程度的“战斗测试”，因此从可能性的角度来看，我们可以将其评为“稀有”（有问题）（我们知道这里有辩论的空间，并鼓励您对这些评分进行反馈。

_请注意，Uniswap 中有一个_[_已知的攻击媒介_](https://blog.openzeppelin.com/exploiting-uniswap-from-reentrancy-to-actual-profit/)_和一些令牌。特别是ERC-777和一些具有扩展功能的更复杂的ERC-20。所有基本的ERC-20令牌都可以。_

**后果：**如果存在错误，则影响可能是“严重的”，因为所有资金都可能被盗或无法使用。

因此，我们通过交叉参考上面的矩阵，在技术风险方面将Uniswap评为“中等”。

### 外部风险 <a id="136f"></a>

Uniswap的定义功能之一是，智能合约没有预言，没有管理权限，也没有治理。它们是完全独立的，是具有此功能的广泛使用的智能合约的少数实例之一。

因此，在这种情况下，实际上没有外部风险。

### 经济激励失败风险 <a id="773d"></a>

Uniswap的唯一实际经济参数是每笔交易0.30％的交易费。这是为了鼓励流动性提供者将其资金放入流动性池中，以便交易者可以使用该协议。如果这笔费用过高或过低，则可能会改变每个集合中的资金水平，进而改变流动性提供者的回报，但对流动性提供者的资本没有影响。

因此，我们认为这种情况下实际上没有经济激励失败的风险。

### Uniswap风险评分摘要 <a id="65e7"></a>

因此，对于Uniswap，我们有以下风险评分：![](https://miro.medium.com/max/50/1*4rJRYPXTk-oL9i-jzF8z_g.png?q=20)![](https://miro.medium.com/max/1168/1*4rJRYPXTk-oL9i-jzF8z_g.png)

### 成为Uniswap流动性提供商 <a id="e2fa"></a>

如果您有兴趣成为Uniswap流动性提供商，我们建议您调查历史收益，并加深对流动性池资产随价格变动而变化的方式的了解。作为流动性提供者，由于汇率将在您的出入点之间变动，您可能会获得提供的两种资产的不同比率。

在收益方面，在过去的三个月中，DAI：ETH池中的[Uniswap收益](https://zumzoom.github.io/analytics/uniswap/roi.html)约为5.53％，并且随流动性池的大小和交易量而变化。![](https://miro.medium.com/max/60/1*2K3o2FHOBQK1-Lpxt3zvIw.png?q=20)![](https://miro.medium.com/max/3830/1*2K3o2FHOBQK1-Lpxt3zvIw.png)Uniswap DAI：以太坊池收益

### Uniswap +智能合约封面 <a id="beb2"></a>

Nexus Mutual的智能合约保障可用于减轻使用Uniswap的智能合约涉及的技术风险。作为索赔将在智能合约失败的情况下支付。Uniswap上智能合约保险的当前报价为每年1.3％。

作为ETH：DAI流动性提供商，您现在有两种选择：

1. 赚5.5％并承担智能合约的技术风险
2. 净赚4.2％，减轻智能合约的技术风险。

购买智能合约保险可以将您的风险评分调整为以下各项：![](https://miro.medium.com/max/60/1*VSYf9LEQjw6EFJJGFOM6rA.png?q=20)![](https://miro.medium.com/max/1978/1*VSYf9LEQjw6EFJJGFOM6rA.png)

通过输入uniswap.nexusmutual.eth作为智能合约地址，您可以在Uniswap的智能合约封面上获得[报价](https://app.nexusmutual.io/#/SmartContractCover)。[Nexus Mutual](https://medium.com/nexus-mutual?source=post_sidebar--------------------------post_sidebar-)

**以人为本的替代保险。基于区块链的共同平台 建立在以太坊上。**

跟随

**286**

**感谢Kayleigh Petrie 。** 


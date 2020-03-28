# 【ICO】如何以简单方式创建ERC20令牌

## [https://www.toptal.com/ethereum/create-erc20-token-tutorial](https://www.toptal.com/ethereum/create-erc20-token-tutorial)

## 如何以简单方式创建ERC20令牌

本文的目的是演示如何在尽可能短的时间内创建ERC20令牌。

让我们从基础开始：_什么是ERC20令牌？_

近年来，ERC20令牌规范已成为以太坊令牌的事实上的标准。换句话说，当今大多数以太坊合同都符合ERC20。本文将详细介绍如何创建自己的以太坊令牌，但是在开始之前，让我们仔细看看ERC20标准。

![ERC20&#x4EE4;&#x724C;&#x56FE;](https://uploads.toptal.io/blog/image/127334/toptal-blog-image-1539181697913-90cdece406de0c3caf6a57f3444bf553.png)

是什么使ERC20代币如此有吸引力和成功呢？有几个因素在起作用：

1. 正如您将在本教程中看到的那样，ERC20令牌既简单又易于部署。
2. ERC20标准解决了一个重大问题，因为基于区块链的市场和加密货币钱包需要一套标准化的命令来与其管理的令牌范围进行通信。这包括不同代币之间的交互规则，以及代币购买规则。
3. 它是第一个提供以太坊令牌标准化的流行规范。它绝对不是_第一个_，但是由于它的流行，它很快成为了行业标准。

与其他以太坊令牌一样，ERC20令牌被实现为智能合约，并以分散的方式在以太坊虚拟机（EVM）上执行。

### 可靠性：智能合约编程语言 <a id="solidity-the-smart-contract-programming-language"></a>

以太坊智能合约以Solidity编写。尽管存在替代语言，但几乎没有人为此目的使用它们。Solidity与JavaScript相似，因此，如果您对JavaScript甚至Java和其他类似C的语言有一定的了解，那么即使您真正掌握了Solidity足以使用的知识，您也可以毫无疑问地确定Solidity中的一段代码可以做到。它。

这就是乐趣的开始，因为您应该能够立即开始创建简单的ERC20合同。这是一项简单的任务，非常简单，因此本文将演示如何在一个小时内编写和部署ERC20令牌。

我们将在此演示中创建的令牌将是一个简单的ERC20实现，而没有太多的麻烦。但是，我在现实世界中看到了许多类似的简单令牌，它们往往做得很好。

### ERC20代币标准概述 <a id="overview-of-erc20-token-standard"></a>

#### 什么是ERC20？ <a id="what-is-erc20"></a>

简而言之，ERC20标准定义了一组由所有ERC20代币实现的功能，以便与其他合同，钱包或市场进行集成。这套功能相当简短和基本。

```java
function totalSupply() public view returns (uint256);
function balanceOf(address tokenOwner) public view returns (uint);
function allowance(address tokenOwner, address spender)
public view returns (uint);
function transfer(address to, uint tokens) public returns (bool);
function approve(address spender, uint tokens)  public returns (bool);
function transferFrom(address from, address to, uint tokens) public returns (bool);
```

ERC20功能允许外部用户（例如，加密钱包应用程序）找出用户的余额，并通过适当的授权将资金从一个用户转移到另一个用户。

智能合约定义了两个明确定义的事件：

```java
event Approval(address indexed tokenOwner, address indexed spender,
 uint tokens);
event Transfer(address indexed from, address indexed to,
 uint tokens);
```

当授予用户从帐户中撤回令牌的权限时，以及在实际转移令牌之后，将调用或_发出_这些事件。

除了标准的ERC20功能外，许多ERC20令牌还具有其他字段，并且即使不是书面形式，也实际上已成为ERC20标准的实际部分。以下是此类字段的一些示例。

```java
string public constant name;
string public constant symbol;
uint8 public constant decimals;
```

以下是有关ERC20和Solidity命名法的几点：

* 一个`public`功能可以是合同本身的外部访问的
* `view` 本质上是指常量，即合约的内部状态不会被该功能更改
* 这`event`是Solidity的一种方式，它允许客户（例如，您的应用程序前端）在合同中发生的特定情况下得到通知

如果您已经具备基本的Java / JavaScript技能，则大多数Solidity语言构造应该清楚。

#### 牢固地编写ERC20令牌 <a id="writing-an-erc20-token-in-solidity"></a>

![&#x575A;&#x56FA;&#x7684;ERC20&#x4EE3;&#x5E01;](https://uploads.toptal.io/blog/image/127335/toptal-blog-image-1539181714183-62a47883ea777f12969345038389fb22.png)

现在，我们已经概述了基础知识并解释了创建ERC20令牌所需的时间，是时候开始编写一些逻辑了。

首先，我们需要定义两个映射对象。这是关联或键/值数组的Solidity概念：

```java
mapping(address => uint256) balances;
mapping(address => mapping (address => uint256)) allowed;
```

表达式`mapping(address => uint256)`定义了一个关联数组，其键型的`address`-用于表示帐户地址，并且其值是类型的数`uint256` 的256位整数通常用于存储令牌余额- 。

第一个映射对象，`balances`将保存每个所有者帐户的令牌余额。

第二个映射对象，`allowed`将包括所有获准从给定帐户中提取的帐户以及每个帐户允许的提取金额。

如您所见，允许的映射的value字段本身就是映射绘图帐户地址到其批准的取款金额的映射。

这些映射以及所有其他合同字段将存储在区块链中，并将被_挖掘，_从而将更改传播到所有网络用户节点。

区块链存储非常昂贵，您合同的用户将需要以一种或另一种方式付费。因此，您应始终尝试最小化存储大小并写入区块链。

现在我们已经有了所需的数据结构，我们可以开始将ERC20逻辑实际写入适当的函数中了。

### 设置ICO代币数量 <a id="setting-the-number-of-ico-tokens"></a>

我们如何设置ICO代币数量？嗯，有很多方法可以设置ICO令牌的最大数量，而这件事本身值得进行冗长的讨论。

为了满足我们的ECR20教程的需求，我们将使用最简单的方法：在合同创建时设置令牌的总量，并首先将所有令牌分配给“合同所有者”，即部署智能合同的帐户：

```java
uint256 totalSupply_;
constructor(uint256 total) public {
   totalSupply_ = total;
   balances[msg.sender] = _totalSupply;
}
```

构造函数是在部署合同后立即由以太坊自动调用的特殊功能。它通常用于通过合同的部署帐户传递的参数来初始化令牌的状态。

`msg`是由以太坊本身声明和填充的全局变量。它包含执行合同的重要数据。我们在此处使用的字段：`msg.sender`包含执行当前合约功能的以太坊账户。

只有部署帐户可以输入合同的构造函数。合同启动时，此功能会将可用令牌分配给“合同所有者”帐户。

### 获取总代币供应 <a id="get-total-token-supply"></a>

```java
function totalSupply() public view returns (uint256) {
  return totalSupply_;
}
```

此函数将返回此合同分配的所有令牌的数量，而与所有者无关。

### 获取所有者的代币余额 <a id="get-token-balance-of-owner"></a>

```java
function balanceOf(address tokenOwner) public view returns (uint) {
  return balances[tokenOwner];
}
```

`balanceOf` 将返回帐户的当前令牌余额，由帐户所有者的地址标识。

### 将令牌转移到另一个帐户 <a id="transfer-tokens-to-another-account"></a>

```java
function transfer(address receiver,
                 uint numTokens) public returns (bool) {
  require(numTokens <= balances[msg.sender]);
  balances[msg.sender] = balances[msg.sender] — numTokens;
  balances[receiver] = balances[receiver] + numTokens;
  emit Transfer(msg.sender, receiver, numTokens);
  return true;
}
```

顾名思义，该`transfer`功能用于将`numTokens`令牌数量从所有者的余额转移到另一个用户的，或`receiver`。转让所有者`msg.sender`即执行该功能的所有者，这意味着只有令牌的所有者才能将其转让给他人。

Solidity断言的方式为`require`。在这种情况下，转帐帐户有足够的余额来执行转帐。如果`require`声明失败，则交易将立即回滚，而不会将任何更改写入区块链。

在退出之前，该函数会触发ERC20事件，`Transfer`允许已注册的侦听器对其完成做出反应。

### 批准代表提取代币 <a id="approve-delegate-to-withdraw-tokens"></a>

此功能最常用于令牌市场场景中。

```java
function approve(address delegate,
                uint numTokens) public returns (bool) {
  allowed[msg.sender][delegate] = numTokens;
  emit Approval(msg.sender, delegate, numTokens);
  return true;
}
```

什么`approve`确实是让业主即`msg.sender`批准代理帐户-可能是市场本身-退出从他的账户代币，并将其转移到其他账户。

如您所见，此功能用于所有者在市场上提供令牌的方案。它允许市场在无需等待事先批准的情况下完成交易。

执行结束时，此函数将触发一个`Approval`事件。

#### 获取批准提取的代币数量 <a id="get-number-of-tokens-approved-for-withdrawal"></a>

```text
function allowance(address owner,
                  address delegate) public view returns (uint) {
  return allowed[owner][delegate];
}
```

此函数将所有者当前批准的令牌数量返回给特定的委托，如在`approve`函数中设置的那样。

#### 通过委托转移代币 <a id="transfer-tokens-by-delegate"></a>

所述`transferFrom`函数是对端`approve`功能，这是我们前面所讨论的。它允许批准撤回的代表将所有者资金转移到第三方帐户。

```java
function transferFrom(address owner, address buyer,
                     uint numTokens) public returns (bool) {
  require(numTokens <= balances[owner]);
  require(numTokens <= allowed[owner][msg.sender]);
  balances[owner] = balances[owner] — numTokens;
  allowed[owner][msg.sender] =
        allowed[from][msg.sender] — numTokens;
  balances[buyer] = balances[buyer] + numTokens;
  Transfer(owner, buyer, numTokens);
  return true;
}
```

`require`函数启动时的两条语句用于验证交易是否合法，即所有者拥有足够的令牌来转让，以及委托人具有（至少）`numTokens`撤回的批准。

除了将`numTokens`金额从所有者转移到买方之外，此功能还`numTokens`从代表的津贴中扣除。基本上，这允许具有给定限额的代表将其分成几个单独的提款，这是典型的市场行为。

我们可以在这里停下来，并有一个有效的ERC20实施方案。但是，我们想要更进一步，因为我们想要一个具有工业实力的代币。这要求我们使代码更加安全，尽管我们仍然能够使令牌相对简单（即使不是基本的）。

### SafeMath Solidity库 <a id="safemath-solidity-library"></a>

[_SafeMath_](https://openzeppelin.org/api/docs/math_SafeMath.html)是一个[ _Solidity_](https://openzeppelin.org/api/docs/math_SafeMath.html)库，旨在处理已知的破坏合同的一种方式：整数溢出攻击。在这种攻击中，黑客通过传递将使相关整数**超过**其最大值的参数来强迫合同使用不正确的数值。

![Solidity&#x4E2D;&#x7684;Safemath&#x5E93;&#xFF1A;&#x63D2;&#x56FE;](https://uploads.toptal.io/blog/image/127336/toptal-blog-image-1539181732450-e81e93f6028bd7db90c30d5a1814195d.png)

_SafeMath_通过在执行算术操作之前测试溢出情况来防止这种情况的发生，从而消除了溢出攻击的危险。该库是如此之小，以至于对合同规模的影响最小，不会产生任何性能，并且几乎不会增加存储成本。

让我们将_SafeMath_添加到我们的代码中：

```text
library SafeMath { // Only relevant functions
function sub(uint256 a, uint256 b) internal pure returns (uint256) {
  assert(b <= a);
  return a — b;
}
function add(uint256 a, uint256 b) internal pure returns (uint256)   {
  uint256 c = a + b;
  assert(c >= a);
  return c;
}
}
```

_SafeMath_使用`assert`语句来验证所传递参数的正确性。如果`assert`失败，函数执行将立即停止，所有区块链更改应回滚。

接下来，让我们添加以下语句，将库引入Solidity编译器：

`using SafeMath for uint256;`

然后，我们用SafeMath函数替换开始时使用的朴素算法：

```text
balances[msg.sender] = balances[msg.sender].sub(numTokens);
balances[receiver] = balances[receiver].add(numTokens);
balances[buyer] = balances[buyer].add(numTokens);
balances[owner] = balances[owner].sub(numTokens);
```

**打包在一起**

在Solidity中，智能合约的功能和事件被包装到称为_合约_的实体中，您可以将其静默转换为“区块链类”。下面是我们创建的与ERC20兼容的合同，其中包括代码要点。名称和符号字段可以随意更改。大多数令牌将十进制值保持为18，因此我们将执行相同的操作。

#### 以太坊合约部署 <a id="ethereum-contract-deployment"></a>

现在是[将我们的合同部署到区块链的时候了](https://www.toptal.com/ethereum-smart-contract/time-locked-wallet-truffle-tutorial)。部署后，我们的合同将被转移到参与网络的所有节点。对合同所做的所有更改都将传播到所有参与节点。

以太坊开发人员通常会使用[Truffle](https://truffleframework.com/)等部署工具。就本文的有限需求而言，即使是Truffle也是过大的，并且一个叫做[Remix](https://remix.ethereum.org/)的简单在线工具就足够了。

要使用它，您需要在浏览器上安装[MetaMask插件](https://chrome.google.com/webstore/detail/metamask/nkbihfbeogaeaoehlefnkodbefgpgknn?hl=en)，并在其中至少装有一些Rinkeby Ether的Rinkeby（以太坊测试网络）帐户中安装。这些是相对简单的步骤，因此我们将不做详细介绍。

如果您都没有，请访问[MetaMask](https://metamask.io/)和[Rinkeby](https://www.rinkeby.io/#stats)以获取下载链接，并获得清晰的安装和使用说明。

现在我们已经有了所有的构建块，我们将转到[Remix](https://remix.ethereum.org/)并将上面的代码（包括pragma行和SafeMath库）粘贴到在线编辑器中。

然后，我们将跳至右侧第二个选项卡，称为“ **运行** ”，然后单击“ **部署”**。会出现一个MetaMask弹出窗口，要求我们确认交易。当然，我们会批准。

![&#x56FE;&#x7247;&#x66FF;&#x4EE3;&#x6587;&#x5B57;](https://uploads.toptal.io/blog/image/127337/toptal-blog-image-1539181745550-fe4de03d6ec83c06cae3c092ae235c0a.png)

* _绿框：确保您在Rinkeby上_
* _蓝框：设置总令牌供应量_
* _红框：部署！_

**要点**：[https](https://gist.github.com/giladHaimov/8e81dbde10c9aeff69a1d683ed6870be#file-basicerc20-sol) : [//gist.github.com/giladHaimov/8e81dbde10c9aeff69a1d683ed6870be\#file-basicerc20-sol](https://gist.github.com/giladHaimov/8e81dbde10c9aeff69a1d683ed6870be#file-basicerc20-sol)

**恭喜！**您刚刚部署了第一个ERC20令牌，就像真正的[以太坊专家一样](https://www.toptal.com/ethereum)。如所承诺的那样，该令牌既简单又轻便，但功能齐全，符合ERC20标准，并由MathSafe进行保护。它随时可以在整个区块链中购买，付款和转移。

**这就是智能合约的全部内容吗？**

不，甚至不接近，因为我们的简短演示几乎没有涉及表面，仅涉及智能合约开发的一个方面。

根据您的业务逻辑，对用户交互的建模，是否允许令牌铸造和刻录，合同中引入的生命周期更改，对管理级别功能的需求（通常随合同附带），智能合约可能会更加复杂。管理员授权的功能集，等等。您得到图片。

不过，如果您可以复制我们在这里所做的工作，那么这将是扩展您的知识并在必要时转向更复杂的合同的坚实基础。


# 【ICO】分步指南：如何创建自己的以太坊ERC-20令牌

{% embed url="https://blockonomi.com/create-ethereum-token/" %}

## 分步指南：如何创建自己的以太坊ERC-20令牌

有关如何在以太坊网络上创建和部署自己的ERC-20令牌的完整教程-您所需的所有代码

![&#x521B;&#x5EFA;&#x4E00;&#x4E2A;ERC-20&#x4EE4;&#x724C;](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/create-erc-20-token-1-770x515.jpg)

这是我们的第二本Solidity教程，如果您错过了它，请看一下《 Solidity [简介》，](https://blockonomi.com/solidity-tutorial/)其中带您逐步了解以太坊区块链这种编程语言的一些基础知识。

我们向您解释了Solidity的工作原理，结构方式，并以编写“ Hello World”智能合约的一些简单代码开始。

在本教程中，我们会更深入地讲授代码以部署您自己的以太坊ERC-20令牌。（这是我们的[Blockonomi令牌](https://ropsten.etherscan.io/token/0xcaed5a2327083f55a29224f91576217ab19dfc0e)）。

### 以太坊和ICO繁荣

目录\[ [显示](https://blockonomi.com/create-ethereum-token/#) \]

ICO代表初始代币发行，它是一种使用加密货币的融资。在ICO中，一定数量的加密货币以“代币”（“硬币”）的形式出售给投机者或投资者，以换取法定货币或其他加密货币，例如比特币或以太坊。

如果达到ICO的资金目标并启动项目，则出售的代币将作为未来的货币功能单位进行推广。

我们已经讨论过智能合约如何为开发人员创造和创新打开一个全新的世界。但是，这些开发人员需要一种为其项目筹集资金的方法。

解决方案是ICO。

在2017年，ICO蓬勃发展-每天都有无数的项目出现，它们对实现目标的承诺令人wild然，投资者对此予以l顾。

从那以后，随着空间的成熟和投资者的消失，事情变得平静了，许多ICO未能兑现承诺的承诺，但这是另一篇文章的故事–我们在这里讨论技术方面。

### 什么是代币？

代币本质上是存在于以太坊区块链上的智能合约，它们可以具有可能的用途和目的。

令牌不限于一个特定角色。它可以在其本地生态系统中扮演许多角色。这是令牌可以扮演的一些角色的列表。

* **收费**：令牌可以充当Dapp的网关。基本上，为了访问Dapp，您将需要持有令牌。
* **投票权**：令牌还可以使持有人有一定的投票权。想想EOS，持有EOS代币将使您能够投票给区块生产者。EOS区块链旨在成为可支持工业规模去中心化应用程序的去中心化操作系统。
* **价值交换**：这是令牌在生态系统中较常见的角色之一。令牌可以帮助在应用程序内创建内部经济系统。
* **用户体验增强**：令牌还可以使持有人在特定环境的范围内丰富用户体验。例如。在Brave（Web浏览器）中，BAT（Brave中使用的令牌）的持有者将有权使用其令牌在Brave平台上添加广告或其他基于关注的服务来丰富客户体验。
* **货币**：可以用作价值存储，可以用于在给定生态系统内外进行交易。

### 什么是ERC-20？

ERC-20是用于以太坊区块链上智能合约以实现令牌的技术标准。以太坊区块链上发行的大多数代币都符合ERC-20。

ERC-20是一个协议标准，定义了在以太坊网络上发行令牌的某些规则和标准。在“ ERC-20”中，ERC代表以太坊请求注释，而20代表唯一的ID号，以区别于其他标准。

为简单起见，ERC-20是规则和法规的指南，可帮助创建基于以太坊的智能合约创建其令牌的蓝图。

以太坊上的令牌基本上只是遵循一些通用规则的智能合约-即，它实现了所有其他令牌合约共享的一组标准功能，例如_transferFrom（address \_from，address \_to，uint256 \_tokenId）_和_balanceOf（address \_owner）_。

因此，基本上，令牌只是一种合约，可以跟踪谁拥有该令牌的多少以及一些功能，以便那些用户可以将其令牌转移到其他地址。

### 为什么ERC-20标准如此重要？

由于所有ERC-20令牌都使用相同的名称共享相同的功能集，因此它们都可以以相同的方式进行交互。

这意味着，如果您构建的应用程序能够与一个ERC-20令牌进行交互，那么它也能够与任何ERC-20令牌进行交互。这样，将来就可以轻松地将更多令牌添加到您的应用中，而无需进行自定义编码。您只需插入新的令牌合同地址，然后繁荣，您的应用程序即可使用另一个令牌。

交换就是一个例子。当交易所添加新的ERC-20令牌时，实际上只需要添加与之对话的另一个智能合约。用户可以告诉该合同将令牌发送到交易所的钱包地址，而交易所可以告诉合同在用户提款时将令牌发送回给用户。

交易所只需要实现一次该转移逻辑，然后当它想添加新的ERC-20令牌时，只需将新的合同地址添加到其数据库即可。

### 让我们开始创建令牌

我们将使用Remix IDE为ERC-20令牌开发智能合约。

Remix是一种在线工具，可让您编写Solidity智能合约，然后进行部署和运行。

只需从您的浏览器访问[https://remix.ethereum.org](https://remix.ethereum.org/)，我们就可以开始编码。

![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture1-1.png)

单击“ Solidity”按钮，然后单击左上角的“加号”按钮。

我将其命名为“ BlockonomiToken”，您可以为自己的加密货币选择任何喜欢的名称。

![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture2.png)

很好，一切都已设置完毕。

### ERC-20令牌规则

ERC-20令牌遵循一系列规则，以便可以共享，交换其他令牌或将其转移到加密钱包。

ERC20标准包含3个可选规则和6个强制性规则。

用外行术语来说，如果您在代币的智能合约中包含某些功能，则说明您符合ERC20。如果您不包括强制性功能，则您不是ERC20。

强制性规则如下：

1. 总供应
2. balanceOf
3. 传递
4. transferFrom
5. 批准
6. 津贴

另一方面，可选规则是：

1. 代币名称
2. 符号
3. 小数（最多18个）

通常在接口中定义这些规则。在Solidity中并没有真正叫做接口的东西，它只是另一个智能合约。幸运的是，人们可以继承Solidity编程语言的智能合约。

### 继承性

在Solidity中，继承与经典的面向对象编程语言非常相似。首先，您要编写基本合同，并告诉您新合同将继承于基本合同。

```text
contract IBank {
  // base contract code...
}

contract Bank is IBank {
  // inherited contract code...
}
```

您还需要知道Solidity通过复制包括多态性的代码来支持多重继承。

所有函数调用都是虚拟的，这意味着将调用派生程度最高的函数，除非明确指定了合同名称。

当合同从多个合同继承时，在区块链上仅创建一个合同，并将所有基本合同的代码复制到创建的合同中。

让我们回到我们的ERC-20令牌。为了创建ERC-20令牌，我们具有强制性规则。

我们将它们定义为6个函数并将其写入接口。然后，我们实际的令牌合同将继承该so调用接口。

您的代码将需要如下所示。

```text
contract ERC20Interface {
    function totalSupply() 
		public 
		view 
		returns (uint);

    function balanceOf(address tokenOwner) 
		public 
		view 
		returns (uint balance);
    
	function allowance
		(address tokenOwner, address spender) 
		public 
		view 
		returns (uint remaining);

    function transfer(address to, uint tokens) 				public 
		returns (bool success);
    
	function approve(address spender, uint tokens) 		public 
		returns (bool success);

    function transferFrom 
		(address from, address to, uint tokens) 				public 
		returns (bool success);


    event Transfer(address indexed from, address indexed to, uint tokens);
    event Approval(address indexed tokenOwner, address indexed spender, uint tokens);
}
```

![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture3.png)

### 代币合约

让我们创建我们的代币合约。输入**合同** &lt;Name\_of\_token&gt; {}

现在，我们将通过3个可选规则。

即使不必命名您的令牌，但给它一个标识仍然很重要。

接下来，我们有符号。我们根本不能低估它们的重要性。醒目的标志有助于更好的品牌塑造。

最后，我们具有可除性，这将有助于我们确定令牌的最低可能值。可除数为0表示令牌的最小值为1。另一方面，可除数为2表示其最小值将为0.01。强烈建议默认的小数位数最大为18。建议使用18个小数，请避免对其进行更改

让我们定义它们并在构造函数中初始化。

```text
contract BlockonomiToken is ERC20Interface {
    string public name;
    string public symbol;
    uint8 public decimals; 
    

    constructor() public {
        name = "BlockonomiToken";
        symbol = "BKM";
        decimals = 18;
    }
}
```

我们的代币还需要有初始供应，以及所有余额的一些记录。我们可以将该信息存储在数组中。

在构造函数中，我们将使用向合同创建者（即**msg.sender**）的初始供应令牌初始化合同。将这些行添加到我们的代码中，我们将讨论所有这些行的目的。

```text
contract BlockonomiToken is ERC20Interface {
    string public name;
    string public symbol;
    uint8 public decimals;
    
    uint256 public _totalSupply;
    
    mapping(address => uint) balances;
    mapping(address => mapping(address => uint)) allowed;
    

    constructor() public {
        name = "BlockonomiToken";
        symbol = "BKM";
        decimals = 18;
        _totalSupply = 100000000000000000000000000;
        
        balances[msg.sender] = _totalSupply;
        emit Transfer(address(0), msg.sender, _totalSupply);
    }
}
```

### 实体数据类型

如您所见，_\_totalSupply_具有**uint256**数据类型和_十进制_ **uint8**。

统一性是一种静态类型的语言，这意味着需要在编译时指定每个变量的类型（状态和局部）。实体提供了几种基本类型，可以将它们组合起来以形成复杂类型。

现在让我们讨论整数类型。

整数可以是**int**或**uint**：各种大小的有符号和无符号整数。如果您熟悉计算机科学理论，或者您知道C语言中有符号整数和无符号整数之间的区别，那么Solidity中的一切都绝对相同。

如果不是的话，我们只能说**unsigned是一个永远不能为负的整数！**另一方面，签订的合同既可以是正面的，也可以是正面的，但是我们将仅在合同中使用单位。

关键字uint8到uint256的步长为8（8个无符号数，最多256位），以及int8到int256。uint和int分别是uint256和int256的别名。

我们说过，我们将以某种形式存储余额。好吧，更好的解决方案是使用哈希表或在Solidity映射中。

基本上，我们将**address**（也是数据类型）映射到**uint**。

msg.sender（地址）：消息的发件人（当前通话）

**msg.sender**将是当前与合同建立联系的人。

稍后，您可能会处理与合同相关的合同。在这种情况下，创建调用的合同将为**msg.sender**。

### 对应

映射类型声明为**mapping（**_**\_KeyType**_ **=&gt;** _**\_ValueType**_**）**。_\_KeyType_在这里_几乎_可以是任何类型，除了映射，动态大小的数组，协定，枚举和结构。_\_ValueType_实际上可以是任何类型，包括映射。

映射可以看作是哈希表，实际上已经进行了初始化，因此每个可能的键都存在，并且映射到一个其字节表示全为零的值：一种类型的默认值。但是，相似性到此结束：关键数据实际上没有存储在映射中，只有其keccak256哈希用于查找值。

因此，映射没有长度或键或值被“设置”的概念。

只有状态变量（或内部函数中的存储引用类型）才允许使用映射。

可以将映射标记为公共，并让Solidity创建吸气剂。该_\_KeyType_将成为吸气必需的参数，它会返回_\_ValueType_。

该_\_ValueType_可以是映射了。对于每个_\_KeyType_，getter都将有一个参数，递归地。

### 大事记

区块链是一个块列表，从根本上讲就是交易列表。每个事务都有一个附件收据，其中包含零个或多个日志条目。日志条目表示从智能合约触发的事件的结果。

在Solidity源代码中，要定义事件，您可以在**事件**之前加上**event**关键字（用法类似于function关键字）来对其进行标记。ÿ

然后，您可以在希望引起该事件的任何函数的主体中调用或触发该事件。（我怀疑是否有标准的措词）。您可以使用**发出**关键字从任何函数触发事件。

![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture4-1-1024x649.png)

### ERC-20接口

让我们现在实现ERC-20接口。为此，我们需要为所有六个强制性功能编写代码。

#### 1.总_供应量_

标识创建的ERC-20令牌的总数。该方法的目的是确定围绕生态系统浮动的令牌总数。

```text
function totalSupply() 
	public 
	view 
	returns (uint) 
{
    return _totalSupply - balances[address(0)];
}
```

#### 2. _balanceOf_ 

返回特定地址（在这种情况下，合约所有者）在其帐户中拥有的令牌数量。

```text
function balanceOf(address tokenOwner) 
	public 
	view 
	returns (uint balance) 
{
    return balances[tokenOwner];
}
```

#### 3. _津贴_

为了进行交易，合同应该知道的最重要的数据之一是用户的余额。毕竟，用户应具有进行交易所需的最少令牌数量。

因此，ERC-20合同还包含allowance（）函数。如果用户没有最少数量的令牌，该函数将取消交易。

```text
function allowance
	(address tokenOwner, address spender) 
	public 
	view 
	returns (uint remaining) 
{
    return allowed[tokenOwner][spender];
}
```

#### 4. _批准_

一旦检查完余额，合同所有者就可以批准用户，以从合同地址中收集所需数量的令牌。

批准功能还会根据令牌的总供应量检查交易，以确保没有遗漏或多余。

换句话说，它确保了仿冒是不可能的。

```text
function approve(address spender, uint tokens) 			public 
	returns 
	(bool success) 
{
    allowed[msg.sender][spender] = tokens;
    emit Approval(msg.sender, spender, tokens);
    return true;}
```

![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture23.png)

### 安全数学库

为了正确实现剩余的两个功能，我们需要安全数学库。

安全数学库通过增加的溢出检查包装了Solidity的算术运算。

Solidity中的算术运算会在溢出时自动换行。这很容易导致错误，因为程序员通常认为溢出会引发错误，这是高级编程语言中的标准行为。

当操作溢出时，Safe Math通过还原事务来恢复这种直觉。

使用此库而不是未经检查的操作可以消除整个错误类别，因此建议始终使用它。

现在我们要做的就是将代码复制到合同上方，然后继承它。

```text
contract SafeMath {
    function safeAdd(uint a, uint b) public pure returns (uint c) {
        c = a + b;
        require(c >= a);
    }
    function safeSub(uint a, uint b) public pure returns (uint c) {
        require(b <= a); c = a - b; } function safeMul(uint a, uint b) public pure returns (uint c) { c = a * b; require(a == 0 || c / a == b); } function safeDiv(uint a, uint b) public pure returns (uint c) { require(b > 0);
        c = a / b;
    }
}
```

不要忘记继承它。

```text
contract BlockonomiToken is ERC20Interface, SafeMath
```

![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture25.png)

#### 5. _转移_

因此，既然所有检查都已经完成，并且合同知道用户具有完成交易所需的令牌数量，那么合同所有者可以使用transfer（）函数向他们发送令牌。

就像常规的加密货币交易一样，此功能使合同的所有者可以将给定数量的令牌发送到另一个地址，从而允许将一定数量的令牌从总供应量转移到用户帐户。

```text
function transfer(address to, uint tokens) 
	public 
	returns (bool success) 
{
    balances[msg.sender] = safeSub(balances[msg.sender], tokens);
    balances[to] = safeAdd(balances[to], tokens);

    emit Transfer(msg.sender, to, tokens);
    return true;
}
```

#### 6. _transferFrom_

我们已经介绍了传递函数，为什么还有另一个？

好，让我们举个例子看看为什么transferFrom是ERC20合同的如此出色的补充。

像发条一样，我们每个月都必须支付一些钱。它可能是您的租金，账单等。您实际上并不需要亲自支付所有这些费用。您始终可以与银行一起建立自动付款系统来处理这些付款。

这就是transferFrom（）允许您执行的操作。它可以帮助您自动将付款转账到特定帐户。

```text
function transferFrom
	(address from, address to, uint tokens) 
	public 
	returns (bool success) 
{
    balances[from] = safeSub(balances[from], tokens);
    allowed[from][msg.sender] = safeSub(allowed[from][msg.sender], tokens);
    balances[to] = safeAdd(balances[to], tokens);
        
	emit Transfer(from, to, tokens);
    return true;
}
```

### 完整代码

这是我们的Blockonomi令牌的完整代码。

```text
pragma solidity ^0.5.0;

// ----------------------------------------------------------------------------
// ERC Token Standard #20 Interface
//
// ----------------------------------------------------------------------------
contract ERC20Interface {
    function totalSupply() public view returns (uint);
    function balanceOf(address tokenOwner) public view returns (uint balance);
    function allowance(address tokenOwner, address spender) public view returns (uint remaining);
    function transfer(address to, uint tokens) public returns (bool success);
    function approve(address spender, uint tokens) public returns (bool success);
    function transferFrom(address from, address to, uint tokens) public returns (bool success);

    event Transfer(address indexed from, address indexed to, uint tokens);
    event Approval(address indexed tokenOwner, address indexed spender, uint tokens);
}

// ----------------------------------------------------------------------------
// Safe Math Library 
// ----------------------------------------------------------------------------
contract SafeMath {
    function safeAdd(uint a, uint b) public pure returns (uint c) {
        c = a + b;
        require(c >= a);
    }
    function safeSub(uint a, uint b) public pure returns (uint c) {
        require(b <= a); c = a - b; } function safeMul(uint a, uint b) public pure returns (uint c) { c = a * b; require(a == 0 || c / a == b); } function safeDiv(uint a, uint b) public pure returns (uint c) { require(b > 0);
        c = a / b;
    }
}


contract BlockonomiToken is ERC20Interface, SafeMath {
    string public name;
    string public symbol;
    uint8 public decimals; // 18 decimals is the strongly suggested default, avoid changing it
    
    uint256 public _totalSupply;
    
    mapping(address => uint) balances;
    mapping(address => mapping(address => uint)) allowed;
    
    /**
     * Constrctor function
     *
     * Initializes contract with initial supply tokens to the creator of the contract
     */
    constructor() public {
        name = "BlockonomiToken";
        symbol = "BKM";
        decimals = 18;
        _totalSupply = 100000000000000000000000000;
        
        balances[msg.sender] = _totalSupply;
        emit Transfer(address(0), msg.sender, _totalSupply);
    }
    
    function totalSupply() public view returns (uint) {
        return _totalSupply  - balances[address(0)];
    }
    
    function balanceOf(address tokenOwner) public view returns (uint balance) {
        return balances[tokenOwner];
    }
    
    function allowance(address tokenOwner, address spender) public view returns (uint remaining) {
        return allowed[tokenOwner][spender];
    }
    
    function approve(address spender, uint tokens) public returns (bool success) {
        allowed[msg.sender][spender] = tokens;
        emit Approval(msg.sender, spender, tokens);
        return true;
    }
    
    function transfer(address to, uint tokens) public returns (bool success) {
        balances[msg.sender] = safeSub(balances[msg.sender], tokens);
        balances[to] = safeAdd(balances[to], tokens);
        emit Transfer(msg.sender, to, tokens);
        return true;
    }
    
    function transferFrom(address from, address to, uint tokens) public returns (bool success) {
        balances[from] = safeSub(balances[from], tokens);
        allowed[from][msg.sender] = safeSub(allowed[from][msg.sender], tokens);
        balances[to] = safeAdd(balances[to], tokens);
        emit Transfer(from, to, tokens);
        return true;
    }
}
```

恭喜你！您成功开发了自己的以太坊令牌。

最后一步是部署到实际网络。

### 部署令牌

为此，我们将需要Metamask钱包。

Metamask是扩展程序，可让您直接在浏览器中运行以太坊dApp，而无需运行完整的以太坊节点。

从浏览器（Chrome，Firefox或Opera）转到[https://metamask.io/](https://metamask.io/)并添加它。

![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture6-1.png)

![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture7-1.png)

### 在MetaMask中创建一个新钱包

安装扩展程序后，单击浏览器右上角的图标即可开始创建钱包。

阅读并接受条款，然后输入一个强密码，然后单击“创建”。

![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture8-1.png)![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture9-1.png)

您将看到一个12个单词的种子短语。将种子词另存为文件或将其复制到安全的地方，然后单击“我已将其复制到安全的地方”。

您现在已成功在MetaMask中使用新的钱包地址创建了一个帐户！

您会发现当前钱包中有0 ETH。要在以太坊网络上部署合约，需要一些以太币。我们不会将合同部署到主网络，因为这只是演示。

我们会将这份合同发布到测试网络。实际上有一些以太坊区块链测试网– Ropsten，Rinkeby，Kovan…

让我们以Ropsten为例。

首先，您需要一些醚，对吗？在测试网络上，我们使用假冒的自由醚。一个人只需要从水龙头中索取一些即可。

转到：[https](https://faucet.ropsten.be/) : [//faucet.ropsten.be/](https://faucet.ropsten.be/)，粘贴您的钱包地址，然后单击“向我发送测试醚”。

![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture11-1.png)

几秒钟后，您会在钱包中看到一些ETH。

![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture12-1.png)

### 直播

现在是时候让一切变得生动起来了！

转到Remix IDE并编译合同。如果没有错误，我们已准备好进行部署。

![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture13-1.png)

对于环境，请选择“注入Web3”。它将自动检测您的metamask钱包。

![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture14-1.png)

点击部署按钮。

现在，Metamask将要求您从钱包中提取一些资金以购买此交易。

![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture15-1.png)

确认。然后回到Remix IDE，并注意终端。我们看到交易已经成功。

结果是交易哈希。在终端上单击uri，如下所示：_ropsten.etherscan.io/ &lt;transaction\_hash&gt;_

![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture16-1.png)

它将把我们导航到[etherscan.io](http://etherscan.io/) –这是以太坊区块链资源管理器，在这里您可以跟踪主网络和测试网络上正在运行的所有内容，因为所有内容当然都是在区块链上公开的。

当我们转到此uri时，我们将看到有关我们交易的详细信息。单击合同哈希以探索更多。

![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture17-1.png)

一切都是在区块链上公开的，甚至是我们的代码。Solidity开发人员没有错误的余地！

![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture18-1.png)

单击[合同选项卡](https://ropsten.etherscan.io/address/0xcaed5a2327083f55a29224f91576217ab19dfc0e#code)，您将看到我们编译的字节码

![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture19-1.png)

现在，您可以转到令牌跟踪器以查看我们的[Blockonomi令牌的](https://ropsten.etherscan.io/token/0xcaed5a2327083f55a29224f91576217ab19dfc0e)详细信息。您可以看到我们之前定义的3个可选规则。

![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture20-1.png)

现在检查您的钱包。您将看到我们为在Ropsten上部署智能合约而支付的以太币已被删除。

![](https://blockonomi-9fcd.kxcdn.com/wp-content/uploads/2020/01/Picture21.png)

### 结论

遵循这些步骤和代码示例，完成了我们的教程，您应该能够部署自己的以太坊ERC-20令牌。

玩得开心！


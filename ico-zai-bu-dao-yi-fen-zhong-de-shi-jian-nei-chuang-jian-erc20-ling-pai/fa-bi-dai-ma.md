# 【ICO】如何在15分钟内创建你的加密货币

《 如何在15分钟内创建你的加密货币》[**https://mp.weixin.qq.com/s?\_\_biz=MzI3NzQ2MjU4NA==&mid=2247483998&idx=1&sn=71602644a8f66fdb3b3142f0fae08b3c&chksm=eb64a909dc13201fb271338fab012ecea14a888bf81ce2bc7a0ab527eaa31b39e3391f1243c1&scene=21\#wechat\_redirect**](https://mp.weixin.qq.com/s?__biz=MzI3NzQ2MjU4NA==&mid=2247483998&idx=1&sn=71602644a8f66fdb3b3142f0fae08b3c&chksm=eb64a909dc13201fb271338fab012ecea14a888bf81ce2bc7a0ab527eaa31b39e3391f1243c1&scene=21#wechat_redirect)  


\*\*\*\*

**来来来，一起动手。在测试网络发个币。然后还能转到其它钱包，更让人惊喜的是：我们可以在etherscan上查到自己发的币，以及转出记录。**

**首先**打开 https://remix.ethereum.org/，我们使用 remix 网站的集成开发环境，来编写属于自己的智能合约，同时remix网站可以将合约部署到eth网络上。

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhAiaT10oOzXFbsO5yjzQtahNVjMS4wAqhfYJ8dgcibv8TvibBC4XGSfOYOg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**其次，**安装MetaMask Chrome插件。 remix IDE\(集成开发环境）需要我们安装meta mask插件。MetaMask 插件将Google Chrome 变成一个Eth 浏览器。它能让网站很方便的从blockchain上面取回数据，让用户安全地管理身份认证，和签署交易。

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhAWXu25Eh8VwEd6yz8gPmqPp2E4mTTroxW5YoAVL5QicJhwAs0S8xWNkg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

装好插件后，创建一个账户，比如eliza，就是这个样子：

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhABKJUbKMic4EKo8TCF3AtIckzccDpZTosLqCdfKyvzxdoM12GUicAymQw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**第三步，**选择 rinkeby test network。

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhAX9Q2VSfCvhAUyLicAiaBwE7JKYaQnpg2ibkNpoJoIBCaDPjVfSLsgWibIA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**第四步**，去 https://www.rinkeby.io/\#faucet 借Eth用于测试。

借用eth进行测试，是为防止耗尽所有可用资金，或着恶意的eth网络攻击，rinkeby网站会要求你绑定常见的第三方社交网络帐户。比如Twitter，Google+或Facebook帐户。 

爱莉莎使用Facebook账户，URL后面加上MetaMask钱包地址，申请3eth。

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhA6ILBBMxX30QNicGziahA53mrkntGN2A5YYYMWXgkJT5Aoq5PkWV9nGXQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

当地址栏后面的按钮，显示 funded，转账成功。可以在MetaMask钱包里看到，借来的3eth到账啦。如下图：

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhAtOPcfMSk6KibanIRxN5ZzRicu8QbQwMk7ZamicNAicvyDkwicTQgULY18CA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhAQSMYCNFv39auI69Pt5goeyibkX6P1s7nCrWZ2KlwaGGibQDKy3Q8M1QQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

3

**复制粘贴代码**

程序员常常高呼：**不必重复造车轮**。

https://github.com/ConsenSys/Tokens 有现成的代码，**拿来！用起！**

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhAYtiayYLdlJysrowvEzn0aGIXs2SIb7sJLuIfVWaPKbG42LVUlwUWRfw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

在 Tokens/contracts/eip20 里有三个文件，今天我们会copy两个。

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhAoWdderv9iaSppFDrIdibibvrE5gMo3GepEXKqffv4uKiaxr98VDKvFicaVg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**第一步**，在remix IDE（集成开发环境）里新建文件，文件以你想创建的Token命名。比如爱莉莎想发eliza币，那就 The Eliza Token吧！

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhA7UkyOWQ5j5BCUOPnOIxfVAOdG48xa6JP7egjze8s3h87v1cXSxYH6w/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**接下来**，将Tokens/EIP20.so！文件内容，复制到 TheElizaToken.so!中。

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhAl62ibjTaiaeuvNIzreCjqxoiay5PmE1CD7xO1tibwReicU5LuZDkY3guYlA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**第三步**，将代码中，contract 名字，更改为： TheElizaToken。

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhALibzgKBatvuktOXNFC1N8l4fpocYlPbiayhOwJzI5QH2cK3vSOOhWGRg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**第四步**，将Function EIP20 更改为 function TheElizaToken

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhA7lsIn5nQNQVYmicDh1ZLZSWiaI414lnibbshGNaibwMibg09dav7Ng3yN3w/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**第五步，**复制 EIP20Interface.so! 到remix IDE中。

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhAsHMf5ZoferdbNicrLvHs3hxhUNlw3VC9yaJk67YGtBPpkxyhOgGTmxQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhANZ9g0pY8Piap8w7aRiaFQYtIyPPvtZDDfFPBJ7cN2y5yoe3qovia4vkeQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhA59msdReJ73wg7iaPmOJ0DjH0AYsE6mnVcRSia46CiaSViavs38ya0KqxRQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

4

**发币**

**第一步**，在remix IDE右边，点击“Run”，选择 “TheElizaToken”。

输入：初始发行量，Token名称，decimal Unit（此处设为0），币符号。

比如：21000000，“TheElizaToken”，0，“TET”。

2100万，是向比特币致敬。

点击“Create”，MetaMask会弹出提示框，选“Submit”。

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhAVw10vtQDojibZlIjibeShKmZejuL0g8NXIFgXj7bY1nHqlRia0yaibZBfQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

等待一会儿，会如下图显示，新的合约地址，已经创建。

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhAl79MwyIl4yODgV8P7MFX1kic8QxibpXxS8MibAZY2Sl7BWPibEUs6nqttQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**接着**，验证发币量。

这里有个**坑**，**地址要加“”，不加“”，会出现 balance 0。**

看到这个0，爱莉莎心想，我的币呢？被外星人劫持了？

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhAicMFWrPCJ6BDibwmKo2q6aYm1IMjsTbn6RjN8olYHSbIjbPfNqpvaTmQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

加入“”，输入地址，显示正确。发币量：2100万。

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhAb3Mgo58wcOToGcrqYGKxRkyNS2ibN6jUFs9DMvM9hiaTfzhte8FgHLUg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

5

**转币**

**首先**，在右侧下方的 transfer 栏位，填入转入的测试地址及数量。

格式：“地址”，数量。

测试数量填10000。

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhAVnmjoN1elB4ggXk6bQ9m0MPtWBkMfU9T6eVlTBO1loCwR1nHvrqiaYQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

等待一会儿，显示： 0 pending transactions。传输成功。

查询“balanceOf”，显示20990000。 成功转出。

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhAnriaYwAibs1k4OoliaibhNXvX1KfWL2YmjerTGLS62XtRxrM6Kjr24xK5A/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

6

**EtherScan 查询**

打开 https://etherscan.io/token-search，输入合约地址0x20886a1B9628f16cDA6D74aba99b09963cE516fe，

可以看到——爱莉莎的 the eliza token，以及传输记录。

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhAoaewOaXwNO5uiasBHFJ5DdYbalYcnKK2HbkmiaNmyLtI4akN38oZZk6Q/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

合约信息：

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhAibEibM2YK3TicYkv1AjKz62VL38F7OPDFJs0R7V2FyiaqCKkPNpBJFTxNQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

传输记录：

![](https://mmbiz.qpic.cn/mmbiz_png/O8Vz4KCqibjCYx9tOibevdTVUDicWqecDhAPmgdZc8JicQicy7bl1yr9ljk7ylG8iah70LDWedblmDCfg5W3gIopl6tg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**发币，转币，传输记录查询成功！Cheers！**

BFM\_Token\_ERC20.sol

```java
/*
Implements EIP20 token standard: https://github.com/ethereum/EIPs/blob/master/EIPS/eip-20.md
.*/


pragma solidity ^0.4.21;

import "./EIP20Interface.sol";


contract BFM_Token_ERC20 is EIP20Interface {

    uint256 constant private MAX_UINT256 = 2**256 - 1;
    mapping (address => uint256) public balances;
    mapping (address => mapping (address => uint256)) public allowed;
    /*
    NOTE:
    The following variables are OPTIONAL vanities. One does not have to include them.
    They allow one to customise the token contract & in no way influences the core functionality.
    Some wallets/interfaces might not even bother to look at this information.
    */
    string public name;                   //fancy name: eg Simon Bucks
    uint8 public decimals;                //How many decimals to show.
    string public symbol;                 //An identifier: eg SBX

    function BFM_Token_ERC20(
        uint256 _initialAmount,
        string _tokenName,
        uint8 _decimalUnits,
        string _tokenSymbol
    ) public {
        balances[msg.sender] = _initialAmount;               // Give the creator all initial tokens
        totalSupply = _initialAmount;                        // Update total supply
        name = _tokenName;                                   // Set the name for display purposes
        decimals = _decimalUnits;                            // Amount of decimals for display purposes
        symbol = _tokenSymbol;                               // Set the symbol for display purposes
    }

    function transfer(address _to, uint256 _value) public returns (bool success) {
        require(balances[msg.sender] >= _value);
        balances[msg.sender] -= _value;
        balances[_to] += _value;
        emit Transfer(msg.sender, _to, _value); //solhint-disable-line indent, no-unused-vars
        return true;
    }

    function transferFrom(address _from, address _to, uint256 _value) public returns (bool success) {
        uint256 allowance = allowed[_from][msg.sender];
        require(balances[_from] >= _value && allowance >= _value);
        balances[_to] += _value;
        balances[_from] -= _value;
        if (allowance < MAX_UINT256) {
            allowed[_from][msg.sender] -= _value;
        }
        emit Transfer(_from, _to, _value); //solhint-disable-line indent, no-unused-vars
        return true;
    }

    function balanceOf(address _owner) public view returns (uint256 balance) {
        return balances[_owner];
    }

    function approve(address _spender, uint256 _value) public returns (bool success) {
        allowed[msg.sender][_spender] = _value;
        emit Approval(msg.sender, _spender, _value); //solhint-disable-line indent, no-unused-vars
        return true;
    }

    function allowance(address _owner, address _spender) public view returns (uint256 remaining) {
        return allowed[_owner][_spender];
    }
}
```


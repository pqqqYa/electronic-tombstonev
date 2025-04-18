> 以以太坊账户为例

## 账户分类

以太坊有两种账户类型：

- Externally-owned account (EOA外部拥有的账户） – 由拥有私钥的任何人控制
- Contract account（Contract account 合约账户） – 部署到网络的智能合约，由代码控制

这两种账户类型都能够：

- 接收、持有和发送 ETH 和代币
- 与已部署的智能合约交互


**外部所有账户**

- 创建帐户无需任何费用
- 可以发起交易
- 外部账户之间的交易只能是ETH/token转账
- 由一对加密密钥组成：控制账户活动的公钥和私钥

**合约账户**

- 创建合约账户是有成本的，因为使用的是网络存储
- 只能发送交易以响应接收交易
- 从外部账户到合约账户的交易可以触发代码，这些代码可以执行许多不同的操作，例如转移代币甚至创建新合约（智能合约）
- 合约账户没有私钥，由智能合约代码的逻辑控制

## 账户组成

Ethereum 账户有四个字段：

- `nonce` 一个计数器，指示从外部拥有的账户发送的交易数量或合同账户创建的合同数量。每个账户只能执行一个具有给定 nonce 的交易，以防止重放攻击，即重复广播和重新执行已签名的交易。
- `balance` 此地址拥有的 wei 数量。Wei 是 ETH 的面额，每个 ETH 有 1e+18 wei。
- `codeHash` 此哈希是指以太坊虚拟机（EVM）上的合约账户代码。合约账户具有编程的代码片段，可以执行不同的操作。如果账户收到消息调用，则执行此 EVM 代码。与其他账户字段不同，它无法更改。所有此类代码片段都包含在状态数据库中的相应哈希值下，以供以后检索。此哈希值称为 codeHash。对于外部拥有的账户，codeHash 字段是空字符串的哈希值。
- `storageRoot` 有时称为存储哈希。Merkle Patricia trie（默克尔树）的根节点的 256 位哈希值，用于对帐户的存储内容（256 位整数值之间的映射）进行编码，作为从 256 位整数键的 Keccak 256 位哈希到 RLP 编码的 256 位整数值的映射编码到树中。此 trie 对此账户的存储内容的哈希进行编码，默认情况下为空。

![](attachment/account4part.png)

## 外部拥有的账户和密钥对

EOA账户由一对加密密钥组成：public公钥和 private私钥。用于证明交易实际上是由发件人签署的，并防止伪造。私钥是用来签署交易的密钥，因此授予你对与你的账户关联的资金的保管权。用户从来没有真正持有加密货币，用户仅仅是持有私钥，资金始终存储在以太坊的账本上。

这种模式可以防止恶意行为者广播虚假交易，因为用户始终可以验证交易的发送者。

如果 Alice 想从自己的账户向 Bob 的账户发送以太币，Alice 需要创建一个交易请求并将其发送到网络进行验证。以太坊对公钥加密的使用确保 Alice 可以证明她最初发起了交易请求。如果没有加密机制，恶意对手 Eve 可以简单地公开广播一个请求，该请求类似于“从 Alice 的账户向 Eve 的账户发送 5 个 ETH”，并且没有人能够验证它不是来自 Alice。

## 帐户创建

创建帐户时，大多数的库都会生成一个随机的私钥。私钥由 64 个十六进制字符组成，可以使用密码进行加密。私钥只能由账户所有者访问。私钥用于“签署”交易和数据，以便可以用密码学证明持有者批准了特定私钥的某些操作。

公钥是使用[椭圆曲线数字签名算法](https://wikipedia.org/wiki/Elliptic_Curve_Digital_Signature_Algorithm) 从私钥生成的。用户可以使用私钥派生新的公钥，但不能从公钥派生私钥。公钥用作 Ethereum 地址的基础，它对公众可见并用作唯一标识符

> You need a private key to sign messages and transactions which output a signature.
> message + key pair = signature
> signature + message =  address or public key


所有用户都需要一个私钥通过[Clef](https://geth.ethereum.org/docs/tools/clef/introduction)（一种在安全的本地环境中对交易和数据进行签名的工具）来对输出签名的消息和交易进行签名。然后其他人可以获取签名来派生您的公钥，从而证明消息的作者。

public address公共地址可以通过堆公钥进行Keccak-256 哈希算法运算，取最后 20 个byte并在开头添加 `0x`获得。这意味着EOA （外部拥有的帐户）有一个 42 个字符的地址（20 字节段，即 40 个十六进制字符加上 `0x` 前缀）。

## 合约账户

合约账户也有一个 42 个字符的十六进制地址

合约地址通常在将合约部署到以太坊区块链时给出。该地址来自创建者的地址和从该地址发送的交易数量（“nonce”）。

## Validator keys 验证程序密钥

当以太坊从工作量证明切换到基于权益证明的共识时引入的例外一种密钥。“BLS”密钥，用于识别验证者。这些密钥可以有效地聚合，以减少网络达成共识所需的带宽。如果没有这种密钥聚合，验证者的最低赌注会高得多。


## 钱包
# Sui术语

查找下面定义的 Sui 中使用的术语。在可能的情况下，我们链接到一个规范的定义，并专注于 Sui 对该术语的使用。

## 累加器
累加器确保交易被法定人数的验证者接收，收集法定人数的投票，将证书提交给验证人，并回复客户端。累加器使交易能够被认证。Sui 提供了一个网关服务，该服务可以充当累加器的角色，并从 Sui 中的验证者那里收集交易投票，从而节省最终用户的带宽。

## 因果顺序

[因果顺序](https://www.scattered-thoughts.net/writing/causal-ordering/)是事务和它们产生的对象之间的关系的表示，被布置为依赖关系。验证者无法执行依赖于由尚未完成的先前事务创建的对象的事务。Sui 没有使用全序，而是使用因果序（偏序）。

有关更多信息，请参阅[因果顺序和总顺序](https://docs.sui-cn.xyz/learn/different_from_sui_move_and_core_move)

## 证书

证书是证明交易已被批准或认证的机制。验证者对交易进行投票，聚合器将这些选票中的多数选票收集到证书中，并将其广播给所有 Sui 验证者，从而确保最终确定性。

## 模棱两可

区块链中的模棱两可是不诚实行为者为同一消息提供相互冲突的信息的恶意行为，例如不一致或重复的投票。

## 纪元(epoch)

Sui 网络的操作在时间上被划分为不重叠的、固定持续时间的*时期*。在特定时期，参与网络的验证者集合是固定的。

有关更多信息，请参阅[时期](https://docs.sui-cn.xyz/build/about_validator)

## 最终一致性

[最终一致性](https://en.wikipedia.org/wiki/Eventual_consistency)是 Sui 采用的共识模型；如果一个诚实的验证者验证了交易，那么所有其他诚实的验证者最终也会如此。

## 因果历史

因果历史是Sui中的一个对象与其直接前辈和后继者之间的关系。这个历史对于 Sui 用来处理交易的因果顺序是必不可少的。相比之下，其他区块链会为每笔交易读取其世界的整个状态，从而引入延迟。

## 终局性(Finality)
[终局性](https://en.wikipedia.org/wiki/Eventual_consistency)是交易不会被撤销的保证。此阶段被视为交易所或其他区块链交易的关闭。

## Gas

[Gas](https://ethereum.org/en/developers/docs/gas/)是指在 Sui 网络上执行操作所需的计算量。在 Sui 中，gas 使用网络的本地货币 SUI 支付。以 SUI 为单位执行交易的成本称为交易费用。

## 创世纪

Genesis 是创建帐户和gas对象的初始行为。Sui 提供了一个`genesis`命令，允许用户创建和检查设置网络以进行操作的创世对象。

## 网关服务

Sui 提供网关服务，使第三方（例如应用程序/游戏开发人员）能够代表用户路由交易。因为 Sui 从不要求交换私钥，所以用户可以将交易提交的带宽使用（例如，当从移动设备操作时）卸载到不受信任的服务器上。

## 多重写对象

多作者对象是由多个帐户拥有的对象。影响多写者对象的事务需要在 Sui 中达成共识。这与只影响单写者对象的那些形成对比，后者只需要确认所有者的帐户内容。

## 对象

Sui 中的基本存储单位是对象。与许多其他区块链的存储以账户为中心并且每个账户都包含一个键值存储相比，Sui 的存储以对象为中心。Sui 对象有以下主要状态：

- 不可变- 无法修改对象。
- 可变的 - 可以更改对象。
- 
此外，可变对象分为以下几类：

- 拥有- 对象只能由其所有者修改。
- 共享- 任何人都可以修改对象。
不可变对象不需要这种区别，因为它们没有所有者。

有关详细信息，请参阅[管理对象](https://docs.sui-cn.xyz/build/manage_objects)

## 权益证明

POS (Proof of Stake)  是一种区块链共识机制，其中验证者或验证者的投票权重与网络本地货币的保税金额（称为他们在网络中的股份）成正比。这通过迫使不良行为者首先在区块链中获得大量股份来减轻[女巫攻击](https://en.wikipedia.org/wiki/Sybil_attack)

## 智能合约

[智能合约](https://en.wikipedia.org/wiki/Smart_contract)是基于在区块链中进行交易的协议的协议。在 Sui 中，智能合约是用[Move](https://github.com/MystenLabs/awesome-move)编程语言编写的。

## Sui / SUI

Sui 是指 Sui 区块链、SUI 币和[Sui 开源项目](https://github.com/MystenLabs/sui/)的整体。

## 总订单（Total Order）

[总订单](https://en.wikipedia.org/wiki/Total_order)是指传统区块链在给定时间内处理的所有交易历史的有序呈现。这是由许多区块链系统维护的，作为处理交易的唯一方式。相反，Sui 尽可能且安全地使用因果（部分）顺序。

有关更多信息，请参阅[因果顺序和总顺序](https://docs.sui-cn.xyz/learn/different_from_sui_move_and_core_move)

## 转移(Transfer)

转移是通过 Sui 中的命令将Token的所有者地址转换为新的。这是通过 Sui Wallet命令行界面完成的。它是钱包中可用的许多命令中最常见的一种。

有关详细信息，请参阅[传输对象](https://docs.sui.io/build/wallet#transferring-objects)。

## 验证者(Validator)

Sui中的验证者扮演着一个被动的角色，类似于其他区块链中验证者和矿工之类的更积极的角色。在Sui中，验证者并不持续参与共识协议，而是只有在收到交易或证书时才会被召集起来采取行动。

有关更多信息，请参阅[验证者](https://docs.sui-cn.xyz/build/about_validator)


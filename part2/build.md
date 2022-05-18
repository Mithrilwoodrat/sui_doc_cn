---
title: 构建 Sui
---

现在你已经[了解了Sui](./learn/index.md)，是时候开始构建了。

## 工作流程

以下是我们推荐的与Sui互动的工作流程。

1. [安装](.../build/install.md)所有的 *必要的工具*。
1. [快速启动](.../build/move.md) Move *智能合约*。
   1. [编写](./build/move.md#writing-a-package) 一个软件包。
   1. [测试](../build/move.md#testing-a-package) 一个软件包。
   1. [调试](../build/move.md#debugging-a-package) 一个软件包。
   1. [发布](../build/move.md#publishing-a-package) 一个软件包。
1. [创建](.../build/wallet.md#genesis)和[启动](.../build/wallet.md#starting-the-network)一个*本地Sui网络。
1. [开始](./build/json-rpc.md#start-local-rpc-server) 一个*本地的JSON-RPC网关服务器*。
1. 1. [连接](.../build/wallet.md#rpc-gateway)，用*Sui Wallet*连接到Sui网络网关服务。
1. 构建dApps。
   1. [使用](./build/json-rpc.md) *Sui RPC服务器和JSON-RPC API*与本地Sui网络互动。
   1. [运用](./build/sui-json.md) *SuiJSON格式*以使JSON输入与Move call参数更加一致。


##相关概念

如果你还没有，请熟悉这些关键的Sui概念。

* [验证器](.../learn/architecture/validators.md) - Sui网络是由一组独立的验证器操作的，每个验证器都在单独的机器上运行自己的Sui软件实例（或由同一实体操作的机器分片集群）。
* [对象](.../build/objects.md) - Sui有可编程的对象，由Move包（又称智能合约）创建和管理。Move包本身也是对象。因此，Sui的对象可以被划分为两类可变的数据值和不可变的包。
* [交易](.../build/transactions.md) - 所有对Sui分类账的更新都是通过交易进行的。本节描述了Sui所支持的交易类型，并解释了它们的执行是如何改变分类帐的。

在我们的[FAQ](.../contribute/faq.md)中找到关于我们[路线图](https://github.com/MystenLabs/sui/blob/main/ROADMAP.md)和更多常见问题的答案。

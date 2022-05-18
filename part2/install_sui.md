---
title: 安装Sui
---

Sui是用Rust编写的，我们使用Cargo来构建和管理
依赖关系。 作为先决条件，你需要[安装
Cargo](https://doc.rust-lang.org/cargo/getting-started/installation.html)
1.60.0或更高版本，以便在你的机器上构建和安装Sui。

##二进制文件

要用Sui开发，你需要Sui的二进制文件。安装完`cargo'后，运行。

``shell
$ cargo install --locked --git https://github.com/MystenLabs/sui.git --branch "devnet" sui
```

这将把这些二进制文件放在你的`PATH`（例如在`~/.cargo/bin`下），它们提供这些命令行接口（CLI）。
* [`sui-move`](move.md) - 建立和测试Move软件包
* [`wallet`](wallet.md) - 运行一个通过wallet CLI访问的本地Sui网络和网关服务。wallet CLI管理密钥对以签署/发送交易。
* `rpc-server`](json-rpc.md) - 运行一个通过RPC接口访问的本地Sui网络和网关服务。

用以下方式确认安装。

```
$ echo $PATH
```

并确保出现`.cargo/bin`目录。

## 集成开发环境
对于Move的开发，我们推荐使用[Visual Studio Code (vscode)](https://code.visualstudio.com/)IDE，并安装Move Analyzer语言服务器插件。

``shell
$ cargo install --git https://github.com/move-language/move move-analyzer
```

然后按照Visual Studio Marketplace的说明来安装[Move Analyzer扩展](https://marketplace.visualstudio.com/items?itemName=move.move-analyzer)。(语言服务器的`cargo install`命令在那里被破坏了；因此，我们在上面包括正确的命令)。

请参阅[Awesome Move](https://github.com/MystenLabs/awesome-move)文档中的更多[IDE选项](https://github.com/MystenLabs/awesome-move#ides)。

## 源代码

如果你需要下载和了解Sui的源代码，请克隆Sui的仓库。

``shell
$ git clone https://github.com/MystenLabs/sui.git
```

你可以通过查看以下主要目录来开始探索Sui的源代码。
* [sui](https://github.com/MystenLabs/sui/tree/main/sui) - Sui的二进制文件（`wallet', `sui-move', 和其他）。
* [sui_programmability](https://github.com/MystenLabs/sui/tree/main/sui_programmability) - Sui的Move语言集成，也包括游戏和其他Move代码实例，用于测试和重复使用
* [sui_core](https://github.com/MystenLabs/sui/tree/main/sui_core) - 认证服务器和Sui网关
* [sui-types](https://github.com/MystenLabs/sui/tree/main/crates/sui-types) - 币、gas和其他对象类型
* [explorer](https://github.com/MystenLabs/sui/tree/main/explorer) - Sui 区块链网络浏览器
* [sui-network](https://github.com/MystenLabs/sui/tree/main/crates/sui-network) - 网络接口

可以看到Rust [Crates](https://doc.rust-lang.org/rust-by-example/crates.html)的使用案例:
* https://mystenlabs.github.io/sui/ - Sui区块链
* https://mystenlabs.github.io/narwhal/ - Narwhal和Tusk共识引擎
* https://mystenlabs.github.io/mysten-infra/ - Mysten实验室的基础设施

要对Sui代码进行更新，请[send pull requests](.../contribute/index.md#send-pull-requests)。

## 接下来的步骤

通过以下方式继续你的旅程。

* [Smart Contracts with Move](write_contract_by_move.md)
* [钱包快速入门](create_sui_wallet.md)
* [RPC服务器API](use_sui_rpc_server.md)
* [端到端教程](./explore/tutorials.md)

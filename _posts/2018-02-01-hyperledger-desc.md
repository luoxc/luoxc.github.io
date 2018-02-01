---
layout: post
title: HyperLedger 简介
date: 2018-02-01 19:34:00 +0300
description: [HyperLedger](https://www.hyperledger.org/) 是区块链技术中的比较流行的开源项目。
img_url: http://himg2.huanqiu.com/attachment2010/2015/0514/20150514095718228.jpg
tags: [Java]
---

[HyperLedger](https://www.hyperledger.org/) 是区块链技术中的比较流行的开源项目。
## 项目简介

Hyperledger是由Linux基金会主导推广的区块链开源项目。在Hyperledger
 
Fabric的基础上又衍生出了其他一些相关的项目。HyperLedger项目汇集了金融、银行、物联网、供应链、制造等各界开发人员的心血。目的是为了打造一个跨领域的区块链应用。随着网络技术的不断发展，区块链也从比特币中脱离开始在其他领域发挥重要作用。在区块链中，基于P2P网络的分布式的记账系统通过一定的机制获得共识，并且在节点上执行“智能合约”。作为区块链最重要的应用之一。市场已经将Hyperledger当作开发未来金融市场市场所需要的交易网络、代币和去中心化的智能社区的重要手段。得益于它的内在特性，Hyperledger将大大减少交易的成本和复杂度。回顾近年来信息技术的发展，开源社区激发出的创造力让区块链技术慢慢在主流商业应用上崭露头角。目前已有100多家企业和众多开发人员投入到打造一个透明、公开、去中心化的项目中来，也正是Hyerldger项目的意义所在。

## 重要数据

* 2015 年 12 月，Linux 基金 会牵头，联合 30 家初始成员（包括 IBM、Accenture、Intel、J.P.Morgan、R3、DAH、DTCC、FUJITSU、HITACHI、SWIFT、Cisco 等），共同 宣告 了 Hyperledger 项目的成立。
* 超过 80 家企业和机构（大部分均为各自行业的领导者）宣布加入 Hyperledger 项目，目前包括 13 家来自中国的公司，包括艾亿新融旗下的艾亿数融科技公司（2016.05.19）、Onchain（2016.06.22）、比邻共赢（Belink）信息技术有限公司（2016.06.22）、BitSE（2016.06.22）、布比（2016.07.27）、三一重工（2016.08.30）等。

## Fabric项目介绍

### Fabric

2016年3月，在Linux协会的推动下，超级账本项目将正式把Blockstream，Digital Asset Holdings（数字资产控股公司）以及科技巨头IBM这三个项目成员贡献的代码合并为一个新的代码库，形成一个新的企业级区块链的基础。这个代码集合被称为Hyperledger Fabric。

Fabric 致力在一个共识网络内，对指定资产资产的信息进行互换、维护和调阅。Fabric的架构支持模块的插拔，例如：共识模块、会员模块等。它将进一步推广“智能和约”在容器技术中的应用，从而实现各种商业应用场景。

Fabric目前主要包括以下三部分：
* fabric (Gerrit)
* fabric-api (Gerrit)
* fabric-chaintool

你可以在Github上找到fabric和fabric-api的对应镜像。

#### 主要功能：
- 定位许可制区块链;
- 由Go、JAVA语言实现运行任意智能合约;
- 用户定义的智能合约封装在Docker容器中执行;
- 系统智能合约与节点运行相同的进程;
- 共识算法是可插拔的，目前支持使用PBFT;
- 通过证书颁发机构（CA）提供TLS证书，登录证书和交易证书;
- 使用KV持久化数据存储，支持RocksDB、LevelDB;
- 支持预定义和定制事件的事件框架;
- 与Fabric交互的客户端Node.js 、Python SDK;
- 支持基本的REST API和CLI

#### 技术架构：
Fabric的构架由成员服务（Membership）、区块链服务（Blockchain）和链码服务（Chaincode）三个主要类别构成。这些类别仅仅是Fabric的逻辑结构，并不是在物理上将组件划分成不同的进程、地址空间或者虚拟机。

### 子项目介绍

除了Fabric之外，Hyperledger也衍生出其他几个有潜力的项目。下面将一一介绍。

#### Blockchain Explorer
是为了便于Hyperledger应用浏览/查询区块信息、交易相关信息、网络信息（名称、状态，关联节点）、智能合约信息（浏览、调用、部署、查询）和其他相关信息而设计的Web应用。它由IBM公司的Dan Middletonmiais 和Pardha Vishnumolakala提出。 

#### Cello
是一个用于部署区块链服务BSAS（Blockchain-as-a-Service）的工具，它可以帮助用户降低创建、管理和删除区块信息的复杂度。Cello的意义在于，它让区块链的定制化成为了可能，也就是说Cello可以在多种环境下：裸机、虚拟机和其他容器之上，提供有自治的多租户服务。

主要负责人：IBM研发团队的 Baohua Yang 和Haitao Yue 
主要合作方：Soramitsu, Huawei and Intel.

#### Iroha
Hyperledger Iroha 项目由Makoto Takemiya (Soramitsu), Toshiya Cho (Hitachi), Takahiro Inaba (NTT Data), and Mark Smargon (Colu)几个人提出。目前正处于孵化阶段。Iroha项目的目的在于将分布式账本技术便捷的应用于现有的基础项目上。

主要特点：
- 实施简单
- 领域驱动C++设计（domain-driven C++ design）
- 聚焦移动终端应用的开发
- 采用新的BFT共识算法：Sumeragi

#### Sawtooth Lake
Sawtooth Lake是Intel主导的区块链应用组件，目的在于实现区块链技术的多用途和可扩展性。从物联网到金融，人们已经尝试将分布式账本技术应用在多个领域。Sawtooth Lake架构将兼顾各类不同的需求。Sawtooth Lake 支持有许可和无需许可的不是方式，并引入了新的共识算法：Proof of Elapsed Time (PoET)。PoET可以减少肌群达到共识所消耗的资源。交易逻辑的管理由Transaction Families负责，从共识管理层剥离。这样将大大减少交易逻辑的约束。
---
sip: 4
title: Add VLX/USDT Swapp Pool 新增VLX/USDT交易对
status: Proposed
author: Fudezl (@Fudezl)
created: 2020-11-28
---

<!--You can leave these HTML comments in your merged SIP and delete the visible duplicate text guides, they will not appear and may be helpful to refer to if you edit it again. This is the suggested template for new SIPs. Note that a SIP number will be assigned by an editor. When opening a pull request to submit your SIP, please use an abbreviated title in the filename, `sip-draft_title_abbrev.md`. The title should be 44 characters or less.-->

## 摘要 Summary

<!--"If you can't explain it simply, you don't understand it well enough." Simply describe the outcome the proposed changes intends to achieve. This should be non-technical and accessible to a casual community member.-->

-   新增 VLX/USDT 交易对提案；
-   对 VLX/USDT 矿池进行 20%比例 SYX 代币奖励；

## 简述 Abstract

<!--A short (~200 word) description of the proposed change, the abstract should clearly describe the proposed change. This is what *will* be done if the SIP is implemented, not *why* it should be done or *how* it will be done. If the SIP proposes deploying a new contract, write, "we propose to deploy a new contract that will do x".-->

目前 Symblox 协议上 VLX 总交易额突破 11 亿枚（转入转出），因为 Symblox 协议上没有 VLX/USDT 对，导致社区用户需在其余交易所购买/转入 Symblox 协议再进行流动性挖矿，这样的体验，一较为麻烦；其次一些中心化交易所流动性不强，不易成交；三是给别的交易所导流。因此，Symblox 社区应该将这部分流量转变成自己的，我们有流量，对 VLX 及 SYX 将形成绝对优势定价权。

为鼓励 VLX 原始持有者对 VLX/USDT 做出的流动性贡献，社区将对该交易对矿池进行一定比例的 SYX 代币奖励。

## 目的 Motivation

<!--This is the problem statement. This is the *why* of the SIP. It should clearly explain *why* the current state of the protocol is inadequate. It is critical that you explain *why* the change is needed, if the SIP proposes changing how something is calculated, you must address *why* the current calculation is innaccurate or wrong. This is not the place to describe how the SIP will address the issue!-->

将 Symblox 社区 VLX 的被动流量转变为主动流量，Symblox 社区有自主流量，对 VLX 及 SYX 将形成绝对优势定价权。

## 详细说明 Specification

<!--The specification should describe the syntax and semantics of any new feature, there are five sections
1. Overview
2. Rationale
3. Technical Specification
4. Test Cases
5. Configurable Values
-->

### 简介 Overview

<!--This is a high level overview of *how* the SIP will solve the problem. The overview should clearly describe how the new feature will be implemented.-->

新增资产交易对

-   VLX/USDT

矿池奖励分配比例调整

- 将VLX种子矿池比例调整为1%；

- 将VLX/SYX矿池比例调整为49%；

- 将VLX/USDT矿池奖励分配比例调整为20%；


-   将 VLX 种子矿池比例调整为 1%；
-   将 VLX/SYX 矿池比例调整为 49%；
-   将 VLX/USDT 矿池奖励分配比例调整为 20%；

| 矿池/交易对名称 | 调整前 | 调整后 |
| --------------- | :----: | :----: |
| VLX 种子池      |   5%   |   1%   |
| VLX/SYX         |  65%   |  49%   |
| USDT/SYX        |  30%   |  30%   |
| VLX/USDT        |   -    |  20%   |

### 原由 Rationale

<!--This is where you explain the reasoning behind how you propose to solve the problem. Why did you propose to implement the change in this way, what were the considerations and trade-offs. The rationale fleshes out what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.-->

增加资产交易对的同时，也将增加流动性。其次，当 VLX 与 USDT 之间有价差（套利空间）时，社区用户需去到相应的中心化交易所去交易，因其它交易所流动性不强，在交易过程中不易成交，如果所有交易在 Symblox 协议上完成，带动交易量的同时还能推动价格。

另外，以太坊上 DeFi 项目 gas 费用过高导致一些小资金用户难参与其中，Symblox 在不断增加资产交易对之余也将带来流动性，而 Symblox 刚好可以去承接这部分用户，Symblox 协议上支持的资产越多，参与进来的社区也将越多，Symblox 协议上流动性起来了，对于 VLX 与 SYX 将在价格上形成主导权。

VELAS 跨链属于全新推出的功能，具有一定的风险性。因此，建议用户在投入资产数量时应做好风险评估，不宜超过自己可承担损失的数量。

### 技术实现说明 Technical Specification

<!--The technical specification should outline the public API of the changes proposed. That is, changes to any of the interfaces Synthetix currently exposes or the creations of new ones.-->

### 测试方案 Test Cases

<!--Test cases for an implementation are mandatory for SIPs but can be included with the implementation..-->

### 实施方法 Implementation

<!--Please list all values configurable under this implementation.-->

Overview
提案分为以下3步 

There are 3 steps for the proposal.

- 首先，创建 VLX 和 USDT 的 Balancer Pool (BPT)，并设置 BPT 相应的比例为 90:10。根据当前 VLX 价格为 0.025 USDT, 则需存入 90,000 VLX 和 250 USDT 作为初始流动性。

- Firstly, we create a new Balancer pool for VLX and USDT, and set the weights of SYX and USDT to be 90:10 respectively. Based on the current market price of VLX is 1 VLX = 0.025 USDT, we deposit 90,000 VLX and 250 USDT to see the pool;

- 第二步，将 USDT/VLX 的交易池添加到 RewardManager，并设置该矿池的奖励点数为 20;

- Secondly, we need to add the new USDT/VLX pool to the RewardManager, and set the reward allocation points to 20;

- 第三步，设置 USDT/SYX 交易池的奖励点数为 30。

- Thirdly, set the reward allocation points for USDT/SYX pool to be 30.

- 最后，设置 VLX/SYX 交易池的奖励点数为 49。

- Lastly, we set the reward allocation points for VLX/SYX swap pool to be 49.

| Pool Name 矿池名称 | Before 修改前 | After 修改后 | Previous Allocation 修改前奖励数 | After Allocation 修改后奖励数 |
|---|---:|---:|---:|
| VLX Seed 种子池 | 5% | 1% | 1 | 1 |
| VLX/SYX 交易池 | 65% | 49% | 13 | 49 |
| USDT/SYX 交易池 | 30% | 30% | 6 | 30 |
| USDT/VLLX 交易池 | - | 20% | - | 20 |


## 版权 Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

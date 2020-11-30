---
sip: 4
title: 新增VLX/USDT交易对提案
status: Proposed
author:  Fudezl (@Fudezl)

created: 2020-11-28
---

<!--You can leave these HTML comments in your merged SIP and delete the visible duplicate text guides, they will not appear and may be helpful to refer to if you edit it again. This is the suggested template for new SIPs. Note that a SIP number will be assigned by an editor. When opening a pull request to submit your SIP, please use an abbreviated title in the filename, `sip-draft_title_abbrev.md`. The title should be 44 characters or less.-->

## 摘要 Summary

<!--"If you can't explain it simply, you don't understand it well enough." Simply describe the outcome the proposed changes intends to achieve. This should be non-technical and accessible to a casual community member.-->

- 新增VLX/USDT交易对提案；
- 对VLX/USDT矿池进行20%比例SYX代币奖励；

## 简述 Abstract

<!--A short (~200 word) description of the proposed change, the abstract should clearly describe the proposed change. This is what *will* be done if the SIP is implemented, not *why* it should be done or *how* it will be done. If the SIP proposes deploying a new contract, write, "we propose to deploy a new contract that will do x".-->

目前Symblox 协议上VLX总交易额突破11亿枚（转入转出），因为Symblox 协议上没有VLX/USDT对，导致社区用户需在其余交易所购买/转入Symblox协议再进行流动性挖矿，这样的体验，一较为麻烦；其次一些中心化交易所流动性不强，不易成交；三是给别的交易所导流。因此，Symblox社区应该将这部分流量转变成自己的，我们有流量，对VLX及SYX将形成绝对优势定价权。
 
为鼓励VLX原始持有者对VLX/USDT做出的流动性贡献，社区将对该交易对矿池进行一定比例的SYX代币奖励。

## 目的 Motivation

<!--This is the problem statement. This is the *why* of the SIP. It should clearly explain *why* the current state of the protocol is inadequate. It is critical that you explain *why* the change is needed, if the SIP proposes changing how something is calculated, you must address *why* the current calculation is innaccurate or wrong. This is not the place to describe how the SIP will address the issue!-->

将Symblox社区VLX的被动流量转变为主动流量，Symblox社区有自主流量，对VLX及SYX将形成绝对优势定价权。

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
- VLX/USDT

矿池奖励分配比例调整
- 将VLX种子矿池比例调整为1%；
- 将VLX/SYX矿池比例调整为49%；
- 将VLX/USDT矿池奖励分配比例调整为20%；

|  矿池/交易对名称  | 调整前  | 调整后 |
|  ----  | :----:  | :----: |
| VLX 种子池 | 5% | 1% |
| VLX/SYX | 65% | 49% |
| USDT/SYX | 30% | 30% |
| VLX/USDT | - | 20% |

### 原由 Rationale

<!--This is where you explain the reasoning behind how you propose to solve the problem. Why did you propose to implement the change in this way, what were the considerations and trade-offs. The rationale fleshes out what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.-->

增加资产交易对的同时，也将增加流动性。其次，当VLX与USDT之间有价差（套利空间）时，社区用户需去到相应的中心化交易所去交易，因其它交易所流动性不强，在交易过程中不易成交，如果所有交易在Symblox协议上完成，带动交易量的同时还能推动价格。
 
另外，以太坊上DeFi项目gas费用过高导致一些小资金用户难参与其中，Symblox在不断增加资产交易对之余也将带来流动性，而Symblox刚好可以去承接这部分用户，Symblox协议上支持的资产越多，参与进来的社区也将越多，Symblox协议上流动性起来了，对于VLX与SYX将在价格上形成主导权。
 
VELAS 跨链属于全新推出的功能，具有一定的风险性。因此，建议用户在投入资产数量时应做好风险评估，不宜超过自己可承担损失的数量。

### 技术实现说明 Technical Specification

<!--The technical specification should outline the public API of the changes proposed. That is, changes to any of the interfaces Synthetix currently exposes or the creations of new ones.-->



### 测试方案 Test Cases

<!--Test cases for an implementation are mandatory for SIPs but can be included with the implementation..-->



### 实施方法 Implementation

<!--Please list all values configurable under this implementation.-->

-
## 版权 Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

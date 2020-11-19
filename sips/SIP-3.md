---
sip: SIP-3
title: 新增USDT、ETH矿池提案
status: WIP
author: Fudezl (@Fudezl)

created: 2020-11-18
---

<!--You can leave these HTML comments in your merged SIP and delete the visible duplicate text guides, they will not appear and may be helpful to refer to if you edit it again. This is the suggested template for new SIPs. Note that a SIP number will be assigned by an editor. When opening a pull request to submit your SIP, please use an abbreviated title in the filename, `sip-draft_title_abbrev.md`. The title should be 44 characters or less.-->

## 摘要 Summary

<!--"If you can't explain it simply, you don't understand it well enough." Simply describe the outcome the proposed changes intends to achieve. This should be non-technical and accessible to a casual community member.-->

- 新增USDT/SYX、ETH/SYX两个交易资产矿池；
- 调整VLX、VLX/SYX、USDT/SYX、ETH/SYX矿池奖励分配比例；

## 简述 Abstract

<!--A short (~200 word) description of the proposed change, the abstract should clearly describe the proposed change. This is what *will* be done if the SIP is implemented, not *why* it should be done or *how* it will be done. If the SIP proposes deploying a new contract, write, "we propose to deploy a new contract that will do x".-->

为激励VLX用户参与到Symblox的流动性挖矿中，设立了无风险种子矿池（VLX）、交易矿池（VLX/SYX）。首期Symblox的流动性挖矿还剩下3周左右 ，社区对于新增资产诉求日渐强烈，不再满足于当前单一资产的挖矿（VLX、VLX/SYX），因此急需增加新的资产，故本次提案新增USDT、ETH两个矿池。
 
当前种子矿池（VLX）与交易矿池（VLX/SYX）中奖励分配比例分别为10：90，为支持持有VLX代币用户可继续享受无风险挖矿，本次VLX种子矿池将依旧保留一定奖励分配比例。因总分配比例为100%，现增加了新的矿池，故需对已有矿池（VLX、VLX/SYX）及新的矿池（USDT/SYX、ETH/SYX）奖励分配比例进行重新调整。

## 目的 Motivation

<!--This is the problem statement. This is the *why* of the SIP. It should clearly explain *why* the current state of the protocol is inadequate. It is critical that you explain *why* the change is needed, if the SIP proposes changing how something is calculated, you must address *why* the current calculation is innaccurate or wrong. This is not the place to describe how the SIP will address the issue!-->

为吸引更多元化的资产参与到 Symblox 协议中作为未来 Symblox 衍生品的抵押资产，从而进一步增加 Symblox 协议的资产规模以及流动性。

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
- USDT/SYX
- ETH/SYX

矿池奖励分配比例调整
- 将原种子矿池比例（VLX）调整为5%；
- 将原交易矿池比例（VLX/SYX）调整为75%；
- 新增的资产矿池奖励分配比例（USDT/SYX、ETH/SYX）各调整为10%；

|  矿池/交易对名称  | 调整前  | 调整后 |
|  ----  | :----:  | :----: |
| VLX 种子池 | 10% | 5% |
| VLX/SYX | 90% | 75% |
| USDT/SYX | - | 10% |
| ETH/SYX | - | 10% |

### 原由 Rationale

<!--This is where you explain the reasoning behind how you propose to solve the problem. Why did you propose to implement the change in this way, what were the considerations and trade-offs. The rationale fleshes out what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.-->

VELAS 跨链属于全新推出的功能，具有一定的风险性。因此，建议用户在投入资产数量时应做好风险评估，不宜超过自己可承担损失的数量。

在 SYX 挖矿奖励分配比例上，本次新增的 USDT/SYX、ETH/SYX矿池建议先各分配10%比例，如运行良好，期间有用户希望调整这两个新增矿池比例时，可对奖励分配比例另行发起投票调整比例。

### 技术实现说明 Technical Specification

<!--The technical specification should outline the public API of the changes proposed. That is, changes to any of the interfaces Synthetix currently exposes or the creations of new ones.-->



### 测试方案 Test Cases

<!--Test cases for an implementation are mandatory for SIPs but can be included with the implementation..-->



### 实施方法 Implementation

<!--Please list all values configurable under this implementation.-->

- 创建 vUSDT/SYX 交易池；
- 创建 vETH/SYX 交易池；
- 创建新增交易池链上提案；提案包括以下5个动作 (Actions)：
    - 向 RewardManager 添加 vUSDT/SYX 交易池，并设置奖励数为 2
    - 向 RewardManager 添加 vETH/SYX 交易池，并设置奖励数为 2
    - 向 ConnectorFactory 添加 vUSDT/SYX 交易池的 ConnectorImplementation
    - 向 ConnectorFactory 添加 vETH/SYX 交易池的 ConnectorImplementation
    - 设置 VLX/SYX 交易池奖励数为 15

## 版权 Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

---
sip: SIP-3
title: 新增USDT、ETH矿池提案
status: WIP
author: Fudezl (@Fudezl)

created: 2020-11-18
---

<!--You can leave these HTML comments in your merged SIP and delete the visible duplicate text guides, they will not appear and may be helpful to refer to if you edit it again. This is the suggested template for new SIPs. Note that a SIP number will be assigned by an editor. When opening a pull request to submit your SIP, please use an abbreviated title in the filename, `sip-draft_title_abbrev.md`. The title should be 44 characters or less.-->

## Simple Summary

<!--"If you can't explain it simply, you don't understand it well enough." Simply describe the outcome the proposed changes intends to achieve. This should be non-technical and accessible to a casual community member.-->

- 新增USDT/SYX、ETH/SYX两个交易资产矿池；
- 调整VLX、VLX/SYX、USDT/SYX、ETH/SYX矿池奖励分配比例；

## Abstract

<!--A short (~200 word) description of the proposed change, the abstract should clearly describe the proposed change. This is what *will* be done if the SIP is implemented, not *why* it should be done or *how* it will be done. If the SIP proposes deploying a new contract, write, "we propose to deploy a new contract that will do x".-->

为激励VLX用户参与到Symblox的流动性挖矿中，设立了无风险种子矿池（VLX）、交易矿池（VLX/SYX）。首期Symblox的流动性挖矿还剩下3周左右 ，社区对于新增资产诉求日渐强烈，不再满足于当前单一资产的挖矿（VLX、VLX/SYX），因此急需增加新的资产，故本次提案新增USDT、ETH两个矿池。
 
当前种子矿池（VLX）与交易矿池（VLX/SYX）中奖励分配比例分别为10：90，为支持持有VLX代币用户可继续享受无风险挖矿，本次VLX种子矿池将依旧保留一定奖励分配比例。因总分配比例为100%，现增加了新的矿池，故需对已有矿池（VLX、VLX/SYX）及新的矿池（USDT/SYX、ETH/SYX）的奖励分配比例进行重新调整。

## Motivation

<!--This is the problem statement. This is the *why* of the SIP. It should clearly explain *why* the current state of the protocol is inadequate. It is critical that you explain *why* the change is needed, if the SIP proposes changing how something is calculated, you must address *why* the current calculation is innaccurate or wrong. This is not the place to describe how the SIP will address the issue!-->

为了吸引更多元化的资产参与到 Symblox 协议中作为未来 Symblox 衍生品的抵押资产，从而进一步增加 Symblox 协议的资产规模以及流动性。

## Specification

<!--The specification should describe the syntax and semantics of any new feature, there are five sections
1. Overview
2. Rationale
3. Technical Specification
4. Test Cases
5. Configurable Values
-->

### Overview

<!--This is a high level overview of *how* the SIP will solve the problem. The overview should clearly describe how the new feature will be implemented.-->

This is a high level overview of _how_ the SIP will solve the problem. The overview should clearly describe how the new feature will be implemented.

### Rationale

<!--This is where you explain the reasoning behind how you propose to solve the problem. Why did you propose to implement the change in this way, what were the considerations and trade-offs. The rationale fleshes out what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.-->

This is where you explain the reasoning behind how you propose to solve the problem. Why did you propose to implement the change in this way, what were the considerations and trade-offs. The rationale fleshes out what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.

### Technical Specification

<!--The technical specification should outline the public API of the changes proposed. That is, changes to any of the interfaces Synthetix currently exposes or the creations of new ones.-->

The technical specification should outline the public API of the changes proposed. That is, changes to any of the interfaces Synthetix currently exposes or the creations of new ones.

### Test Cases

<!--Test cases for an implementation are mandatory for SIPs but can be included with the implementation..-->

Test cases for an implementation are mandatory for SIPs but can be included with the implementation.

### Configurable Values

<!--Please list all values configurable under this implementation.-->

Please list all values configurable under this implementation.

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

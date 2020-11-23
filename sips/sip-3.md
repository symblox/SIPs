---
sip: 3
title: Add USDT/SYX Swap Pool
status: Proposed
author: hxl009 (@hxl009)

created: 2020-11-17
---

## Simple Summary

该sip建议增加USDT矿池挖矿，并调整原有矿池与新矿池的收益配比。

This SIP proposes to add a USDT/SYX swap pool, and change the reward allocation ratio for exisiting pools.

## Abstract

增加USDT矿池挖矿，并调整原有矿池与新矿池的收益配比。调整后 VLX 种子池：VLX 交易池：USDT 交易池收益比率分别为 5%：65%：30%。

In order to add more liquidity to Symblox, we propose to add USDT/SYX swap pool first, and set the reward allocation ratios for VLX seed pool, VLX swap pool, and USDT swap pool to 5%, 65%, and 30% respectively.

## Motivation

目前只有VLX可以参与挖矿，为激励更多的用户加入SYX流动性挖矿，提升整个项目的活跃度以及市场份额，我们提案开通USDT矿池挖矿，因为 USDT 当前的市值超过 10 亿美元而且也是流动性最好的数字资产之一。

Right now, only VLX holders can participate Symblox yield farming. In order to encourage more users to join Symblox and increase the activity and market share of the entire project, we proposes to add USDT swap pool first beause USDT has over 1 billion market cap, and is so far one of the most liuqid assets in crypto.

## Specification

### Overview

提案分为以下3步
There are 3 steps for the proposal. 

- 首先，创建 SYX 和 USDT 的 Balancer Pool (BPT)，并设置 BPT 相应的比例为 80:20。例如，当目前价格为 1 SYX = 1 USDT 时， 该交易池每 1个 USDT 需对应 4个 SYX;
- Firstly, we create a new Balancer pool for SYX and USDT, and set the weights of SYX and USDT to be 80:20 respectively. For example, assuming the market price for 1 SYX = 1 USDT, there needs to be 4 SYX for every USDT in the pool;

- 然后，将 USDT/SYX 的交易池添加到 RewardManager，并设置该矿池的奖励点数为 6;
- Secondly, we need to add the new USDT/SYX Balancer pool to the RewardManager, and set the reward allocation points to 6;

- 最后，设置 VLX/SYX 交易池的奖励点数为 13。
- Lastly, we set the reward allocation points for VLX/SYX swap pool to be 13.

| Pool Name 矿池名称 | Before 修改前 | After 修改后 | Allocation Points 奖励点数 |
|---|---:|---:|---:|
| VLX Seed 种子池 | 10% | 5% | 1 |
| VLX Swap 交易池 | 90% | 65% | 13 |
| USDT Swap 交易池 | - | 30% | 6 |

### Rationale

### Technical Specification

---
sip:<to be assigned>
title:<SIP title>
status:WIP
author:foo@bar.com>,FirstName (GitHubUsername) and GitHubUsername (@GitHubUsername)>discussions-to:<Create a new thread on http:s//t.me/symbloxsips and drop the link here>

created:<date created on, in ISO 8601(yyyy-mm-dd)format>
requires(*optional):<SIP number(s)>
---
sip: 4
title: Add ETH/SYX Swap Pool
status: Proposed
author: xizi0803(@xizi0803)

created: 2020-11-29
---

## Simple Summary

该sip建议增加ETH/SYX矿池挖矿，并调整原有矿池与新矿池的收益配比。

This SIP proposes to add a ETH/SYX swap pool, and change the reward allocation ratio for exisiting pools.

## Abstract

增加ETH/SYX矿池挖矿，并调整原有矿池与新矿池的收益配比。调整后 VLX 种子池：VLX 交易池：USDT 交易池:ETH交易池收益比率分别为 5%：35%：30%：30%。

In order to add more liquidity to Symblox, we propose to add ETH/SYX swap pool first, and set the reward allocation ratios for VLX seed pool, VLX swap pool, USDT swap pool ，and ETH swap pool to 5%, 35%, 30% and 30% respectively.

## Motivation

目前只有VLX 和USDT 可以参与挖矿，为激励更多的用户加入SYX流动性挖矿，提升整个项目的活跃度以及市场份额，我们提案开通ETH矿池挖矿，因为 ETH当前的市值超过 10 亿美元而且也是流动性最好的数字资产之一。

Right now, only VLX and USDT holders can participate Symblox yield farming. In order to encourage more users to join Symblox and increase the activity and market share of the entire project, we proposes to add ETH swap pool first beause ETH has over 1 billion market cap, and is so far one of the most liuqid assets in crypto.

## Specification

### Overview

提案分为以下3步
There are 3 steps for the proposal. 

- 首先，创建 SYX 和 ETH  的 Balancer Pool (BPT)，并设置 BPT 相应的比例为 20:1。例如，当目前价格为 1ETH = 20SYX时， 该交易池每 1个 ETH 需对应 20个 SYX;
- Firstly, we create a new Balancer pool for SYX and ETH, and set the weights of SYX and ETH to be 20:1 respectively. For example, assuming the market price for 20SYX = 1ETH, there needs to be 20SYX for every ETH in the pool;

- 然后，将 ETH/SYX 的交易池添加到 RewardManager，并设置该矿池的奖励点数为 6;
- Secondly, we need to add the new ETH/SYX Balancer pool to the RewardManager, and set the reward allocation points to 6;

- 最后，设置 VLX/SYX 交易池的奖励点数为 7。
- Lastly, we set the reward allocation points for VLX/SYX swap pool to be 7.

| Pool Name 矿池名称 | Before 修改前 | After 修改后 | Allocation Points 奖励点数 |
|---|---:|---:|---:|
| VLX Seed 种子池 | 5% | 5% | 1 |
| VLX Swap 交易池 | 65% | 35% | 7 |
| USDT Swap 交易池 | 30%| 30% | 6 |
| ETH Swap 交易池 |- | 30% | 6 |

### Rationale

### Technical Specification

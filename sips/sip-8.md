---
sip: 8
title: Add/Remove Liquidity with 2 Tokens
status: Proposed
author: vs2021（@ vs2021）

created: 2021-01-14
---

## Simple Summary

增加双资产平衡流动性矿池三个:
- VLX+SYX,比例50%；
- USDT+SYX,比例25%；
- ETH+SYX,比例25%；

币币交易功能支持的资产如下:
VLX.SYX.USDT.ETH

This SIP proposes to add new swap pools, including SYX/VLX, SYX/USDT, and SYX/ETH that support adding/removing liquidity with 2 tokens; and change the reward allocation ratios for exisiting pools.

## Abstract

该sip建议增加双资产平衡比例的流动性矿池挖矿，该类矿池是为 Symblox 提供基础流动性而设，减少了参与者的挖矿风险，根据vlx和syx在symblox平台的时时价格，价值平衡后的份额（LP token）参与挖矿。

例如：当前是 1syx = 20vlx，那么 20vlx + 1syx 为1份参与额，依次类推，同时调整现有交易池的奖励分配比率。

This SIP proposes to add swap pools that support adding/removing liquidity with 2 tokens to provide liquidity for Symblox tokens and minimize the volatilities for liquidity providers. The amount of each tokens is determined by the market price when adding or removing the liquidity. For example, if the current exchange rate for 1 syx = 20 vlx, there will be 1 syx to 20 vlx ratio when adding the liquidity, and same goes true when removing the liquidity. 


## Motivation

此方案将提供流动性与交易兑划分开来，让不愿意承受风险的参与者也能通过双资产平衡矿池来提供流动性获取奖励，让出色的交易者可以在交易池中享受风险与利润并存的快感。伴随人们大胆参与，参与者基数大增，流动性资产基数大增，可承载更多资产的交易，逐渐有更多资产的矿池上线，合成资产上线，使symblox成为全球defi爱好者的首选平台。

The intent of this proposal is to minimize the volatilities for the liquidity providers so that more liquidity can be brought to Symblox; and at the same time traders will be able to profit by using the swap function of the pool. 


## Specification

调整后：

1、双资产矿池

- SYX / VLX, 矿池资产比例为 SYX 40 : VLX 60，奖励比例50%；
- SYX / USDT，矿池资产比例为 SYX 90 : USDT 10，奖励比例25%；
- SYX / ETH，矿池资产比例为 SYX 90 : ETH 10，奖励比例25%；

2、单资矿池

- vlx / syx 交易池占比0％
- vlx / usdt 交易池占比0%
- SYX / usdt 交易池占比0％
- vlx / eth 交易池占比0％
- syx / eth 交易池占比0％

There will be 3 new pools that support adding/removing liquidity with 2 tokens

- SYX/VLX, with the asset ratio being SYX 40 : VLX 60, reward ratio 50%;
- SYX/USDT, asset ratio SYX 90 : USDT 10, reward ratio 25%;
- SYX/ETH, asset ratio SYX 90 : ETH 10, reward ratio 25%

### Overview

| Pool Name 矿池名称 | Before 修改前 | After 修改后 | Allocation Points 奖励点数 |
| ------------------ | ------------: | -----------: | -------------------------: |
| VLX+SYX           |         - |          50% |                       2|
| USDT+SYX           |         - |          25% |                       1|
| ETH+SYX           |         - |          25% |                       1|
| SYX/VLX            |         66% |          0% |                        0|
| VLX/USDT           |         5% |           0% |                          0 |
| SYX/USDT           |        12% |          0% |                        0 |
| SYX/ETH            |        12% |          0% |                        0 |
| VLX/ETH            |        5% |           0% |                          0 |

### Technical Specification

提案分为以下3步 There are 3 steps for the proposal.

- 创建双资产 SYX 和 VLX 的 Balancer Pool (BPT)，并设置 BPT 相应的比例为 40:60; Create a new Balancer pool for SYX and VLX, and set the asset weights of SYX and VLX to be 40:60 respectively;

- 创建双资产 SYX 和 USDT 的 Balancer Pool (BPT)，并设置 BPT 相应的比例为 90:10; Create a new Balancer pool for SYX and USDT, and set the asset weights to be 90:10 respectively;

- 创建双资产 SYX 和 ETH 的 Balancer Pool (BPT)，并设置 BPT 相应的比例为 90:10; Create a new Balancer pool for SYX and ETH, and set the asset weights to be 90:10 respectively;

- 将新的 SYX / VLX 的交易池添加到 RewardManager，并设置该矿池的奖励点数为 2; Add the new SYX/VLX Balancer pool to the RewardManager, and set the reward allocation points to 2;

- 将新的 SYX / USDT 的交易池添加到 RewardManager，并设置该矿池的奖励点数为 1; Add the new SYX/USDT Balancer pool to the RewardManager, and set the reward allocation points to 1;

- 将新的 SYX / ETH 的交易池添加到 RewardManager，并设置该矿池的奖励点数为 1; Add the new SYX/ETH Balancer pool to the RewardManager, and set the reward allocation points to 1;

- 将单资产 SYX / VLX 的交易池奖励点数设置为 0; Set the old SYX / VLX pool reward allocation points to 0;

- 将单资产 SYX / USDT 的交易池奖励点数设置为 0; Set the old SYX / USDT pool reward allocation points to 0;

- 将单资产 SYX / ETH 的交易池奖励点数设置为 0; Set the old SYX / ETH pool reward allocation points to 0;

- 将单资产 VLX / USDT 的交易池奖励点数设置为 0; Set the old VLX / USDT pool reward allocation points to 0;

- 将单资产 VLX / ETH 的交易池奖励点数设置为 0; Set the old VLX / ETH pool reward allocation points to 0;


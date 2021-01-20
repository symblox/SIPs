---
sip: 8
title: Add/Remove Liquidity with 2 Tokens
status: Proposed
author: vs2021（@ vs2021）

created: 2021-01-14
---

## Simple Summary

添加VLX + SYX双资产平衡流动性矿池


## Abstract

该sip建议增加VLX + SYX双资产平衡比例的流动性矿池挖矿，该矿池是为Symblox提供基础流动性而设，减少了参与者的挖矿风险，根据vlx和syx在symblox平台的时时价格，价值平衡后的份额（LP token）参与挖矿。

例如：当前是20vlx ＝ 1syx，那么20vlx + 1syx为1份参与额，依次类推，同时调整现有交易池的奖励分配比率。


## Motivation

此方案将提供流动性与交易兑划分开来，让不愿意承受风险的参与者也能通过双资产平衡矿池来提供流动性获取奖励，让出色的交易者可以在交易池中享受风险与利润并存的快感。伴随人们大胆参与，参与者基数大增，流动性资产基数大增，可承载更多资产的交易，逐渐有更多资产的矿池上线，合成资产上线，使symblox成为全球defi爱好者的首选平台。


## Specification

调整后，vlx + syx双资产平衡流动性矿池挖矿奖励占比50％。待这个基础矿池根基稳定后，依次可增加其他资产＋ syx的双资产平衡流动性矿池。
vlx / syx交易池占比10％
vlx / usdt交易池占比10%
SYX /美元交易池占比10％
vlx / eth交易池占比10％
syx / eth交易池占比10％

### Overview


| Pool Name 矿池名称 | Before 修改前 | After 修改后 | Allocation Points 奖励点数 |
| ------------------ | ------------: | -----------: | -------------------------: |
| vlx + syx           |         - |          50% |                       5|
| SYX/VLX            |         66% |          10% |                       1 |
| VLX/USDT           |         5% |           10% |                          1 |
| SYX/USDT           |        12% |          10% |                        1 |
| SYX/ETH            |        12% |          10% |                        1 |
| VLX/ETH            |        5% |           10% |                          1 |

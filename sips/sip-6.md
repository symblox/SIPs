---
sip: 6
title: Change Reward Allocation Points for Swap Pools
status: Proposed
author: hxl009(@hxl009)
discussions-to: https://t.me/symbloxsips
created: 2020-12-28

---
## Simple Summary

该sip修改现有5个矿池的挖矿配比。调整后挖矿分配比例为 SYX2/VLX：SYX2/USDT: SYX2/ETH: USDT/VLX：ETH/VLX = 66%:12%:12%:5%:5%
Change the reward allocations of the swap pools to 66%, 12%, 12%, 5%, and 5% for SYX2/VLX, SYX2/USDT, SYX2/ETH, USDT/VLX, and ETH/VLX respectively.

## Abstract

基于现有提供流动性的资金情况，现有VLX挖矿相对于USDT和ETH挖矿的收益配比相差太远，为确保SYMBLOX总市值实现正向现金流，同时提高symblox的流动性，建议修改现有矿池的收益分配比。
Based on the existing funds that provide liquidity, the profit ratio of existing VLX mining compared to USDT and ETH mining is too far apart. In order to ensure the total market value of SYMBLOX to achieve positive cash flow, and to improve the liquidity of SYMBLOX, it is recommended to modify The reward distribution ratio of existing mining pools.

### Overview

| Pool Name 矿池名称 | Before 修改前 | After 修改后
|---|---:|---:|
| SYX/VLX  Swap 交易池 | 42% | 66% |
| VLX/USDT  Swap 交易池 | 7%  |  5% |
| SYX/USDT Swap 交易池 | 22% | 12% |
| SYX/ETH  Swap 交易池 | 22% | 12% |
| VLX/ETH   Swap 交易池 | 7%  |  5% |

### Technical Specification

提案分为以下 5 个动作
There are 5 steps for the proposal. 

- 设置 VLX/SYX 交易池的奖励点数为 13.2;
- Set the reward allocation points for VLX/SYX swap pool to be 13.2;

- 设置 USDT/VLX 交易池的奖励点数为 1;
- Set the reward allocation points for VLX/SYX swap pool to be 13.2;

- 设置 SYX/USDT 交易池的奖励点数为 2.4;
- Set the reward allocation points for VLX/SYX swap pool to be 13.2;

- 设置 SYX/ETH 交易池的奖励点数为 2.4;
- Set the reward allocation points for VLX/SYX swap pool to be 13.2;

- 设置 VLX/ETH 交易池的奖励点数为 1;
- Set the reward allocation points for VLX/SYX swap pool to be 13.2;

| Pool Name 矿池名称 | Before 修改前 | After 修改后 | Allocation Points 奖励点数 |
|---|---:|---:|---:|
| SYX/VLX  Swap 交易池 | 42% | 66% | 13.2 |
| VLX/USDT  Swap 交易池 | 7%  |  5% | 1 |
| SYX/USDT Swap 交易池 | 22% | 12% | 2.4 |
| SYX/ETH  Swap 交易池 | 22% | 12% | 2.4 |
| VLX/ETH   Swap 交易池 | 7%  |  5% | 1 |

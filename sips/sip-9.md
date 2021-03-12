---
sip: 9
title: Kick-start a New Symblox Yield Farming Season on VELAS
status: Proposed
author: symblox(@symblox)

created: 2021-03-04
---

## Simple Summary

为 Symblox 新一季流动性挖矿发行 512,000 个 SYX 代币；并且支持 sVLX 合成资产挖矿；新增交易对：sVLX+SYX；同时调整现有矿池奖励比例。

This SIP proposes to mint 512,000 SYX tokens to RewardManager, and start a new yield farming season with trading pairs of sVLX/SYX, VLX/SYX, USDT/SYX, and ETH/SYX.

## Abstract

Symblox 协议 sVLX 合成资产即将上线 VELAS 区块链，目前在 VELAS 区块链上的流动性挖矿支持 4 个资产参与挖矿，分别是 VLX、SYX、USDT、ETH。
第 4 期流动性挖矿资产延续第三期流动性支持的资产同时，将新增 sVLX 资产进行挖矿。而 sVLX 合成资产则来自 VLX 资产质押而得，为鼓励给 sVLX 合成资产提供流动性的用户，社区提案增加"sVLX"资产参与流动性挖矿。

The new sVLX asset will be launched on VELAS, and now there are already 4 supported assets for Symblox yield farming, which are VLX, SYX, USDT, ETH. The new season will continue to support those assets while would like to include the new sVLX asset so that VLX holders can enjoy VLX staking rewards while participate the yield farming.

## Specification

1. 向奖励池 RewardManager 发行 51.2 万枚 SYX 代币；

2. 新增资产交易对，并给予该交易对挖矿奖励；

- 创建 VLX+SYX 矿池并设置资产比例分别为 50:50;
- 创建 sVLX+SYX 矿池并设置资产比例分别为 50:50;
- 创建 USDT+SYX 矿池并设置资产比例分别为 10:90;
- 创建 ETH+SYX 矿池并设置资产比例分别为 10:90;

3. 矿池奖励分配比例调整

- 将 VLX+SYX 矿池奖励比例设置为：40%
- 将 sVLX+SYX 矿池奖励比例设置为：20%；
- 将 USDT+SYX 矿池奖励比例设置为：20%；
- 将 ETH+SYX 矿池奖励分配比例设置为：20%；

There are 3 parts of this proposal

1. Mint 512,000 SYX tokens to RewardManager;

2. Create Balancer pools for all the supported trading pairs, which are:

- VLX / SYX, with asset weight ratio 50:50
- sVLX / SYX, with asset weight ratio 50:50
- USDT / SYX, with asset weight ratio 10:90
- ETH / SYX, with asset weight ratio 10:90

3. Add those pools to the RewardManager and set the reward ratios, which are:

- VLX / SYX, 40%
- sVLX / SYX, 20%
- USDT / SYX, 20%
- ETH / SYX, 20%

### Overview

| Pool Name 矿池名称 | Before 修改前 | After 修改后 | Allocation Points 奖励点数 |
| ------------------ | ------------: | -----------: | -------------------------: |
| VLX+SYX            |           50% |          40% |                          2 |
| USDT+SYX           |           25% |          20% |                          1 |
| ETH+SYX            |           25% |          20% |                          1 |
| SVLX+SYX           |             - |          20% |                          1 |

### Technical Specification

提案分为以下几步

- 向 RewardManager 发行数量 512,000 的 SYX 代币;

- 创建双资产 SYX 和 VLX 的 Balancer Pool (BPT)，并设置 BPT 相应的比例为 50:50;
- 创建双资产 SYX 和 USDT 的 Balancer Pool (BPT)，并设置 BPT 相应的比例为 90:10;
- 创建双资产 SYX 和 ETH 的 Balancer Pool (BPT)，并设置 BPT 相应的比例为 90:10;
- 创建双资产 SYX 和 SVLX 的 Balancer Pool (BPT)，并设置 BPT 相应的比例为 50:50;

- 将 SYX / VLX 的交易池添加到 RewardManager，并设置该矿池的奖励点数为 2;
- 将 SYX / USDT 的交易池添加到 RewardManager，并设置该矿池的奖励点数为 1;
- 将 SYX / ETH 的交易池添加到 RewardManager，并设置该矿池的奖励点数为 1;
- 将 SYX / SVLX 的交易池添加到 RewardManager，并设置该矿池的奖励点数为 1;

There are the following steps for the proposal:

- Mint 512,000 SYX tokens to RewardManager;

- Create a new Balancer pool for SYX and VLX, and set the asset weights of SYX and VLX to be 50:50 respectively;
- Create a new Balancer pool for SYX and USDT, and set the asset weights to be 90:10 respectively;
- Create a new Balancer pool for SYX and ETH, and set the asset weights to be 90:10 respectively;
- Create a new Balancer pool for SYX and SVLX, and set the asset weights of SYX and VLX to be 50:50 respectively;

- Add SYX/VLX pool to the RewardManager, and set the reward allocation points to 2;
- Add SYX/USDT pool to the RewardManager, and set the reward allocation points to 1;
- Add SYX/ETH pool to the RewardManager, and set the reward allocation points to 1;
- Add SYX/SVLX pool to the RewardManager, and set the reward allocation points to 1;

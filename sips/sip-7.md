---
sip: 7
title: Change Reward Allocations for SYX/VLX and VLX/ETH Pools
status: WIP
author: Symblox (@symblox)

created: 2020-11-17
---

## Simple Summary

该 sip 建议调整 SYX/VLX 和 VLX/ETH 矿池的比例。

This SIP proposes to change the reward allocation ratio for SYX/VLX and VLX/ETH pools.

## Abstract

将 SYX/VLX 和 VLX/ETH 的矿池奖励分配点分别调整为 13.2 和 1。

We propose to set the reward allocation ratios for SYX/VLX and VLX/ETH pools to be 13.2 and 1 respectively.

## Motivation

根据上次 SIP 6 号提案的内容，需要将当前的 5 个矿池奖励比例分布做出调整，但是因为链上投票最后一步设置错误，造成 SYX/VLX 和 VLX/ETH 的奖励分配点错误设置。因此，我们建议通过这个提案及时修复上述的修复错误。

Previous SIP-6 is supposed to change the ratio allocation rewards for all the exisiting pools. But because the errors in creating the on-chain proposal, SYX/VLX and VLX/ETH pools now have the incorrect reward allocation ratios. We propose to fix the issues with this new proposal.

## Specification

### Overview

提案分为以下 2 步
There are 2 steps for the proposal.

- 首先，将 SYX/VLX 矿池的奖励点数设置为 13.2;
- Firstly, set the SYX/VLX pool (ID #0)'s reward allocation ratio to 13.2;

- 然后，将 VLX/ETH 矿池的奖励点数设置为 1;
- Secondly, set the VLX/ETH pool (ID #4)'s reward allocation ratio to 1;

| Pool Name 矿池名称 | Before 修改前 | After 修改后 | Allocation Points 奖励点数 |
| ------------------ | ------------: | -----------: | -------------------------: |
| SYX/VLX            |         7.24% |          66% |                       13.2 |
| VLX/USDT           |         7.24% |           5% |                          1 |
| SYX/USDT           |        17.39% |          12% |                        2.4 |
| SYX/ETH            |        17.39% |          12% |                        2.4 |
| VLX/ETH            |        50.72% |           5% |                          1 |

---
sip: <to be assigned>
title: <SIP title>
status: WIP
author: <a list of the author's or authors' name(s) and/or username(s), or name(s) and email(s), e.g. (use with the parentheses or triangular brackets): FirstName LastName (@GitHubUsername), FirstName LastName <foo@bar.com>, FirstName (@GitHubUsername) and GitHubUsername (@GitHubUsername)>
discussions-to: <Create a new thread on https://t.me/symbloxsips and drop the link here> 

created: <date created on, in ISO 8601 (yyyy-mm-dd) format>
requires (*optional): <SIP number(s)>
---
## Simple Summary

该sip修改现有5个矿池的挖矿配比。调整后 SYX2/VLX：USDT/VLX：SYX2/USDT:SYX2/ETH:ETH/VLX=66%:12%:12%:5%:5%

## Abstract

基于现有提供流动性的资金情况，现有VLX挖矿相对于USDT和ETH挖矿的收益配比相差太远，同时因为收益低，大部分一期VLX参与挖矿的资金出现外流，为了提高symblox的流动性，建议修改现有矿池的收益分配比。

## Motivation

目前

## Specification

### Overview

| Pool Name 矿池名称 | Before 修改前 | After 修改后 | Allocation Points 奖励点数 |
|---|---:|---:|---:|
| SYX2/VLX  Swap 交易池 | 42% | 66% |  |
| USDT/VLX  Swap 交易池 | 7%  |  5% |  |
| SYX2/USDT Swap 交易池 | 22% | 12% |  |
| SYX2/ETH  Swap 交易池 | 22% | 12% |  |
| ETH/VLX   Swap 交易池 | 7%  |  5% |  |

### Rationale

### Technical Specification

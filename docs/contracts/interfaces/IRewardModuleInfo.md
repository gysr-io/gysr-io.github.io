---
layout: page
title: IRewardModuleInfo
description: "this contract defines the common interface that any reward module info
must implement to be compatible with the modular Pool architecture."
permalink: /docs/IRewardModuleInfo/
exclude: true
categories: [contract]
---

Reward module info interface



**`IRewardModuleInfo`**

this contract defines the common interface that any reward module info
must implement to be compatible with the modular Pool architecture.







****
<br>

**`tokens`**`(address module) → address[], string[], string[], uint8[]` (external)

get all token metadata




*Parameters*  
- `module`: address of reward module




****
<br>

**`rewards`**`(address module, bytes32 account, uint256 shares, bytes data) → uint256[]` (external)

generic function to get pending reward balances




*Parameters*  
- `module`: address of reward module

- `account`: bytes32 account of interest for preview

- `shares`: number of shares that would be used

- `data`: additional encoded data


*Returns*  
- estimated reward balances



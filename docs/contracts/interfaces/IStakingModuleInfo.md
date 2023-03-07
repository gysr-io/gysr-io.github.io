---
layout: page
title: IStakingModuleInfo
description: "this contract defines the common interface that any staking module info
must implement to be compatible with the modular Pool architecture."
permalink: /docs/IStakingModuleInfo/
exclude: true
categories: [contract]
---

Staking module info interface



**`IStakingModuleInfo`**

this contract defines the common interface that any staking module info
must implement to be compatible with the modular Pool architecture.







****
<br>

**`tokens`**`(address module) → address[], string[], string[], uint8[]` (external)

convenience function to get all token metadata in a single call




*Parameters*  
- `module`: address of staking module




****
<br>

**`positions`**`(address module, address addr, bytes data) → bytes32[], uint256[]` (external)

get all staking positions for user




*Parameters*  
- `module`: address of staking module

- `addr`: user address of interest

- `data`: additional encoded data





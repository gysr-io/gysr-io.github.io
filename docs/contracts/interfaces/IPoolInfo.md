---
layout: page
title: IPoolInfo
description: "this defines the Pool info contract interface"
permalink: /docs/IPoolInfo/
exclude: true
categories: [contract]
---

Pool info interface



**`IPoolInfo`**

this defines the Pool info contract interface







****
<br>

**`modules`**`(address pool) → address, address, address, address` (external)

get information about the underlying staking and reward modules




*Parameters*  
- `pool`: address of Pool contract


*Returns*  
- staking module address

- reward module address

- staking module type

- reward module type


****
<br>

**`rewards`**`(address pool, address addr, bytes stakingdata, bytes rewarddata) → uint256[]` (external)

get pending rewards for arbitrary Pool and user pair




*Parameters*  
- `pool`: address of Pool contract

- `addr`: address of user for preview

- `stakingdata`: additional data passed to staking module info library

- `rewarddata`: additional data passed to reward module info library




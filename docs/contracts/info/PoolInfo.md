---
layout: page
title: PoolInfo
description: "this implements the Pool info library, which provides read-only
convenience functions to query additional information and metadata
about the core Pool contract."
permalink: /docs/PoolInfo/
exclude: true
categories: [contract]
---

Pool info library



**`PoolInfo`**

this implements the Pool info library, which provides read-only
convenience functions to query additional information and metadata
about the core Pool contract.







****
<br>

**`modules`**`(address pool) → address, address, address, address` (public)

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

**`register`**`(address factory, address info)` (external)

register factory to info module




*Parameters*  
- `factory`: address of factory

- `info`: address of info module contract



****
<br>

**`rewards`**`(address pool, address addr, bytes stakingdata, bytes rewarddata) → uint256[] rewards_` (public)

get pending rewards for arbitrary Pool and user pair




*Parameters*  
- `pool`: address of Pool contract

- `addr`: address of user for preview

- `stakingdata`: additional data passed to staking module info library

- `rewarddata`: additional data passed to reward module info library




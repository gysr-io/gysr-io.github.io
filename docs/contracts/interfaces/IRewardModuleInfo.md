---
layout: page
title: IRewardModuleInfo
description: "this contract defines the common interface that any reward module info
must implement to be compatible with the modular Pool architecture."
permalink: /docs/IRewardModuleInfo/
exclude: true
categories: [contract]
---

### Reward module info interface



`IRewardModuleInfo`

this contract defines the common interface that any reward module info
must implement to be compatible with the modular Pool architecture.





****

`tokens(address module) → address[], string[], string[], uint8[]` (external)

get all token metadata




**Parameters**  
- `module`: address of reward module


**Returns**


****

`rewards(address module, address addr, uint256 shares) → uint256[]` (external)

generic function to get pending reward balances




**Parameters**  
- `module`: address of reward module

- `addr`: account address of interest for preview

- `shares`: number of shares that would be used


**Returns**
- estimated reward balances



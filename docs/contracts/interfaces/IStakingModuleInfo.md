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

**`token`**`(address module) → address, string, string, uint8` (external)

convenience function to get token metadata in a single call




*Parameters*  
- `module`: address of staking module




****
<br>

**`shares`**`(address module, address addr, uint256 amount) → uint256` (external)

quote the share value for an amount of tokens




*Parameters*  
- `module`: address of staking module

- `addr`: account address of interest

- `amount`: number of tokens. if zero, return entire share balance


*Returns*  
- number of shares


****
<br>

**`sharesPerToken`**`(address module) → uint256` (external)






*Returns*  
- current shares per token



---
layout: page
title: ERC20StakingModuleInfo
description: "this library provides read-only convenience functions to query
additional information about the ERC20StakingModule contract."
permalink: /docs/ERC20StakingModuleInfo/
exclude: true
categories: [contract]
---

ERC20 staking module info library



**`ERC20StakingModuleInfo`**

this library provides read-only convenience functions to query
additional information about the ERC20StakingModule contract.







****
<br>

**`token`**`(address module) → address, string, string, uint8` (public)

convenience function to get token metadata in a single call




*Parameters*  
- `module`: address of staking module




****
<br>

**`shares`**`(address module, address addr, uint256 amount) → uint256` (public)

quote the share value for an amount of tokens




*Parameters*  
- `module`: address of staking module

- `addr`: account address of interest

- `amount`: number of tokens. if zero, return entire share balance


*Returns*  
- number of shares


****
<br>

**`sharesPerToken`**`(address module) → uint256` (public)

get shares per token




*Parameters*  
- `module`: address of staking module


*Returns*  
- current shares per token



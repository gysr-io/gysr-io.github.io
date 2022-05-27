---
layout: page
title: ERC721StakingModuleInfo
description: "this library provides read-only convenience functions to query
additional information about the ERC721StakingModule contract."
permalink: /docs/ERC721StakingModuleInfo/
exclude: true
categories: [contract]
---

ERC721 staking module info library



**`ERC721StakingModuleInfo`**

this library provides read-only convenience functions to query
additional information about the ERC721StakingModule contract.







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


****
<br>

**`tokenIds`**`(address module, address addr, uint256 amount, uint256 start) → uint256[] ids` (public)

get staked token ids for user




*Parameters*  
- `module`: address of staking module

- `addr`: account address of interest

- `amount`: number of tokens to enumerate

- `start`: token index to start at


*Returns*  
- ids array of token ids



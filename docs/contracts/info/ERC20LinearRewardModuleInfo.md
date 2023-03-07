---
layout: page
title: ERC20LinearRewardModuleInfo
description: "this library provides read-only convenience functions to query
additional information about the ERC20LinearRewardModule contract."
permalink: /docs/ERC20LinearRewardModuleInfo/
exclude: true
categories: [contract]
---

ERC20 linear reward module info library



**`ERC20LinearRewardModuleInfo`**

this library provides read-only convenience functions to query
additional information about the ERC20LinearRewardModule contract.







****
<br>

**`tokens`**`(address module) → address[] addresses_, string[] names_, string[] symbols_, uint8[] decimals_` (external)

get all token metadata




*Parameters*  
- `module`: address of reward module




****
<br>

**`token`**`(address module) → address, string, string, uint8` (public)

convenience function to get token metadata in a single call




*Parameters*  
- `module`: address of reward module




****
<br>

**`rewards`**`(address module, bytes32 account, uint256 shares, bytes) → uint256[] rewards_` (public)

generic function to get pending reward balances




*Parameters*  
- `module`: address of reward module

- `account`: bytes32 account of interest for preview

- `shares`: number of shares that would be used


*Returns*  
- rewards_ estimated reward balances


****
<br>

**`preview`**`(address module, bytes32 account) → uint256` (public)

preview estimated rewards




*Parameters*  
- `module`: address of reward module

- `account`: bytes32 account of interest for preview


*Returns*  
- estimated reward


****
<br>

**`runway`**`(address module) → uint256` (public)

compute effective runway with current budget and reward rate




*Parameters*  
- `module`: address of reward module


*Returns*  
- estimated runway in seconds


****
<br>

**`validate`**`(address module, uint256 shares) → bool, uint256` (public)

check potential increase in shares for sufficient budget and runway




*Parameters*  
- `module`: address of reward module

- `shares`: number of shares to be staked


*Returns*  
- okay if stake amount is within budget for time period

- estimated runway in seconds



---
layout: page
title: ERC20CompetitiveRewardModuleInfo
description: "this library provides read-only convenience functions to query
additional information about the ERC20CompetitiveRewardModule contract."
permalink: /docs/ERC20CompetitiveRewardModuleInfo/
exclude: true
categories: [contract]
---

ERC20 competitive reward module info library



**`ERC20CompetitiveRewardModuleInfo`**

this library provides read-only convenience functions to query
additional information about the ERC20CompetitiveRewardModule contract.







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

**`preview`**`(address module, bytes32 account, uint256 shares, uint256 gysr) → uint256, uint256, uint256` (public)

preview estimated rewards




*Parameters*  
- `module`: address of reward module

- `account`: bytes32 account of interest for preview

- `shares`: number of shares that would be unstaked

- `gysr`: number of GYSR tokens that would be applied


*Returns*  
- estimated reward

- estimated time multiplier

- estimated gysr multiplier


****
<br>

**`unlocked`**`(address module) → uint256` (public)

compute effective unlocked rewards




*Parameters*  
- `module`: address of reward module


*Returns*  
- estimated current unlocked rewards


****
<br>

**`userShareSeconds`**`(address module, bytes32 account, uint256 shares) → uint256, uint256` (public)

compute user share seconds for given number of shares




*Parameters*  
- `module`: module contract address

- `account`: user account

- `shares`: number of shares


*Returns*  
- raw share seconds

- time bonus share seconds


****
<br>

**`totalShareSeconds`**`(address module) → uint256` (public)

compute total expected share seconds for a rewards module




*Parameters*  
- `module`: address for reward module


*Returns*  
- expected total shares seconds



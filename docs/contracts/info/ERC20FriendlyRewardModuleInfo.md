---
layout: page
title: ERC20FriendlyRewardModuleInfo
description: "this library provides read-only convenience functions to query
additional information about the ERC20FriendlyRewardModule contract."
permalink: /docs/ERC20FriendlyRewardModuleInfo/
exclude: true
categories: [contract]
---

ERC20 friendly reward module info library



**`ERC20FriendlyRewardModuleInfo`**

this library provides read-only convenience functions to query
additional information about the ERC20FriendlyRewardModule contract.







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

**`rewards`**`(address module, address addr, uint256 shares) → uint256[] rewards_` (public)

generic function to get pending reward balances




*Parameters*  
- `module`: address of reward module

- `addr`: account address of interest for preview

- `shares`: number of shares that would be used


*Returns*  
- rewards_ estimated reward balances


****
<br>

**`preview`**`(address module, address addr, uint256 shares) → uint256, uint256, uint256` (public)

preview estimated rewards




*Parameters*  
- `module`: address of reward module

- `addr`: account address of interest for preview

- `shares`: number of shares that would be unstaked


*Returns*  
- estimated reward

- estimated time multiplier weighted by rewards

- estimated gysr multiplier weighted by rewards


****
<br>

**`unlockable`**`(address module) → uint256` (public)

compute reward shares to be unlocked on the next update




*Parameters*  
- `module`: address of reward module


*Returns*  
- estimated unlockable rewards


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

**`rewardsPerStakedShare`**`(address module) → uint256` (public)

compute effective rewards per staked share




*Parameters*  
- `module`: module contract address


*Returns*  
- estimated rewards per staked share


****
<br>

**`gysrBonus`**`(address module, uint256 shares, uint256 gysr) → uint256` (public)

compute estimated GYSR bonus for stake




*Parameters*  
- `module`: module contract address

- `shares`: number of shares that would be staked

- `gysr`: number of GYSR tokens that would be applied to stake


*Returns*  
- estimated GYSR multiplier



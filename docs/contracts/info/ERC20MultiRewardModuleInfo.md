---
layout: page
title: ERC20MultiRewardModuleInfo
description: "this library provides read-only convenience functions to query
additional information about the ERC20MultiRewardModule contract."
permalink: /docs/ERC20MultiRewardModuleInfo/
exclude: true
categories: [contract]
---

ERC20 multi reward module info library



**`ERC20MultiRewardModuleInfo`**

this library provides read-only convenience functions to query
additional information about the ERC20MultiRewardModule contract.







****
<br>

**`tokens`**`(address module) → address[] addresses_, string[] names_, string[] symbols_, uint8[] decimals_` (external)

convenience function to get all token metadata in a single call




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

**`preview`**`(address module, bytes32 account, uint256 shares, address[] tokens_) → uint256[] rewards_, uint256[] vesting_` (public)

preview estimated rewards




*Parameters*  
- `module`: address of reward module

- `account`: bytes32 account of interest for preview

- `shares`: number of shares that would be unstaked

- `tokens_`: reward token addresses


*Returns*  
- rewards_ estimated reward balances

- vesting_ estimated time vesting coeffs weighted by rewards


****
<br>

**`unlockable`**`(address module, address token) → uint256` (public)

compute reward shares to be unlocked on the next update




*Parameters*  
- `module`: address of reward module

- `token`: address of reward token


*Returns*  
- estimated unlockable rewards


****
<br>

**`unlocked`**`(address module, address token) → uint256` (public)

compute effective unlocked rewards




*Parameters*  
- `module`: address of reward module

- `token`: address of reward token


*Returns*  
- estimated current unlocked rewards


****
<br>

**`rewardsPerStakedShare`**`(address module, address token) → uint256` (public)

compute effective rewards per staked share




*Parameters*  
- `module`: module contract address

- `token`: address of reward token


*Returns*  
- estimated rewards per staked share



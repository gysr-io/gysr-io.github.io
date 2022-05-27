---
layout: page
title: IRewardModule
description: "this contract defines the common interface that any reward module
must implement to be compatible with the modular Pool architecture."
permalink: /docs/IRewardModule/
exclude: true
categories: [contract]
---

Reward module interface



**`IRewardModule`**

this contract defines the common interface that any reward module
must implement to be compatible with the modular Pool architecture.







****
<br>

**`tokens`**`() → address[]` (external)






*Returns*  
- array of reward tokens


****
<br>

**`balances`**`() → uint256[]` (external)






*Returns*  
- array of reward token balances


****
<br>

**`usage`**`() → uint256` (external)






*Returns*  
- GYSR usage ratio for reward module


****
<br>

**`factory`**`() → address` (external)






*Returns*  
- address of module factory


****
<br>

**`stake`**`(address account, address user, uint256 shares, bytes data) → uint256, uint256` (external)

perform any necessary accounting for new stake




*Parameters*  
- `account`: address of staking account

- `user`: address of user

- `shares`: number of new shares minted

- `data`: addtional data


*Returns*  
- amount of gysr spent

- amount of gysr vested


****
<br>

**`unstake`**`(address account, address user, uint256 shares, bytes data) → uint256, uint256` (external)

reward user and perform any necessary accounting for unstake




*Parameters*  
- `account`: address of staking account

- `user`: address of user

- `shares`: number of shares burned

- `data`: additional data


*Returns*  
- amount of gysr spent

- amount of gysr vested


****
<br>

**`claim`**`(address account, address user, uint256 shares, bytes data) → uint256, uint256` (external)

reward user and perform and necessary accounting for existing stake




*Parameters*  
- `account`: address of staking account

- `user`: address of user

- `shares`: number of shares being claimed against

- `data`: addtional data


*Returns*  
- amount of gysr spent

- amount of gysr vested


****
<br>

**`update`**`(address user)` (external)

method called by anyone to update accounting


will only be called ad hoc and should not contain essential logic

*Parameters*  
- `user`: address of user for update




****
<br>

**`clean`**`()` (external)

method called by owner to clean up and perform additional accounting


will only be called ad hoc and should not contain any essential logic





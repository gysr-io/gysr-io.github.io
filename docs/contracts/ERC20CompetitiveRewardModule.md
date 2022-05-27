---
layout: page
title: ERC20CompetitiveRewardModule
description: "this reward module distributes a single ERC20 token as the staking reward.
It is designed to offer competitive and engaging reward mechanics.

"
permalink: /docs/ERC20CompetitiveRewardModule/
exclude: true
categories: [contract]
---

ERC20 competitive reward module



**`ERC20CompetitiveRewardModule`**

this reward module distributes a single ERC20 token as the staking reward.
It is designed to offer competitive and engaging reward mechanics.



share seconds are the primary unit of accounting in this module. They
are accrued over time and burned during reward distribution. Users can
earn a time multiplier as an incentive for longer term staking. They can
also receive a GYSR multiplier by spending GYSR at the time of unstaking.

h/t https://github.com/ampleforth/token-geyser





****
<br>

**`constructor`**`(address token_, uint256 bonusMin_, uint256 bonusMax_, uint256 bonusPeriod_, address factory_)` (public)





*Parameters*  
- `token_`: the token that will be rewarded

- `bonusMin_`: initial time bonus

- `bonusMax_`: maximum time bonus

- `bonusPeriod_`: period (in seconds) over which time bonus grows to max

- `factory_`: address of module factory



****
<br>

**`tokens`**`() → address[] tokens_` (external)






*Returns*  
- array of reward tokens


****
<br>

**`balances`**`() → uint256[] balances_` (external)






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

**`stake`**`(address account, address, uint256 shares, bytes) → uint256, uint256` (external)

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

**`claim`**`(address account, address user, uint256 shares, bytes data) → uint256 spent, uint256 vested` (external)

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

**`update`**`(address)` (external)

method called by anyone to update accounting


will only be called ad hoc and should not contain essential logic

*Parameters*  
- `user`: address of user for update




****
<br>

**`clean`**`()` (external)

method called by owner to clean up and perform additional accounting


will only be called ad hoc and should not contain any essential logic




****
<br>

**`fund`**`(uint256 amount, uint256 duration)` (external)

fund module by locking up reward tokens for distribution




*Parameters*  
- `amount`: number of reward tokens to lock up as funding

- `duration`: period (seconds) over which funding will be unlocked



****
<br>

**`fund`**`(uint256 amount, uint256 duration, uint256 start)` (external)

fund module by locking up reward tokens for distribution




*Parameters*  
- `amount`: number of reward tokens to lock up as funding

- `duration`: period (seconds) over which funding will be unlocked

- `start`: time (seconds) at which funding begins to unlock



****
<br>

**`timeBonus`**`(uint256 time) → uint256` (public)

compute time bonus earned as a function of staking time




*Parameters*  
- `time`: length of time for which the tokens have been staked


*Returns*  
- bonus multiplier for time


****
<br>

**`totalLocked`**`() → uint256` (public)






*Returns*  
- total number of locked reward tokens


****
<br>

**`totalUnlocked`**`() → uint256` (public)






*Returns*  
- total number of unlocked reward tokens


****
<br>

**`stakeCount`**`(address addr) → uint256` (public)





*Parameters*  
- `addr`: address of interest


*Returns*  
- number of active stakes for user



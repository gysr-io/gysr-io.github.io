---
layout: page
title: ERC20FriendlyRewardModule
description: "this reward module distributes a single ERC20 token as the staking reward.
It is designed to offer simple and predictable reward mechanics.

"
permalink: /docs/ERC20FriendlyRewardModule/
exclude: true
categories: [contract]
---

### ERC20 friendly reward module



`ERC20FriendlyRewardModule`

this reward module distributes a single ERC20 token as the staking reward.
It is designed to offer simple and predictable reward mechanics.



rewards are immutable once earned, and can be claimed by the user at
any time. The module can be configured with a linear vesting schedule to
incentivize longer term staking. The user can spend GYSR at the time of
staking to receive a multiplier on their earning rate.



****

`constructor(address token_, uint256 vestingStart_, uint256 vestingPeriod_, address factory_)` (public)





**Parameters**  
- `token_`: the token that will be rewarded

- `vestingStart_`: minimum ratio earned

- `vestingPeriod_`: period (in seconds) over which investors vest to 100%

- `factory_`: address of module factory

**Returns**


****

`tokens() → address[] tokens_` (external)





**Parameters**  

**Returns**
- array of reward tokens


****

`factory() → address` (external)





**Parameters**  

**Returns**
- address of module factory


****

`balances() → uint256[] balances_` (external)





**Parameters**  

**Returns**
- array of reward token balances


****

`usage() → uint256` (external)





**Parameters**  

**Returns**
- GYSR usage ratio for reward module


****

`stake(address account, address user, uint256 shares, bytes data) → uint256, uint256` (external)

perform any necessary accounting for new stake




**Parameters**  
- `account`: address of staking account

- `user`: address of user

- `shares`: number of new shares minted

- `data`: addtional data


**Returns**
- amount of gysr spent

- amount of gysr vested


****

`_stake(address account, address user, uint256 shares, bytes data) → uint256, uint256` (internal)

internal implementation of stake method




**Parameters**  
- `account`: address of staking account

- `user`: address of user

- `shares`: number of new shares minted

- `data`: addtional data


**Returns**
- amount of gysr spent

- amount of gysr vested


****

`unstake(address account, address user, uint256 shares, bytes) → uint256, uint256` (external)

reward user and perform any necessary accounting for unstake




**Parameters**  
- `account`: address of staking account

- `user`: address of user

- `shares`: number of shares burned

- `data`: additional data


**Returns**
- amount of gysr spent

- amount of gysr vested


****

`_unstake(address account, address user, uint256 shares) → uint256, uint256` (internal)

internal implementation of unstake




**Parameters**  
- `account`: address of staking account

- `user`: address of user

- `shares`: number of shares burned


**Returns**
- amount of gysr spent

- amount of gysr vested


****

`claim(address account, address user, uint256 shares, bytes data) → uint256 spent, uint256 vested` (external)

reward user and perform and necessary accounting for existing stake




**Parameters**  
- `account`: address of staking account

- `user`: address of user

- `shares`: number of shares being claimed against

- `data`: addtional data


**Returns**
- amount of gysr spent

- amount of gysr vested


****

`_rewardForStakedShares(uint256 shares, uint256 bonus, uint256 rewardTally) → uint256` (internal)



compute rewards owed for a specific stake


**Parameters**  
- `shares`: number of shares to calculate rewards for

- `bonus`: associated bonus for this stake

- `rewardTally`: associated rewardTally for this stake


**Returns**
- reward for these staked shares


****

`timeVestingCoefficient(uint256 time) → uint256` (public)

compute vesting multiplier as function of staking time




**Parameters**  
- `time`: epoch time at which the tokens were staked


**Returns**
- vesting multiplier rewards


****

`update(address)` (external)

method called by anyone to update accounting


will only be called ad hoc and should not contain essential logic

**Parameters**  
- `user`: address of user for update


**Returns**


****

`clean()` (external)

method called ad hoc to clean up and perform additional accounting


will only be called manually, and should not contain any essential logic

**Parameters**  

**Returns**


****

`fund(uint256 amount, uint256 duration)` (external)

fund Geyser by locking up reward tokens for distribution




**Parameters**  
- `amount`: number of reward tokens to lock up as funding

- `duration`: period (seconds) over which funding will be unlocked

**Returns**


****

`fund(uint256 amount, uint256 duration, uint256 start)` (external)

fund Geyser by locking up reward tokens for distribution




**Parameters**  
- `amount`: number of reward tokens to lock up as funding

- `duration`: period (seconds) over which funding will be unlocked

- `start`: time (seconds) at which funding begins to unlock

**Returns**


****

`totalLocked() → uint256` (public)





**Parameters**  

**Returns**
- total number of locked reward tokens


****

`totalUnlocked() → uint256` (public)





**Parameters**  

**Returns**
- total number of unlocked reward tokens


****

`stakeCount(address addr) → uint256` (public)





**Parameters**  
- `addr`: address of interest


**Returns**
- number of active stakes for user



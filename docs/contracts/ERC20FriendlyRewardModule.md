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

ERC20 friendly reward module



**`ERC20FriendlyRewardModule`**

this reward module distributes a single ERC20 token as the staking reward.
It is designed to offer simple and predictable reward mechanics.



rewards are immutable once earned, and can be claimed by the user at
any time. The module can be configured with a linear vesting schedule to
incentivize longer term staking. The user can spend GYSR at the time of
staking to receive a multiplier on their earning rate.





****
<br>

**`constructor`**`(address token_, uint256 vestingStart_, uint256 vestingPeriod_, address config_, address factory_)` (public)





*Parameters*  
- `token_`: the token that will be rewarded

- `vestingStart_`: minimum ratio earned

- `vestingPeriod_`: period (in seconds) over which investors vest to 100%

- `config_`: address for configuration contract

- `factory_`: address of module factory



****
<br>

**`tokens`**`() → address[] tokens_` (external)






*Returns*  
- array of reward tokens


****
<br>

**`factory`**`() → address` (external)






*Returns*  
- address of module factory


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

**`stake`**`(bytes32 account, address sender, uint256 shares, bytes data) → uint256, uint256` (external)

perform any necessary accounting for new stake




*Parameters*  
- `account`: bytes32 id of staking account

- `sender`: address of sender

- `shares`: number of new shares minted

- `data`: addtional data


*Returns*  
- amount of gysr spent

- amount of gysr vested


****
<br>

**`_stake`**`(bytes32 account, address sender, uint256 shares, bytes data) → uint256, uint256` (internal)

internal implementation of stake method




*Parameters*  
- `account`: bytes32 id of staking account

- `sender`: address of sender

- `shares`: number of new shares minted

- `data`: addtional data


*Returns*  
- amount of gysr spent

- amount of gysr vested


****
<br>

**`unstake`**`(bytes32 account, address sender, address receiver, uint256 shares, bytes) → uint256, uint256` (external)

reward user and perform any necessary accounting for unstake




*Parameters*  
- `account`: bytes32 id of staking account

- `sender`: address of sender

- `receiver`: address of reward receiver

- `shares`: number of shares burned

- `data`: additional data


*Returns*  
- amount of gysr spent

- amount of gysr vested


****
<br>

**`_unstake`**`(bytes32 account, address sender, address receiver, uint256 shares) → uint256, uint256` (internal)

internal implementation of unstake




*Parameters*  
- `account`: bytes32 of staking account

- `sender`: address of sender

- `receiver`: address of reward receiver

- `shares`: number of shares burned


*Returns*  
- amount of gysr spent

- amount of gysr vested


****
<br>

**`claim`**`(bytes32 account, address sender, address receiver, uint256 shares, bytes data) → uint256 spent, uint256 vested` (external)

reward user and perform and necessary accounting for existing stake




*Parameters*  
- `account`: bytes32 id of staking account

- `sender`: address of sender

- `receiver`: address of reward receiver

- `shares`: number of shares being claimed against

- `data`: additional data


*Returns*  
- amount of gysr spent

- amount of gysr vested


****
<br>

**`_rewardForStakedShares`**`(uint256 shares, uint256 bonus, uint256 rewardTally) → uint256` (internal)



compute rewards owed for a specific stake


*Parameters*  
- `shares`: number of shares to calculate rewards for

- `bonus`: associated bonus for this stake

- `rewardTally`: associated rewardTally for this stake


*Returns*  
- reward for these staked shares


****
<br>

**`timeVestingCoefficient`**`(uint256 time) → uint256` (public)

compute vesting multiplier as function of staking time




*Parameters*  
- `time`: epoch time at which the tokens were staked


*Returns*  
- vesting multiplier rewards


****
<br>

**`update`**`(bytes32, address, bytes)` (external)

method called by anyone to update accounting


will only be called ad hoc and should not contain essential logic


*Parameters*  
- `account`: bytes32 id of staking account for update

- `sender`: address of sender

- `data`: additional data



****
<br>

**`clean`**`(bytes)` (external)

method called ad hoc to clean up and perform additional accounting


will only be called manually, and should not contain any essential logic




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

**`stakeCount`**`(bytes32 account) → uint256` (public)





*Parameters*  
- `account`: bytes32 id for account of interest


*Returns*  
- number of active stakes for user



---
layout: page
title: ERC20MultiRewardModule
description: "this reward module distributes multiple ERC20 token as the staking reward.
It is designed to offer simple and flexible reward mechanics.

"
permalink: /docs/ERC20MultiRewardModule/
exclude: true
categories: [contract]
---

ERC20 multi reward module



**`ERC20MultiRewardModule`**

this reward module distributes multiple ERC20 token as the staking reward.
It is designed to offer simple and flexible reward mechanics.



each reward token is opt-in and must be specified during user operations.
Rewards are immutable once earned, and can be claimed by the user at
any time. The module can be configured with a linear vesting schedule to
incentivize longer term staking.





****
<br>

**`constructor`**`(uint256 vestingStart_, uint256 vestingPeriod_, address config_, address factory_)` (public)





*Parameters*  
- `vestingStart_`: minimum vesting portion earned

- `vestingPeriod_`: period (in seconds) over which user positions fully vest

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

**`stake`**`(bytes32 account, address, uint256 shares, bytes data) → uint256, uint256` (external)

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

**`unstake`**`(bytes32 account, address, address receiver, uint256 shares, bytes data) → uint256, uint256` (external)

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

**`claim`**`(bytes32 account, address, address receiver, uint256, bytes data) → uint256, uint256` (external)

reward user and perform and necessary accounting for existing stake


claim rewards on specified tokens, optionally specify stakes, and optionally deregister


*Parameters*  
- `data`: (bool continue, uint256 start, uint256 end, address[] tokens)

*Returns*  
- amount of gysr spent

- amount of gysr vested


****
<br>

**`update`**`(bytes32 account, address, bytes data)` (external)

method called by anyone to update accounting


register for specified rewards token on existing stake


*Parameters*  
- `uint256`: start, uint256 end, address[] tokens)



****
<br>

**`clean`**`(bytes data)` (external)

method called ad hoc to clean up and perform additional accounting


will only be called manually, and should not contain any essential logic




****
<br>

**`fund`**`(address token, uint256 amount, uint256 duration)` (external)

fund module by locking up reward tokens for distribution




*Parameters*  
- `token`: address of reward token

- `amount`: number of reward tokens to lock up as funding

- `duration`: period (seconds) over which funding will be unlocked



****
<br>

**`fund`**`(address token, uint256 amount, uint256 duration, uint256 start)` (external)

fund module by locking up reward tokens for distribution




*Parameters*  
- `token`: address of reward token

- `amount`: number of reward tokens to lock up as funding

- `duration`: period (seconds) over which funding will be unlocked

- `start`: time (seconds) at which funding begins to unlock



****
<br>

**`tokenCount`**`() → uint256` (public)



helper to get module reward token count



*Returns*  
- number of reward tokens


****
<br>

**`stakeCount`**`(bytes32 account) → uint256` (public)



helper to get user stake count


*Parameters*  
- `account`: bytes32 id for account of interest


*Returns*  
- number of active stakes for user


****
<br>

**`stakeRegistered`**`(bytes32 account, uint256 index, address token) → uint256` (public)



helper to get nested rewards accumulator data


*Parameters*  
- `account`: bytes32 id for account of interest

- `index`: array index of stake

- `token`: address of reward token




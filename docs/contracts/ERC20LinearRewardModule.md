---
layout: page
title: ERC20LinearRewardModule
description: "this reward module distributes a single ERC20 token at a continuous fixed rate.

"
permalink: /docs/ERC20LinearRewardModule/
exclude: true
categories: [contract]
---

ERC20 linear reward module



**`ERC20LinearRewardModule`**

this reward module distributes a single ERC20 token at a continuous fixed rate.



the linear reward module provides a guarantee that a constant reward rate
will be earned over a specified time period. This can be used to create
incentive mechanisms such as streaming payroll, equity vesting, fixed rate
yield farms, and more.





****
<br>

**`constructor`**`(address token_, uint256 period_, uint256 rate_, address config_, address factory_)` (public)





*Parameters*  
- `token_`: the token that will be rewarded

- `period_`: time period (seconds)

- `rate_`: constant reward rate (shares / share second)

- `config_`: address for configuration contract

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

**`stake`**`(bytes32 account, address, uint256 shares, bytes) → uint256, uint256` (external)

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

**`unstake`**`(bytes32 account, address, address receiver, uint256 shares, bytes) → uint256, uint256` (external)

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

**`claim`**`(bytes32 account, address, address receiver, uint256, bytes) → uint256, uint256` (external)

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

method called by owner to clean up and perform additional accounting


will only be called ad hoc and should not contain any essential logic


*Parameters*  
- `data`: additional data



****
<br>

**`fund`**`(uint256 amount)` (external)

fund module by depositing reward tokens


this is a public method callable by any account or contract


*Parameters*  
- `amount`: number of reward tokens to deposit



****
<br>

**`withdraw`**`(uint256 amount)` (external)

withdraw uncommited reward tokens from module




*Parameters*  
- `amount`: number of reward tokens to withdraw




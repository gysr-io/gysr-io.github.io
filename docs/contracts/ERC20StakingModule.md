---
layout: page
title: ERC20StakingModule
description: "this staking module allows users to deposit an amount of ERC20 token
in exchange for shares credited to their address. When the user
unstakes, these shares will be burned and a reward will be distributed."
permalink: /docs/ERC20StakingModule/
exclude: true
categories: [contract]
---

ERC20 staking module



**`ERC20StakingModule`**

this staking module allows users to deposit an amount of ERC20 token
in exchange for shares credited to their address. When the user
unstakes, these shares will be burned and a reward will be distributed.







****
<br>

**`constructor`**`(address token_, address factory_)` (public)





*Parameters*  
- `token_`: the token that will be staked

- `factory_`: address of module factory



****
<br>

**`tokens`**`() → address[] tokens_` (external)






*Returns*  
- array of staking tokens


****
<br>

**`balances`**`(address user) → uint256[] balances_` (external)

get balance of user




*Parameters*  
- `user`: address of user


*Returns*  
- balances of each staking token


****
<br>

**`factory`**`() → address` (external)






*Returns*  
- address of module factory


****
<br>

**`totals`**`() → uint256[] totals_` (external)

get total staked amount





*Returns*  
- totals for each staking token


****
<br>

**`stake`**`(address sender, uint256 amount, bytes data) → bytes32, uint256` (external)

stake an amount of tokens for user




*Parameters*  
- `sender`: address of sender

- `amount`: number of tokens to stake

- `data`: additional data


*Returns*  
- bytes32 id of staking account

- number of shares minted for stake


****
<br>

**`unstake`**`(address sender, uint256 amount, bytes data) → bytes32, address, uint256` (external)

unstake an amount of tokens for user




*Parameters*  
- `sender`: address of sender

- `amount`: number of tokens to unstake

- `data`: additional data


*Returns*  
- bytes32 id of staking account

- address of reward receiver

- number of shares burned for unstake


****
<br>

**`claim`**`(address sender, uint256 amount, bytes data) → bytes32, address, uint256` (external)

quote the share value for an amount of tokens without unstaking




*Parameters*  
- `sender`: address of sender

- `amount`: number of tokens to claim with

- `data`: additional data


*Returns*  
- bytes32 id of staking account

- address of reward receiver

- number of shares that the claim amount is worth


****
<br>

**`update`**`(address sender, bytes data) → bytes32` (external)

method called by anyone to update accounting


will only be called ad hoc and should not contain essential logic


*Parameters*  
- `sender`: address of user for update

- `data`: additional data


*Returns*  
- bytes32 id of staking account


****
<br>

**`clean`**`(bytes)` (external)

method called by owner to clean up and perform additional accounting


will only be called ad hoc and should not contain any essential logic


*Parameters*  
- `data`: additional data



****
<br>

**`approve`**`(address operator, bool value)` (external)

set approval for operators to act on user position




*Parameters*  
- `operator`: address of operator

- `value`: boolean to grant or revoke approval



****
<br>

*Events*  


`Approval(address user, address operator, bool value)`






---
layout: page
title: IStakingModule
description: "this contract defines the common interface that any staking module
must implement to be compatible with the modular Pool architecture."
permalink: /docs/IStakingModule/
exclude: true
categories: [contract]
---

Staking module interface



**`IStakingModule`**

this contract defines the common interface that any staking module
must implement to be compatible with the modular Pool architecture.







****
<br>

**`tokens`**`() → address[]` (external)






*Returns*  
- array of staking tokens


****
<br>

**`balances`**`(address user) → uint256[]` (external)

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

**`totals`**`() → uint256[]` (external)

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

**`clean`**`(bytes data)` (external)

method called by owner to clean up and perform additional accounting


will only be called ad hoc and should not contain any essential logic


*Parameters*  
- `data`: additional data




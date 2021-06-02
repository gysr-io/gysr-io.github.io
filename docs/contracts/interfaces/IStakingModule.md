---
layout: page
title: IStakingModule
description: "this contract defines the common interface that any staking module
must implement to be compatible with the modular Pool architecture."
permalink: /docs/IStakingModule/
exclude: true
categories: [contract]
---

### Staking module interface



`IStakingModule`

this contract defines the common interface that any staking module
must implement to be compatible with the modular Pool architecture.





****

`tokens() → address[]` (external)





**Parameters**  

**Returns**
- array of staking tokens


****

`balances(address user) → uint256[]` (external)

get balance of user




**Parameters**  
- `user`: address of user


**Returns**
- balances of each staking token


****

`factory() → address` (external)





**Parameters**  

**Returns**
- address of module factory


****

`totals() → uint256[]` (external)

get total staked amount




**Parameters**  

**Returns**
- totals for each staking token


****

`stake(address user, uint256 amount, bytes data) → address, uint256` (external)

stake an amount of tokens for user




**Parameters**  
- `user`: address of user

- `amount`: number of tokens to stake

- `data`: additional data


**Returns**
- address of staking account

- number of shares minted for stake


****

`unstake(address user, uint256 amount, bytes data) → address, uint256` (external)

unstake an amount of tokens for user




**Parameters**  
- `user`: address of user

- `amount`: number of tokens to unstake

- `data`: additional data


**Returns**
- address of staking account

- number of shares burned for unstake


****

`claim(address user, uint256 amount, bytes data) → address, uint256` (external)

quote the share value for an amount of tokens without unstaking




**Parameters**  
- `user`: address of user

- `amount`: number of tokens to claim with

- `data`: additional data


**Returns**
- address of staking account

- number of shares that the claim amount is worth


****

`update(address user)` (external)

method called by anyone to update accounting


will only be called ad hoc and should not contain essential logic

**Parameters**  
- `user`: address of user for update


**Returns**


****

`clean()` (external)

method called by owner to clean up and perform additional accounting


will only be called ad hoc and should not contain any essential logic

**Parameters**  

**Returns**



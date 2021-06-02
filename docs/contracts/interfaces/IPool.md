---
layout: page
title: IPool
description: "this defines the core Pool contract interface"
permalink: /docs/IPool/
exclude: true
categories: [contract]
---

### Pool interface



`IPool`

this defines the core Pool contract interface





****

`stakingTokens() → address[]` (external)





**Parameters**  

**Returns**
- staking tokens for Pool


****

`rewardTokens() → address[]` (external)





**Parameters**  

**Returns**
- reward tokens for Pool


****

`stakingBalances(address user) → uint256[]` (external)





**Parameters**  

**Returns**
- staking balances for user


****

`stakingTotals() → uint256[]` (external)





**Parameters**  

**Returns**
- total staking balances for Pool


****

`rewardBalances() → uint256[]` (external)





**Parameters**  

**Returns**
- reward balances for Pool


****

`usage() → uint256` (external)





**Parameters**  

**Returns**
- GYSR usage ratio for Pool


****

`stakingModule() → address` (external)





**Parameters**  

**Returns**
- address of staking module


****

`rewardModule() → address` (external)





**Parameters**  

**Returns**
- address of reward module


****

`stake(uint256 amount, bytes stakingdata, bytes rewarddata)` (external)

stake asset and begin earning rewards




**Parameters**  
- `amount`: number of tokens to unstake

- `stakingdata`: data passed to staking module

- `rewarddata`: data passed to reward module

**Returns**


****

`unstake(uint256 amount, bytes stakingdata, bytes rewarddata)` (external)

unstake asset and claim rewards




**Parameters**  
- `amount`: number of tokens to unstake

- `stakingdata`: data passed to staking module

- `rewarddata`: data passed to reward module

**Returns**


****

`claim(uint256 amount, bytes stakingdata, bytes rewarddata)` (external)

claim rewards without unstaking




**Parameters**  
- `amount`: number of tokens to claim against

- `stakingdata`: data passed to staking module

- `rewarddata`: data passed to reward module

**Returns**


****

`update()` (external)

method called ad hoc to update user accounting



**Parameters**  

**Returns**


****

`clean()` (external)

method called ad hoc to clean up and perform additional accounting



**Parameters**  

**Returns**


****

`gysrBalance() → uint256` (external)





**Parameters**  

**Returns**
- gysr balance available for withdrawal


****

`withdraw(uint256 amount)` (external)

withdraw GYSR tokens applied during unstaking




**Parameters**  
- `amount`: number of GYSR to withdraw

**Returns**



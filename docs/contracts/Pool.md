---
layout: page
title: Pool
description: "this implements the GYSR core Pool contract. It supports generalized
incentive mechanisms through a modular architecture, where
staking and reward logic is contained in child contracts."
permalink: /docs/Pool/
exclude: true
categories: [contract]
---

Pool



**`Pool`**

this implements the GYSR core Pool contract. It supports generalized
incentive mechanisms through a modular architecture, where
staking and reward logic is contained in child contracts.







****
<br>

**`constructor`**`(address staking_, address reward_, address gysr_, address factory_)` (public)





*Parameters*  
- `staking_`: the staking module address

- `reward_`: the reward module address

- `gysr_`: address for GYSR token

- `factory_`: address for parent factory



****
<br>

**`stakingTokens`**`() → address[]` (external)






*Returns*  
- staking tokens for Pool


****
<br>

**`rewardTokens`**`() → address[]` (external)






*Returns*  
- reward tokens for Pool


****
<br>

**`stakingBalances`**`(address user) → uint256[]` (external)






*Returns*  
- staking balances for user


****
<br>

**`stakingTotals`**`() → uint256[]` (external)






*Returns*  
- total staking balances for Pool


****
<br>

**`rewardBalances`**`() → uint256[]` (external)






*Returns*  
- reward balances for Pool


****
<br>

**`usage`**`() → uint256` (external)






*Returns*  
- GYSR usage ratio for Pool


****
<br>

**`stakingModule`**`() → address` (external)






*Returns*  
- address of staking module


****
<br>

**`rewardModule`**`() → address` (external)






*Returns*  
- address of reward module


****
<br>

**`stake`**`(uint256 amount, bytes stakingdata, bytes rewarddata)` (external)

stake asset and begin earning rewards




*Parameters*  
- `amount`: number of tokens to stake

- `stakingdata`: data passed to staking module

- `rewarddata`: data passed to reward module



****
<br>

**`unstake`**`(uint256 amount, bytes stakingdata, bytes rewarddata)` (external)

unstake asset and claim rewards




*Parameters*  
- `amount`: number of tokens to unstake

- `stakingdata`: data passed to staking module

- `rewarddata`: data passed to reward module



****
<br>

**`claim`**`(uint256 amount, bytes stakingdata, bytes rewarddata)` (external)

claim rewards without unstaking




*Parameters*  
- `amount`: number of tokens to claim against

- `stakingdata`: data passed to staking module

- `rewarddata`: data passed to reward module



****
<br>

**`update`**`()` (external)

method called ad hoc to update user accounting






****
<br>

**`clean`**`()` (external)

method called ad hoc to clean up and perform additional accounting






****
<br>

**`gysrBalance`**`() → uint256` (external)






*Returns*  
- gysr balance available for withdrawal


****
<br>

**`withdraw`**`(uint256 amount)` (external)

withdraw GYSR tokens applied during unstaking




*Parameters*  
- `amount`: number of GYSR to withdraw



****
<br>

**`transferControl`**`(address newController)` (public)

transfer control of the Pool and modules to another account




*Parameters*  
- `newController`: address of new controller




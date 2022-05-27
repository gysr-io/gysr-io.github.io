---
layout: page
title: ERC721StakingModule
description: "this staking module allows users to deposit one or more ERC721
tokens in exchange for shares credited to their address. When the user
unstakes, these shares will be burned and a reward will be distributed."
permalink: /docs/ERC721StakingModule/
exclude: true
categories: [contract]
---

ERC721 staking module



**`ERC721StakingModule`**

this staking module allows users to deposit one or more ERC721
tokens in exchange for shares credited to their address. When the user
unstakes, these shares will be burned and a reward will be distributed.







****
<br>

**`constructor`**`(address token_, address factory_)` (public)





*Parameters*  
- `token_`: the token that will be rewarded

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

**`stake`**`(address user, uint256 amount, bytes data) → address, uint256` (external)

stake an amount of tokens for user




*Parameters*  
- `user`: address of user

- `amount`: number of tokens to stake

- `data`: additional data


*Returns*  
- address of staking account

- number of shares minted for stake


****
<br>

**`unstake`**`(address user, uint256 amount, bytes data) → address, uint256` (external)

unstake an amount of tokens for user




*Parameters*  
- `user`: address of user

- `amount`: number of tokens to unstake

- `data`: additional data


*Returns*  
- address of staking account

- number of shares burned for unstake


****
<br>

**`claim`**`(address user, uint256 amount, bytes) → address, uint256` (external)

quote the share value for an amount of tokens without unstaking




*Parameters*  
- `user`: address of user

- `amount`: number of tokens to claim with

- `data`: additional data


*Returns*  
- address of staking account

- number of shares that the claim amount is worth


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





---
layout: page
title: ERC20BondStakingModule
description: "this staking module allows users to permanently sell an ERC20 token
in exchange for bond shares credited to their address. When the user
unstakes, these shares will be burned and a reward will be distributed."
permalink: /docs/ERC20BondStakingModule/
exclude: true
categories: [contract]
---

ERC20 bond staking module



**`ERC20BondStakingModule`**

this staking module allows users to permanently sell an ERC20 token
in exchange for bond shares credited to their address. When the user
unstakes, these shares will be burned and a reward will be distributed.







****
<br>

**`constructor`**`(uint256 period_, bool burndown_, address config_, address factory_)` (public)





*Parameters*  
- `period_`: bond vesting period

- `burndown_`: enable burndown period and opt-out for deposited user funds

- `config_`: address for configuration contract

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


user balances will dynamically decrease as bonds vest to reflect
the amount that can actually be withdrawn

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


pass amount zero to unstake all or to unstake fully vested bond

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

**`claim`**`(address sender, uint256, bytes data) → bytes32, address, uint256` (external)

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

**`open`**`(address token, uint256 price, uint256 coeff, uint256 max, uint256 capacity)` (external)

open a new bond market




*Parameters*  
- `token`: the principal token that will be deposited

- `price`: minimum and starting price of the bond in tokens

- `coeff`: bond pricing coefficient

- `max`: maximum size for an individual bond in debt shares

- `capacity`: the total debt available for this market in shares



****
<br>

**`close`**`(address token)` (external)

close an existing bond market




*Parameters*  
- `token`: the token address of the market to close



****
<br>

**`adjust`**`(address token, uint256 price, uint256 coeff, uint256 max, uint256 capacity)` (external)

adjust the configuration of an existing bond market




*Parameters*  
- `token`: the token address of the market to adjust

- `price`: minimum and starting price of the bond in tokens

- `coeff`: bond pricing coefficient

- `max`: maximum size for an individual bond in debt shares

- `capacity`: the total debt available for this market in shares



****
<br>

**`withdraw`**`(address token, uint256 amount)` (external)

withdraw vested principal token from market




*Parameters*  
- `token`: the principal token address

- `amount`: number of tokens to withdraw



****
<br>

**`tokenURI`**`(uint256 tokenId) → string` (public)



Returns the Uniform Resource Identifier (URI) for `tokenId` token.




****
<br>

**`_beforeTokenTransfer`**`(address from, address to, uint256 tokenId, uint256)` (internal)








****
<br>

*Events*  


`MarketOpened(address token, uint256 price, uint256 coeff, uint256 max, uint256 capacity)`






`MarketClosed(address token)`






`MarketAdjusted(address token, uint256 price, uint256 coeff, uint256 max, uint256 capacity)`






`MarketBalanceWithdrawn(address token, uint256 amount)`






---
layout: page
title: ERC20BondStakingModuleInfo
description: "this library provides read-only convenience functions to query
additional information about the ERC20BondStakingModule contract."
permalink: /docs/ERC20BondStakingModuleInfo/
exclude: true
categories: [contract]
---

ERC20 bond staking module info library



**`ERC20BondStakingModuleInfo`**

this library provides read-only convenience functions to query
additional information about the ERC20BondStakingModule contract.







****
<br>

**`tokens`**`(address module) → address[] addresses_, string[] names_, string[] symbols_, uint8[] decimals_` (external)

convenience function to get all token metadata in a single call




*Parameters*  
- `module`: address of reward module




****
<br>

**`positions`**`(address module, address addr, bytes data) → bytes32[] accounts_, uint256[] shares_` (external)

get all staking positions for user




*Parameters*  
- `module`: address of staking module

- `addr`: user address of interest

- `data`: additional encoded data




****
<br>

**`metadata`**`(address module, uint256 id, bytes) → string` (external)

provide the metadata URI for a bond position




*Parameters*  
- `module`: address of bond staking module

- `id`: bond position identifier



****
<br>

**`quote`**`(address module, address token, uint256 amount) → uint256, bool` (public)

quote the debt share values to be issued for an amount of tokens




*Parameters*  
- `module`: address of bond staking module

- `token`: address of market

- `amount`: number of tokens to be deposited


*Returns*  
- debt estimated debt shares issued

- okay if debt amount is within max size and capacity of market (note: this does not check reward module funding)


****
<br>

**`quote`**`(address module, address token, uint256 amount, address config) → uint256, bool` (external)

quote the debt share values to be issued for an amount of tokens after protocol fees




*Parameters*  
- `module`: address of bond staking module

- `token`: address of market

- `amount`: number of tokens to be deposited

- `config`: address of configuration contract


*Returns*  
- debt estimated debt shares issued

- okay if debt amount is within max size and capacity of market (note: this does not check reward module funding)


****
<br>

**`price`**`(address module, address token) → uint256` (public)

get current price of debt share (reward token) in specified principal token shares




*Parameters*  
- `module`: address of bond staking module

- `token`: address of market


*Returns*  
- price current price of reward debt share in principal token shares


****
<br>

**`unstakeable`**`(address module, uint256 id, uint256 amount) → uint256, uint256, bool` (external)

preview amount of deposit to be returned for an unstake




*Parameters*  
- `module`: address of bond staking module

- `id`: bond position identifier

- `amount`: number of tokens to be unstaked (pass 0 for all)


*Returns*  
- principal token amount returned

- debt shares to be redeemed (possibly not all vested)

- okay if unstake is valid for bond id and principal amount


****
<br>

**`withdrawable`**`(address module, address token) → uint256` (public)

get current vested balance of specified principal token




*Parameters*  
- `module`: address of bond staking module

- `token`: address of market


*Returns*  
- withdrawable amount of principal token



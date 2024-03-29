---
layout: page
title: ERC20BaseRewardModule
description: "this abstract class implements common ERC20 funding and unlocking
logic, which is inherited by other reward modules."
permalink: /docs/ERC20BaseRewardModule/
exclude: true
categories: [contract]
---

ERC20 base reward module



**`ERC20BaseRewardModule`**

this abstract class implements common ERC20 funding and unlocking
logic, which is inherited by other reward modules.







****
<br>

**`totalShares`**`(address token) → uint256` (public)

getter for total token shares






****
<br>

**`lockedShares`**`(address token) → uint256` (public)

getter for total locked token shares






****
<br>

**`fundings`**`(address token, uint256 index) → uint256 amount, uint256 shares, uint256 locked, uint256 updated, uint256 start, uint256 duration` (public)

getter for funding schedule struct






****
<br>

**`fundingCount`**`(address token) → uint256` (public)





*Parameters*  
- `token`: contract address of reward token


*Returns*  
- number of active funding schedules


****
<br>

**`unlockable`**`(address token, uint256 idx) → uint256` (public)

compute number of unlockable shares for a specific funding schedule




*Parameters*  
- `token`: contract address of reward token

- `idx`: index of the funding


*Returns*  
- the number of unlockable shares


****
<br>

**`_fund`**`(address token, uint256 amount, uint256 duration, uint256 start, address feeReceiver, uint256 feeRate)` (internal)

fund pool by locking up reward tokens for future distribution




*Parameters*  
- `token`: contract address of reward token

- `amount`: number of reward tokens to lock up as funding

- `duration`: period (seconds) over which funding will be unlocked

- `start`: time (seconds) at which funding begins to unlock

- `feeReceiver`: address to receive funding fee

- `feeRate`: portion of funding amount to take as fee



****
<br>

**`_clean`**`(address token)` (internal)



internal function to clean up stale funding schedules


*Parameters*  
- `token`: contract address of reward token to clean up



****
<br>

**`_unlockTokens`**`(address token) → uint256 shares` (internal)



unlocks reward tokens based on funding schedules


*Parameters*  
- `token`: contract addres of reward token


*Returns*  
- shares number of shares unlocked


****
<br>

**`_distribute`**`(address user, address token, uint256 shares) → uint256 amount` (internal)



distribute reward tokens to user


*Parameters*  
- `user`: address of user receiving rweard

- `token`: contract address of reward token

- `shares`: number of shares to be distributed


*Returns*  
- amount number of reward tokens distributed



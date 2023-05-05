---
layout: page
title: TokenUtils
description: "this library implements utility methods for token handling,
dynamic balance accounting, and fee processing"
permalink: /docs/TokenUtils/
exclude: true
categories: [contract]
---

Token utilities



**`TokenUtils`**

this library implements utility methods for token handling,
dynamic balance accounting, and fee processing







****
<br>

**`getShares`**`(contract IERC20 token, uint256 total, uint256 amount) → uint256` (internal)

get token shares from amount




*Parameters*  
- `token`: erc20 token interface

- `total`: current total shares

- `amount`: balance of tokens



****
<br>

**`getAmount`**`(contract IERC20 token, uint256 total, uint256 shares) → uint256` (internal)

get token amount from shares




*Parameters*  
- `token`: erc20 token interface

- `total`: current total shares

- `shares`: balance of shares



****
<br>

**`receiveAmount`**`(contract IERC20 token, uint256 total, address sender, uint256 amount) → uint256` (internal)

transfer tokens from sender into contract and convert to shares
for internal accounting




*Parameters*  
- `token`: erc20 token interface

- `total`: current total shares

- `sender`: token sender

- `amount`: number of tokens to be sent



****
<br>

**`receiveWithFee`**`(contract IERC20 token, uint256 total, address sender, uint256 amount, address feeReceiver, uint256 feeRate) → uint256` (internal)

transfer tokens from sender into contract, process protocol fee,
and convert to shares for internal accounting




*Parameters*  
- `token`: erc20 token interface

- `total`: current total shares

- `sender`: token sender

- `amount`: number of tokens to be sent

- `feeReceiver`: address to receive fee

- `feeRate`: portion of amount to take as fee in 18 decimals



****
<br>

*Events*  


`Fee(address receiver, address token, uint256 amount)`






---
layout: page
title: TokenUtilsInfo
description: "this library implements utility methods for token handling,
dynamic balance accounting, and fee processing.

this is a modified version to be used by info libraries."
permalink: /docs/TokenUtilsInfo/
exclude: true
categories: [contract]
---

Token utilities info



**`TokenUtilsInfo`**

this library implements utility methods for token handling,
dynamic balance accounting, and fee processing.

this is a modified version to be used by info libraries.







****
<br>

**`getShares`**`(contract IERC20 token, address module, uint256 total, uint256 amount) → uint256` (internal)

get token shares from amount




*Parameters*  
- `token`: erc20 token interface

- `module`: address of module

- `total`: current total shares

- `amount`: balance of tokens



****
<br>

**`getAmount`**`(contract IERC20 token, address module, uint256 total, uint256 shares) → uint256` (internal)

get token amount from shares




*Parameters*  
- `token`: erc20 token interface

- `module`: address of module

- `total`: current total shares

- `shares`: balance of shares




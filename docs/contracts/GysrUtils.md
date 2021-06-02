---
layout: page
title: GysrUtils
description: "this library implements utility methods for the GYSR multiplier
and spending mechanics"
permalink: /docs/GysrUtils/
exclude: true
categories: [contract]
---

### GYSR utilities



`GysrUtils`

this library implements utility methods for the GYSR multiplier
and spending mechanics





****

`gysrBonus(uint256 gysr, uint256 amount, uint256 total, uint256 ratio) → uint256` (internal)

compute GYSR bonus as a function of usage ratio, stake amount,
and GYSR spent




**Parameters**  
- `gysr`: number of GYSR token applied to bonus

- `amount`: number of tokens or shares to unstake

- `total`: number of tokens or shares in overall pool

- `ratio`: usage ratio from 0 to 1


**Returns**
- multiplier value



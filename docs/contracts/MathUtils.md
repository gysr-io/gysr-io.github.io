---
layout: page
title: MathUtils
description: "this library implements various logarithmic math utilies which support
other contracts and specifically the GYSR multiplier calculation

"
permalink: /docs/MathUtils/
exclude: true
categories: [contract]
---

### Math utilities



`MathUtils`

this library implements various logarithmic math utilies which support
other contracts and specifically the GYSR multiplier calculation



h/t https://github.com/abdk-consulting/abdk-libraries-solidity



****

`logbase2(int128 x) → int128` (internal)

calculate binary logarithm of x





**Parameters**  
- `x`: signed 64.64-bit fixed point number, require x > 0


**Returns**
- signed 64.64-bit fixed point number


****

`ln(int128 x) → int128` (internal)

calculate natural logarithm of x


magic constant comes from ln(2) * 2^128 -> hex


**Parameters**  
- `x`: signed 64.64-bit fixed point number, require x > 0


**Returns**
- signed 64.64-bit fixed point number


****

`logbase10(int128 x) → int128` (internal)

calculate logarithm base 10 of x


magic constant comes from log10(2) * 2^128 -> hex


**Parameters**  
- `x`: signed 64.64-bit fixed point number, require x > 0


**Returns**
- signed 64.64-bit fixed point number


****

`testlogbase2(int128 x) → int128` (public)





**Parameters**  

**Returns**


****

`testlogbase10(int128 x) → int128` (public)





**Parameters**  

**Returns**



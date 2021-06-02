---
layout: page
title: PoolInfo
description: "this implements the Pool info library, which provides read-only
convenience functions to query additional information and metadata
about the core Pool contract."
permalink: /docs/PoolInfo/
exclude: true
categories: [contract]
---

### Pool info library



`PoolInfo`

this implements the Pool info library, which provides read-only
convenience functions to query additional information and metadata
about the core Pool contract.





****

`modules(address pool) → address, address, address, address` (public)

get information about the underlying staking and reward modules




**Parameters**  
- `pool`: address of Pool contract


**Returns**
- staking module address

- reward module address

- staking module type

- reward module type


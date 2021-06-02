---
layout: page
title: ERC20FriendlyRewardModuleFactory
description: "this factory contract handles deployment for the
ERC20FriendlyRewardModule contract

"
permalink: /docs/ERC20FriendlyRewardModuleFactory/
exclude: true
categories: [contract]
---

### ERC20 friendly reward module factory



`ERC20FriendlyRewardModuleFactory`

this factory contract handles deployment for the
ERC20FriendlyRewardModule contract



it is called by the parent PoolFactory and is responsible
for parsing constructor arguments before creating a new contract



****

`createModule(bytes data) → address` (external)

create a new Pool module




**Parameters**  
- `data`: binary encoded construction parameters


**Returns**
- address of newly created module



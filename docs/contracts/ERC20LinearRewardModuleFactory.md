---
layout: page
title: ERC20LinearRewardModuleFactory
description: "this factory contract handles deployment for the
ERC20LinearRewardModule contract

"
permalink: /docs/ERC20LinearRewardModuleFactory/
exclude: true
categories: [contract]
---

ERC20 linear reward module factory



**`ERC20LinearRewardModuleFactory`**

this factory contract handles deployment for the
ERC20LinearRewardModule contract



it is called by the parent PoolFactory and is responsible
for parsing constructor arguments before creating a new contract





****
<br>

**`createModule`**`(address config, bytes data) → address` (external)

create a new Pool module




*Parameters*  
- `config`: address for configuration contract

- `data`: binary encoded construction parameters


*Returns*  
- address of newly created module



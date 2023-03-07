---
layout: page
title: ERC20MultiRewardModuleFactory
description: "this factory contract handles deployment for the
ERC20MultiRewardModule contract

"
permalink: /docs/ERC20MultiRewardModuleFactory/
exclude: true
categories: [contract]
---

ERC20 multi reward module factory



**`ERC20MultiRewardModuleFactory`**

this factory contract handles deployment for the
ERC20MultiRewardModule contract



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



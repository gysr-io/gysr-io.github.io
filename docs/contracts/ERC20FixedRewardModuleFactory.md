---
layout: page
title: ERC20FixedRewardModuleFactory
description: "this factory contract handles deployment for the
ERC20FixedRewardModule contract

"
permalink: /docs/ERC20FixedRewardModuleFactory/
exclude: true
categories: [contract]
---

ERC20 fixed reward module factory



**`ERC20FixedRewardModuleFactory`**

this factory contract handles deployment for the
ERC20FixedRewardModule contract



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



---
layout: page
title: ERC20StakingModuleFactory
description: "this factory contract handles deployment for the
ERC20StakingModule contract

"
permalink: /docs/ERC20StakingModuleFactory/
exclude: true
categories: [contract]
---

ERC20 staking module factory



**`ERC20StakingModuleFactory`**

this factory contract handles deployment for the
ERC20StakingModule contract



it is called by the parent PoolFactory and is responsible
for parsing constructor arguments before creating a new contract





****
<br>

**`createModule`**`(address, bytes data) → address` (external)

create a new Pool module




*Parameters*  
- `config`: address for configuration contract

- `data`: binary encoded construction parameters


*Returns*  
- address of newly created module



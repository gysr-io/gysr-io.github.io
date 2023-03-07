---
layout: page
title: ERC20BondStakingModuleFactory
description: "this factory contract handles deployment for the
ERC20BondStakingModule contract

"
permalink: /docs/ERC20BondStakingModuleFactory/
exclude: true
categories: [contract]
---

ERC20 bond staking module factory



**`ERC20BondStakingModuleFactory`**

this factory contract handles deployment for the
ERC20BondStakingModule contract



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



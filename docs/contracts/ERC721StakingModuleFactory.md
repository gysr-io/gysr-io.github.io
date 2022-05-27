---
layout: page
title: ERC721StakingModuleFactory
description: "this factory contract handles deployment for the
ERC721StakingModule contract

"
permalink: /docs/ERC721StakingModuleFactory/
exclude: true
categories: [contract]
---

ERC721 staking module factory



**`ERC721StakingModuleFactory`**

this factory contract handles deployment for the
ERC721StakingModule contract



it is called by the parent PoolFactory and is responsible
for parsing constructor arguments before creating a new contract





****
<br>

**`createModule`**`(bytes data) → address` (external)

create a new Pool module




*Parameters*  
- `data`: binary encoded construction parameters


*Returns*  
- address of newly created module



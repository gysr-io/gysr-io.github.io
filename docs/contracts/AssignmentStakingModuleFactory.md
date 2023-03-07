---
layout: page
title: AssignmentStakingModuleFactory
description: "this factory contract handles deployment for the
AssignmentStakingModule contract

"
permalink: /docs/AssignmentStakingModuleFactory/
exclude: true
categories: [contract]
---

Assignment staking module factory



**`AssignmentStakingModuleFactory`**

this factory contract handles deployment for the
AssignmentStakingModule contract



it is called by the parent PoolFactory and is responsible
for parsing constructor arguments before creating a new contract





****
<br>

**`createModule`**`(address, bytes) → address` (external)

create a new Pool module




*Parameters*  
- `config`: address for configuration contract

- `data`: binary encoded construction parameters


*Returns*  
- address of newly created module



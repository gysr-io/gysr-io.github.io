---
layout: page
title: IModuleFactory
description: "this defines the common module factory interface used by the
main factory to create the staking and reward modules for a new Pool."
permalink: /docs/IModuleFactory/
exclude: true
categories: [contract]
---

Module factory interface



**`IModuleFactory`**

this defines the common module factory interface used by the
main factory to create the staking and reward modules for a new Pool.







****
<br>

**`createModule`**`(address config, bytes data) → address` (external)

create a new Pool module




*Parameters*  
- `config`: address for configuration contract

- `data`: binary encoded construction parameters


*Returns*  
- address of newly created module


****
<br>

*Events*  


`ModuleCreated(address user, address module)`






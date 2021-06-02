---
layout: page
title: IModuleFactory
description: "this defines the common module factory interface used by the
main factory to create the staking and reward modules for a new Pool."
permalink: /docs/IModuleFactory/
exclude: true
categories: [contract]
---

### Module factory interface



`IModuleFactory`

this defines the common module factory interface used by the
main factory to create the staking and reward modules for a new Pool.





****

`createModule(bytes data) → address` (external)

create a new Pool module




**Parameters**  
- `data`: binary encoded construction parameters


**Returns**
- address of newly created module



****

`ModuleCreated(address user, address module)`






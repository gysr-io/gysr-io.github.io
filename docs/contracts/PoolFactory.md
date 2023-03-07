---
layout: page
title: PoolFactory
description: "this implements the Pool factory contract which allows any user to
easily configure and deploy their own Pool

"
permalink: /docs/PoolFactory/
exclude: true
categories: [contract]
---

Pool factory



**`PoolFactory`**

this implements the Pool factory contract which allows any user to
easily configure and deploy their own Pool



it relies on a system of sub-factories which are responsible for the
creation of underlying staking and reward modules. This primary factory
calls each module factory and assembles the overall Pool contract.

this contract also manages the module factory whitelist.





****
<br>

**`constructor`**`(address gysr_, address config_)` (public)





*Parameters*  
- `gysr_`: address of GYSR token

- `config_`: address of configuration contract



****
<br>

**`create`**`(address staking, address reward, bytes stakingdata, bytes rewarddata) → address` (external)

create a new Pool




*Parameters*  
- `staking`: address of factory that will be used to create staking module

- `reward`: address of factory that will be used to create reward module

- `stakingdata`: construction data for staking module factory

- `rewarddata`: construction data for reward module factory


*Returns*  
- address of newly created Pool


****
<br>

**`setWhitelist`**`(address factory_, uint256 type_)` (external)

set the whitelist status of a module factory




*Parameters*  
- `factory_`: address of module factory

- `type_`: updated whitelist status for module



****
<br>

**`count`**`() → uint256` (public)






*Returns*  
- total number of Pools created by the factory


****
<br>

*Events*  


`PoolCreated(address user, address pool)`






`WhitelistUpdated(address factory, uint256 previous, uint256 updated)`






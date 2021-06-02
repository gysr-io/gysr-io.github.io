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

### Pool factory



`PoolFactory`

this implements the Pool factory contract which allows any user to
easily configure and deploy their own Pool



it relies on a system of sub-factories which are responsible for the
creation of underlying staking and reward modules. This primary factory
calls each module factory and assembles the overall Pool contract.

this contract also manages various privileged platform settings including
treasury address, fee amount, and module factory whitelist.



****

`constructor(address gysr_, address treasury_)` (public)





**Parameters**  
- `gysr_`: address of GYSR token

**Returns**


****

`create(address staking, address reward, bytes stakingdata, bytes rewarddata) → address` (external)

create a new Pool




**Parameters**  
- `staking`: address of factory that will be used to create staking module

- `reward`: address of factory that will be used to create reward module

- `stakingdata`: construction data for staking module factory

- `rewarddata`: construction data for reward module factory


**Returns**
- address of newly created Pool


****

`treasury() → address` (external)





**Parameters**  

**Returns**
- GYSR treasury address


****

`fee() → uint256` (external)





**Parameters**  

**Returns**
- GYSR spending fee


****

`setTreasury(address treasury_)` (external)

update the GYSR treasury address




**Parameters**  
- `treasury_`: new value for treasury address

**Returns**


****

`setFee(uint256 fee_)` (external)

update the global GYSR spending fee




**Parameters**  
- `fee_`: new value for GYSR spending fee

**Returns**


****

`setWhitelist(address factory_, uint256 type_)` (external)

set the whitelist status of a module factory




**Parameters**  
- `factory_`: address of module factory

- `type_`: updated whitelist status for module

**Returns**


****

`count() → uint256` (public)





**Parameters**  

**Returns**
- total number of Pools created by the factory



****

`PoolCreated(address user, address pool)`






****

`FeeUpdated(uint256 previous, uint256 updated)`






****

`TreasuryUpdated(address previous, address updated)`






****

`WhitelistUpdated(address factory, uint256 previous, uint256 updated)`





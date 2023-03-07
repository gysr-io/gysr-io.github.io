---
layout: page
title: IPoolFactory
description: "this defines the Pool factory interface, primarily intended for
the Pool contract to interact with"
permalink: /docs/IPoolFactory/
exclude: true
categories: [contract]
---

Pool factory interface



**`IPoolFactory`**

this defines the Pool factory interface, primarily intended for
the Pool contract to interact with







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

**`map`**`(address) → bool` (external)






*Returns*  
- true if address is a pool created by the factory


****
<br>

**`list`**`(uint256) → address` (external)






*Returns*  
- address of the nth pool created by the factory



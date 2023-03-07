---
layout: page
title: IOwnerController
description: "this defines the interface for any contracts that use the
owner controller access pattern"
permalink: /docs/IOwnerController/
exclude: true
categories: [contract]
---

Owner controller interface



**`IOwnerController`**

this defines the interface for any contracts that use the
owner controller access pattern







****
<br>

**`owner`**`() → address` (external)



Returns the address of the current owner.




****
<br>

**`controller`**`() → address` (external)



Returns the address of the current controller.




****
<br>

**`transferOwnership`**`(address newOwner)` (external)



Transfers ownership of the contract to a new account (`newOwner`). This can
include renouncing ownership by transferring to the zero address.
Can only be called by the current owner.




****
<br>

**`transferControl`**`(address newController)` (external)



Transfers control of the contract to a new account (`newController`).
Can only be called by the owner.





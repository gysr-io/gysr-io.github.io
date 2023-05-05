---
layout: page
title: OwnerController
description: "this base contract implements an owner-controller access model.

"
permalink: /docs/OwnerController/
exclude: true
categories: [contract]
---

Owner controller



**`OwnerController`**

this base contract implements an owner-controller access model.



the contract is an adapted version of the OpenZeppelin Ownable contract.
It allows the owner to designate an additional account as the controller to
perform restricted operations.

Other changes include supporting role verification with a require method
in addition to the modifier option, and removing some unneeded functionality.

Original contract here:
https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/access/Ownable.sol



****
<br>

**`onlyOwner`**`()`



Modifier that throws if called by any account other than the owner.


****
<br>

**`onlyController`**`()`



Modifier that throws if called by any account other than the controller.




****
<br>

**`owner`**`() → address` (public)



Returns the address of the current owner.




****
<br>

**`controller`**`() → address` (public)



Returns the address of the current controller.




****
<br>

**`requireOwner`**`()` (internal)



Throws if called by any account other than the owner.




****
<br>

**`requireController`**`()` (internal)



Throws if called by any account other than the controller.




****
<br>

**`transferOwnership`**`(address newOwner)` (public)



Transfers ownership of the contract to a new account (`newOwner`).
Can only be called by the current owner.




****
<br>

**`transferControl`**`(address newController)` (public)



Transfers control of the contract to a new account (`newController`).
Can only be called by the owner.




****
<br>

*Events*  


`OwnershipTransferred(address previousOwner, address newOwner)`






`ControlTransferred(address previousController, address newController)`






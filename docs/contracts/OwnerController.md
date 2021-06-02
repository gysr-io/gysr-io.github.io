---
layout: page
title: OwnerController
description: "this base contract implements an owner-controller access model.

"
permalink: /docs/OwnerController/
exclude: true
categories: [contract]
---

### Owner controller



`OwnerController`

this base contract implements an owner-controller access model.



the contract is an adapted version of the OpenZeppelin Ownable contract.
It allows the owner to designate an additional account as the controller to
perform restricted operations.

Other changes include supporting role verification with a require method
in addition to the modifier option, and removing some unneeded functionality.

Original contract here:
https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/access/Ownable.sol


****

`onlyOwner()`



Modifier that throws if called by any account other than the owner.


****

`onlyController()`



Modifier that throws if called by any account other than the controller.



****

`owner() → address` (public)



Returns the address of the current owner.

**Parameters**  

**Returns**


****

`controller() → address` (public)



Returns the address of the current controller.

**Parameters**  

**Returns**


****

`requireOwner()` (internal)



Throws if called by any account other than the owner.

**Parameters**  

**Returns**


****

`requireController()` (internal)



Throws if called by any account other than the controller.

**Parameters**  

**Returns**


****

`transferOwnership(address newOwner)` (public)



Transfers ownership of the contract to a new account (`newOwner`). This can
include renouncing ownership by transferring to the zero address.
Can only be called by the current owner.

**Parameters**  

**Returns**


****

`transferControl(address newController)` (public)



Transfers control of the contract to a new account (`newController`).
Can only be called by the owner.

**Parameters**  

**Returns**



****

`OwnershipTransferred(address previousOwner, address newOwner)`






****

`ControlTransferred(address previousController, address newController)`






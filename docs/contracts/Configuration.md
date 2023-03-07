---
layout: page
title: Configuration
description: "configuration contract to define global variables for GYSR protocol"
permalink: /docs/Configuration/
exclude: true
categories: [contract]
---

Configuration



**`Configuration`**

configuration contract to define global variables for GYSR protocol







****
<br>

**`setUint256`**`(bytes32 key, uint256 value)` (external)

set or update uint256 parameter




*Parameters*  
- `key`: keccak256 hash of parameter key

- `value`: uint256 parameter value



****
<br>

**`setAddress`**`(bytes32 key, address value)` (external)

set or update address parameter




*Parameters*  
- `key`: keccak256 hash of parameter key

- `value`: address parameter value



****
<br>

**`setAddressUint96`**`(bytes32 key, address value0, uint96 value1)` (external)

set or update packed address + uint96 pair




*Parameters*  
- `key`: keccak256 hash of parameter key

- `value0`: address parameter value

- `value1`: uint96 parameter value



****
<br>

**`getUint256`**`(bytes32 key) → uint256` (external)

get uint256 parameter




*Parameters*  
- `key`: keccak256 hash of parameter key


*Returns*  
- uint256 parameter value


****
<br>

**`getAddress`**`(bytes32 key) → address` (external)

get address parameter




*Parameters*  
- `key`: keccak256 hash of parameter key


*Returns*  
- uint256 parameter value


****
<br>

**`getAddressUint96`**`(bytes32 key) → address, uint96` (external)

get packed address + uint96 pair




*Parameters*  
- `key`: keccak256 hash of parameter key


*Returns*  
- address parameter value

- uint96 parameter value


****
<br>

**`overrideUint256`**`(address caller, bytes32 key, uint256 value)` (external)

override uint256 parameter for specific caller




*Parameters*  
- `caller`: address of caller

- `key`: keccak256 hash of parameter key

- `value`: uint256 parameter value



****
<br>

**`overrideAddress`**`(address caller, bytes32 key, address value)` (external)

override address parameter for specific caller




*Parameters*  
- `caller`: address of caller

- `key`: keccak256 hash of parameter key

- `value`: address parameter value



****
<br>

**`overrideAddressUint96`**`(address caller, bytes32 key, address value0, uint96 value1)` (external)

override address parameter for specific caller




*Parameters*  
- `caller`: address of caller

- `key`: keccak256 hash of parameter key

- `value0`: address parameter value

- `value1`: uint96 parameter value




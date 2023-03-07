---
layout: page
title: IEvents
description: "common interface to define GYSR event system"
permalink: /docs/IEvents/
exclude: true
categories: [contract]
---

GYSR event system



**`IEvents`**

common interface to define GYSR event system







****
<br>

*Events*  


`Staked(bytes32 account, address user, address token, uint256 amount, uint256 shares)`






`Unstaked(bytes32 account, address user, address token, uint256 amount, uint256 shares)`






`Claimed(bytes32 account, address user, address token, uint256 amount, uint256 shares)`






`Updated(bytes32 account, address user)`






`RewardsDistributed(address user, address token, uint256 amount, uint256 shares)`






`RewardsFunded(address token, uint256 amount, uint256 shares, uint256 timestamp)`






`RewardsExpired(address token, uint256 amount, uint256 shares, uint256 timestamp)`






`RewardsWithdrawn(address token, uint256 amount, uint256 shares, uint256 timestamp)`






`RewardsUpdated(bytes32 account)`






`GysrSpent(address user, uint256 amount)`






`GysrVested(address user, uint256 amount)`






`GysrWithdrawn(uint256 amount)`






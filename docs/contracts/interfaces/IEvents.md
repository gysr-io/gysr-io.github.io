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


`Staked(address user, address token, uint256 amount, uint256 shares)`






`Unstaked(address user, address token, uint256 amount, uint256 shares)`






`Claimed(address user, address token, uint256 amount, uint256 shares)`






`RewardsDistributed(address user, address token, uint256 amount, uint256 shares)`






`RewardsFunded(address token, uint256 amount, uint256 shares, uint256 timestamp)`






`RewardsUnlocked(address token, uint256 shares)`






`RewardsExpired(address token, uint256 amount, uint256 shares, uint256 timestamp)`






`GysrSpent(address user, uint256 amount)`






`GysrVested(address user, uint256 amount)`






`GysrWithdrawn(uint256 amount)`






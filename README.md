# Simple ERC-20 Staking

A secure and efficient smart contract for staking ERC-20 tokens. This repository provides a streamlined implementation for protocols looking to incentivize long-term token holding through reward emissions.

## Overview
Users can stake a specific ERC-20 token and earn rewards in the same token (or a different one) based on the time elapsed. The contract uses a mathematical approach to calculate rewards per block/second to ensure accuracy and gas efficiency.

### Key Features
* **Stake & Unstake:** Users can deposit tokens and withdraw them along with accrued rewards.
* **Reward Calculation:** Linear reward distribution based on the staking duration.
* **Emergency Exit:** A safety feature allowing users to withdraw their principal without rewards in case of contract pauses.
* **Owner Management:** Functions for the owner to fund the reward pool and adjust parameters.

## Technical Stack
* **Language:** Solidity ^0.8.20
* **Library:** OpenZeppelin Contracts
* **License:** MIT

## Getting Started
1. Deploy the contract by providing the address of the Staking Token and the Reward Token.
2. The owner must transfer reward tokens to the contract to fund the pool.
3. Users must `approve` the contract to spend their tokens before calling `stake`.

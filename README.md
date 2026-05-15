# Smart Contract Engineer Home Task

## Overview
This project implements a World Cup Betting system with a Reputation System on the blockchain, deployed on Base Sepolia testnet.

## Contracts

| Contract | Address | Network |
|---|---|---|
| WorldCupBetting | `0x61F90B5D4791fA3a5a67a5441c4bAC5DA0Ee0e24` | Base Sepolia |
| ReputationSystem | `0x69c6dEDe577EF117bF885D1240336110Bf341D88` | Base Sepolia |

## Contract Descriptions

### WorldCupBetting
Allows users to place bets on World Cup match outcomes using ERC20 tokens. Implements reentrancy protection and owner-controlled match management.

### ReputationSystem
Tracks user reputation scores based on betting history and outcomes. Integrated with WorldCupBetting to reward accurate predictions.

## Tech Stack
- Solidity ^0.8.0
- Foundry (forge, cast)
- OpenZeppelin Contracts
- Base Sepolia Testnet (Chain ID: 84532)

## Setup & Installation

```bash
git clone https://github.com/wanzablock/home-task-smart-contract-engineer-role.git
cd home-task-smart-contract-engineer-role

# Install Foundry dependencies
forge install
```

## Deployment

```bash
export PRIVATE_KEY=0xyour_private_key
export BASE_SEPOLIA_RPC=https://sepolia.base.org

forge script contracts/script/Deploy.s.sol:Deploy \
  --rpc-url $BASE_SEPOLIA_RPC \
  --private-key $PRIVATE_KEY \
  --broadcast -vvv
```

## Verify on Basescan
- [WorldCupBetting](https://sepolia.basescan.org/address/0x61F90B5D4791fA3a5a67a5441c4bAC5DA0Ee0e24)
- [ReputationSystem](https://sepolia.basescan.org/address/0x69c6dEDe577EF117bF885D1240336110Bf341D88)

## Notes
- Deployed to Base Sepolia as the Ethereum Devnet equivalent
- Contracts are linked: WorldCupBetting references ReputationSystem for score updates

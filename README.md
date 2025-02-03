# NFT Staking Program

## Overview

This Solana program, built using the Anchor framework, implements an NFT staking mechanism. Users can stake their NFTs to earn points over time, with various configurable parameters to control the staking process.

## Features

- Initialize staking configuration
- User account creation
- NFT staking and unstaking
- Point accumulation based on staking duration
- Freeze period for staked NFTs
- Maximum stake limit per user

## Program Structure

The program consists of several key components:

1. **Context Modules**:
   - `initialize_config.rs`: Sets up the initial staking configuration
   - `initialize_user.rs`: Creates a new user account
   - `stake.rs`: Handles the NFT staking process
   - `unstake.rs`: Manages the NFT unstaking process

2. **State Modules**:
   - `stake_config.rs`: Defines the global staking configuration
   - `user_account.rs`: Stores user-specific staking information
   - `stake_account.rs`: Represents individual staked NFT accounts

3. **Main Program Logic** (`lib.rs`):
   - Defines the program ID and entry points for various instructions

## Key Functionalities

### Initialize Config

- Sets up the staking configuration with parameters like points per stake, maximum stake, and freeze period
- Initializes the rewards mint

### Initialize User

- Creates a new user account to track staking activity and points

### Stake

- Allows users to stake their NFTs
- Verifies NFT ownership and collection
- Freezes the NFT in the user's wallet
- Updates user's staking stats

### Unstake

- Enables users to unstake their NFTs after the freeze period
- Calculates and awards points based on staking duration
- Thaws the NFT in the user's wallet
- Updates user's staking stats

## Usage

To interact with this program, you'll need to:

1. Deploy the program to a Solana cluster
2. Initialize the staking configuration
3. Create user accounts for participants
4. Use the stake and unstake instructions to manage NFT staking

## Development

### Prerequisites

- Rust and Cargo
- Solana CLI tools
- Anchor framework

## Security Considerations

- Ensure proper access controls and signature verifications
- Validate all user inputs and account constraints
- Be cautious with mathematical operations to prevent overflows

## Future Enhancements

- Implement a reward distribution mechanism
- Add more flexible staking options
- Integrate with a front-end application for easier user interaction

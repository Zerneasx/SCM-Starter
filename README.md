# Smart Wallet Assessment Contract

## Overview

This repository contains a Solidity smart contract named Assessment. The contract is designed to manage an account with deposit, withdraw, and transfer functionalities. It includes an owner, balance tracking, and events for deposit, withdraw, and transfer actions.

## Contract Details

### State Variables

- `owner`: The address of the account owner.
- `balance`: The current balance of the account.

### Events

- `Deposit(uint256 amount)`: Triggered when a deposit occurs.
- `Withdraw(uint256 amount)`: Triggered when a withdrawal occurs.
- `Transfer(address indexed to, uint256 amount)`: Triggered when a transfer occurs, with the recipient's address and the transferred amount indexed.

### Constructor

- Initializes the contract with an owner and an initial balance.

### Functions

#### `getBalance() public view returns (uint256)`

- Retrieves the current balance of the account.

#### `deposit(uint256 _amount) public payable`

- Allows the owner to deposit funds into the account.
- Emits a `Deposit` event.

#### `withdraw(uint256 _withdrawAmount) public`

- Allows the owner to withdraw funds from the account.
- Emits a `Withdraw` event.
- Handles insufficient balance with a custom error message.

#### `transfer(uint256 _transferAmount) public`

- Allows the owner to transfer funds to a specific address.
- Emits a `Transfer` event.
- Handles insufficient balance with a require statement.

## Usage

Deploy the contract to an Ethereum-compatible blockchain using a tool like Remix or Truffle.

## Author

Donato, Zeno
202011124@fit.edu.ph

## Acknowledgments

- Ethereum Community

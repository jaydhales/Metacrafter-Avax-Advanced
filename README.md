## Overview 
The vault smart contract is deployed on `0x95CA0a568236fC7413Cd2b794A7da24422c2BBb6`. Users can use this contract to deposit tokens, minting shares in proportion to the deposited amount, and later withdraw a corresponding amount of tokens based on the shares they hold.

## Contract Details
Contract Address: 0x95CA0a568236fC7413Cd2b794A7da24422c2BBb6
Network: JaySUBNET

## Vault Functionality
1. Deposit Function
Users can deposit ERC-20 tokens into the vault by calling the deposit function. This function calculates the number of shares to mint based on the deposited amount and the current total supply of shares.

function deposit(uint _amount) external
2. Withdraw Function
Users can withdraw their tokens from the vault by calling the withdraw function. This function calculates the amount to withdraw based on the number of shares burned and the current total supply of shares.

function withdraw(uint _shares) external
3. ERC-20 Interface
The contract includes an interface for ERC-20 functionality, providing basic token operations like checking balances, transferring tokens, and approving token transfers.

interface IERC20 {
    // ERC-20 functions...
}

## Usage Guidelines
Token Approval: Before depositing, ensure that you have approved the contract to spend your ERC-20 tokens. Use the ERC-20 approve function to grant the necessary permission.

Deposit: Call the deposit function with the desired amount of tokens to mint corresponding shares.

Withdraw: Call the withdraw function with the number of shares to burn and receive the proportional amount of tokens.

Monitor Balances: Keep track of your token balances and shares to manage deposits and withdrawals effectively.

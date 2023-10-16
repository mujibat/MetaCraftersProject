# MetaCraftersProject
# MyToken Contract

The `MyToken` smart contract is a basic Ethereum-based token that allows for minting and burning tokens. This README provides an overview of the contract's features and how to interact with it.

## Table of Contents

- [Contract Overview](#contract-overview)
- [Public Variables](#public-variables)
- [Mapping Variable](#mapping-variable)
- [Mint Function](#mint-function)
- [Burn Function](#burn-function)

## Contract Overview

`MyToken` is a simple Ethereum smart contract for a custom token named "Dolapo" with the abbreviation "DLP." It maintains a total supply and tracks the balances of addresses holding these tokens. The contract also provides minting and burning functions for managing the token supply.

## Public Variables

The contract includes the following public variables:

- `tokenName`: A string representing the name of the token, which is set to "Dolapo."
- `tokenAbbrv`: A string representing the token's abbreviation, which is set to "DLP."
- `totalSupply`: An unsigned integer (uint) that stores the total supply of tokens. Initially, it is set to 0.

These variables can be accessed by anyone without requiring any special permissions.

## Mapping Variable

The contract uses a mapping variable:

- `balances`: This mapping associates Ethereum addresses with their token balances. Users can check their token balances by querying this mapping.

## Mint Function

The `mint` function allows the creation of new tokens. It takes two parameters:

- `_address`: The Ethereum address to which the new tokens will be minted.
- `_value`: The number of tokens to be created and added to the `_address`'s balance.

The `mint` function increases the total supply by the specified `_value` and adds these newly created tokens to the balance of the given `_address`.

## Burn Function

The `burn` function is used to destroy (burn) tokens, reducing the total supply. It also takes two parameters:

- `_address`: The Ethereum address from which tokens will be burned.
- `_value`: The number of tokens to burn from the `_address`.

Before burning tokens, the function checks if the `_address` has a balance greater than or equal to the specified `_value`. If the condition is met, it subtracts the burned tokens from the total supply and the `_address`'s balance.

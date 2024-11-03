# DeFi Kingdom

## Contract

This contract represents a tokenized vault that allows users to deposit and withdraw ERC-20 tokens.

## Components

`token`: Stores the address of the ERC-20 token managed by the vault.
`totalSupply`: Tracks the total number of vault shares in circulation.
`balanceOf`: Maps user addresses to their respective share balances.
`_mint`: Private function to mint new vault shares and assign them to an address.
`_burn`: Private function to burn (destroy) existing vault shares from an address.
`deposit`: Public function for users to deposit ERC-20 tokens into the vault, receiving vault shares in return.
`withdraw`: Public function for users to withdraw ERC-20 tokens from the vault, burning their vault shares.

#### `Deposit`

- Calculates the number of shares to mint based on the deposited amount, total supply, and existing token balance.
- Mints the calculated shares and assigns them to the depositor.
- Transfers the deposited tokens from the user to the vault contract.

#### `Withdraw`

- Calculates the amount of tokens to withdraw based on the shares being burned, total supply, and existing token balance.
- Burns the specified shares from the user's balance.
- Transfers the calculated token amount from the vault contract back to the user.

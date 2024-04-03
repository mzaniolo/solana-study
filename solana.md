Create a wallet
```bash
solana-keygen new
```

Add funds to wallet
```bash
solana-keygen airdrop 2
```

Create a token
```bash
spl-token create-token --decimals 10
```

Create the an account to the new token
The token address is generated when creating the token
```bash
spl-token create-account <token-address>
```

To mint tokens
Works because the account has the token authority
By adding `<user-token-account>` we can specify the user account to mint
```bash
spl-token mint <token-address> <amount-to-mint>
```

To list token accounts
```bash
spl-token accounts
```

To see the amount of tokens from an account
```bash
spl-token supply <token-account>
```

To transfer tokens
```bash
spl-token transfer <token-address> <amount> <recipient-address> --allow-unfunded-recipient --fund-recipient
```

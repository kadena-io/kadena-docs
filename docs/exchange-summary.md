#Exchange Summary

Blockchain transactions are irreversible and if you make a mistake, your coins may not be recoverable. A best practice with any blockchain is to always perform a small test transaction when executing a transfer for the first time. For added security, send those coins back to the sender to verify that the receiver's account works as expected.

The main purpose of a cryptocurrency exchange is to allow users to buy and sell coins. They may also allow users to transfer their coins to some other wallet. Exchanges generally do not support the full range of features enabled by many blockchains, including Kadena. If you would like to interact with the Kadena blockchain in more ways than simply buying and selling KDA, then you will find [Wallet Resources](Public-Chain-Docs.html) helpful.

Here is a summary of notable features regarding the exchanges that support KDA, for informational purposes only—

<br />
*Updated May 2021*

<br />
**<a href="http://kucoin.com/" target="_blank">KuCoin</a>**

- Official KDA exchange
- Accessible globally
- KYC not required
- Supports transfers to (and from!) Chain ID 1 only
- Best practices:
    - When depositing KDA, first cross chain transfer any coins to your Chain 1 address before transferring to your Kucoin address
    - When withdrawing KDA, Kucoin will transfer your KDA to your Chain 1 address 

<br />
**<a href="https://global.bittrex.com/" target="_blank">Bittrex Global</a>**

- Official KDA exchange
- Accessible to non-US residents
- KYC required
- Supports transfers on Chain ID 0 only

<br />
**<a href="https://coinmetro.com/" target="_blank">CoinMetro</a>**

- Official KDA exchange
- Accessible globally
- KYC required
- Supports transfers on all chains (Chain ID 0 - 19), including cross-chain transfers
- Supports TxBuilder, which allows for withdrawal transfers that can create named accounts or multi-signature accounts

<br />
**<a href="https://www.hotbit.io/" target="_blank">HotBit</a>**

- Unofficial KDA exchange
- Accessible globally
- KYC not required
- Supports transfers on Chain ID 0 - 9 only
- Reported user issues:
    - Depositing KDA via cross-chain transfer is unreliable
    - Withdrawing KDA to existing accounts is unreliable
- Reported best practices:
    - When depositing KDA, perform a simple same-chain transfer
    - When withdrawing KDA, either (1) withdraw to an unnamed account that does not yet exist or (2) withdraw to an existing account that was already created by HotBit from a previous withdrawal.

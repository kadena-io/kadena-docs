# Public Chain Interaction

## **Get a Wallet, Create Keys, & Transfer KDA**

**Resources**

- <a href="https://www.kadena.io/chainweaver" target="_blank">Chainweaver</a> (wallet): Official cryptocurrency and smart contract wallet for the Kadena Public Blockchain
- <a href="https://medium.com/@ZelOfficial/zelcore-adds-kadena-assets-store-kda-across-multiple-chains-3b8039f2777c" target="_blank">ZelCore</a> (wallet): Officially supported third-party multi-asset wallet
- <a href="https://github.com/kadena-community/bag-of-holding" target="_blank">Bag of Holding</a> (wallet): Terminal Wallet (Community contribution)
- <a href="https://github.com/kadena-community/secure-keygen" target="_blank">Secure Key Generation</a>: Package for generating ED25519 key pairs with user supplied entropy (Community contribution)
- <a href="https://kadena-community.github.io/kadena-transfer-js/" target="_blank">Simple Key Generation</a>: Generate a key pair with one click (Community contribution)
- <a href="https://kadena-community.github.io/kadena-transfer-js/" target="_blank">Simple Token Transfer</a>: Transfer KDA to new or existing accounts (Community contribution)
- <a href="https://balance.chainweb.com/" target="_blank">Simple Balance Checker</a>: View the current balance of any account
- <a href="http://txtool.chainweb.com/" target="_blank">Transaction Tester</a>: GUI for assembling Pact code and previewing transactions
- <a href="https://kadena-community.github.io/kadena-transfer-js/" target="_blank">Finish Cross-chain Transfer</a>: Enter a Request Key and complete a cross-chain transfer on the recipient chain (Community contribution)

**Guides**

- [Chainweaver User Guide](../Chainweaver-Support): Official support resource for using Chainweaver
- "<a href="https://medium.com/kadenacoin/how-to-generate-a-kda-address-fd009a06ea05" target="_blank">How to generate a KDA address</a>": Article by <a href="https://medium.com/@Thanos_42" target="_blank">Thanos</a> (Community contribution)
- <a href="https://medium.com/kadena-io/beginners-guide-to-kadena-accounts-keysets-fb7f32104291" target="_blank">Beginner's Guide to Accounts & Keysets</a>: Brief description of keys, keysets, accounts and how they work in Kadena
- <a href="https://medium.com/kadena-io/kadena-public-blockchain-getting-started-with-transfers-153bf87d6824" target="_blank">Getting Started with Transfers</a>: Brief description of transfer types and tools

## **View Network Activity**

**Resources**

- <a href="https://explorer.chainweb.com/mainnet" target="_blank">Block Explorer</a>: Analytics tool which visualizes the mining, propagation and braiding of blocks across multiple Kadena chains in real time
- <a href="https://kadena.banteg.xyz/peers" target="_blank">Active Node List</a>: List of known node addresses (Community contribution)

## **Write Smart Contracts**

**Resources**

- <a href="https://github.com/kadena-io/pact#installing-pact" target="_blank">Installing Pact</a>: Official Kadena README
- <a href="https://pact-language.readthedocs.io/en/stable/" target="_blank">Pact Read the Docs</a>: Complete language reference for the Pact smart contract language
- <a href="https://pact.kadena.io/" target="_blank">Pact Web REPL</a>: Web-based environment for writing, testing, and deploying Pact smart contracts to testnet

**Guides**

- <a href="https://pactlang.org/" target="_blank">Pact Developer Tutorials</a>: Learn Pact's fundamental concepts through structured lessons and sample projects
- [Pact Local Queries](../pact-local-queries): Describes how to use `local` API endpoints to dry-run smart contracts using Mainnet data (Community contribution)
- <a href="https://kadena-io.github.io/kadena-docs/cookbook/safe-rotate-and-drain" target="_blank">Safe Rotate and Drain</a> (example): Describes how to rotate an account’s key then transfer the account’s balance to another account (Community contribution)
- <a href="https://kadena-io.github.io/kadena-docs/cookbook/safe-transfer" target="_blank">Safe Transfer</a> (example): Describes how to perform a safe transfer by requiring the recipient to also sign and return some KDA all within a single transaction (Community contribution)
- <a href="https://gist.github.com/LindaOrtega/1c219f887d9782c6745dbd827bdbfb4d" target="_blank">Deploy a module to Testnet using Command Line</a> (example): (Community contribution)

## **Interact with dApps**

**Resources**

- <a href="http://testnet.chainweb.com/" target="_blank">Testnet Portal</a>: Create an account, get free coins, and play games
- <a href="http://testnet.chainweb.com/" target="_blank">Testnet Coin Faucet</a>: Get free coins to practice executing transfers and smart contracts
- <a href="http://hybrid.chainweb.com/" target="_blank">Hybrid Blockchain Demo</a>: Interoperate between public and private blockchain networks through stablecoin smart contracts.
- <a href="https://kadena-io.github.io/signing-api/" target="_blank">Wallet Signing API</a>: Documentation of the signing API which facilitates communication between dApps and wallets

## **Run a Node**

**Resources**

- <a href="https://github.com/kadena-io/chainweb-node" target="_blank">chainweb-node</a>: The complete open-source repository for Chainweb
- <a href="https://github.com/kadena-io/chainweb-node/releases" target="_blank">Chainweb binaries</a>: The latest binary release to run your own node
- <a href="https://github.com/kadena-io/chainweb-node" target="_blank">Bootstrap nodes</a>: A list of bootstrap nodes for Mainnet and Testnet
- <a href="https://github.com/kadena-io/chainweb-node" target="_blank">Hardware specs required to run a node</a>: Kadena official README
- [Troubleshooting](../troubleshoot-chainweb): Common issues related to running a node

**Guides**

- <a href="https://github.com/kadena-io/chainweb-node#installing-chainweb" target="_blank">Installing Chainweb</a> (Mac and Linux): Kadena official README
- <a href="https://github.com/kadena-io/chainweb-node" target="_blank">Configuring and running a node</a>: Kadena official README
- <a href="https://github.com/kadena-community/node-setup" target="_blank">Running a node, alternate 1</a>: Kadena node installation instructions (Community contribution)
- <a href="https://medium.com/kadenacoin/how-to-operate-a-kadena-node-kda-7844622ed5b4" target="_blank">Running a node, alternate 2</a>: Kadena node installation instructions (Community contribution)
- <a href="https://github.com/kadena-io/chainweb-node" target="_blank">Monitoring the health of a node</a>: Kadena official README

## **Interact with Nodes**

**Resources**

- [REST API Examples with curl](../rest-api-examples): View commands for querying a node to get database information such as block header and cut height

## **Index and Analyze the Blockchain**

**Resources**

- <a href="https://github.com/kadena-io/chainweb-data" target="_blank">chainweb-data</a>: Chainweb data indexer for storing blockchain data in a Postgresql database

## **Start Mining**

**Resources**

- <a href="https://github.com/kadena-io/chainweb-miner" target="_blank">Chainweb-miner</a>: Kadena official README for mining to the Kadena Public Blockchain
- <a href="https://github.com/kadena-community/bigolchungus" target="_blank">BigOlChungus</a> (Kadena miner): Open Source Linux AMD/Nvidia OpenCL miner; one instance per card (Community contribution)
- <a href="https://github.com/Jacoby6000/kda-miner/releases" target="_blank">KDA-Miner</a> (Kadena miner): Open Source Linux AMD/Nvidia OpenCL miner, 10% fee (Community contribution)
- <a href="https://github.com/NoncerPro/Kadena" target="_blank">NoncerPro-Kadena</a> (Kadena miner): Closed Source Linux/Windows Nvidia Cuda miner, 2% fee (Community contribution)
- <a href="https://github.com/doktor83/SRBMiner-Multi" target="_blank">SRBMiner</a> (Kadena miner): Closed Source Linux/Windows AMD miner, 0.85% fee (Community contribution)
- [Troubleshooting](../troubleshoot-chainweb): Common issues related to mining KDA

**Guides**

- <a href="https://github.com/kadena-io/chainweb-miner" target="_blank">How to mine with a CPU</a>:
- <a href="https://github.com/kadena-io/chainweb-miner" target="_blank">How to mine with a GPU</a>:
- "<a href="https://medium.com/kadenacoin/how-to-mine-kadena-kda-c5fe1746c83d" target="_blank">How to solo mine Kadena</a>": Article on how to solo mine Kadena, by <a href="https://medium.com/@Thanos_42" target="_blank">Thanos</a> (Community contribution)
- <a href="https://blog.f2pool.com/en/mining-tutorial-en/kda_en" target="_blank">F2Pool Mining Guide</a>: Instruction on mining with f2pool (Community contribution)
- <a href="https://medium.com/how-to-mine-on-icemining-pool/how-to-mine-kda-61e57545eced" target="_blank">Icemining Mining Guide</a>: Instruction on mining with icemining (Community contribution)

# Kadena FAQ

#### What consensus mechanism does Kadena use?

Proof of Work

<br />
#### What hashing algorithm does Kadena use?

Blake2s_256

<br />
#### What is the target block time for Kadena?

30 seconds

<br />
#### What are the block rewards?

Block rewards are readjusted against a set schedule every six months, with roughly half of the remaining minable coins issued as block rewards every 20 years. See the complete miner block reward schedule <a href="https://github.com/kadena-io/chainweb-node/blob/master/rewards/miner_rewards.csv" target="_blank">here</a>.

<br />
#### What is KDA?

See the [What is KDA](what-is-kda.html) page for information regarding Kadena’s native cryptocurrency, KDA.

<br />
#### Does Kadena have a block explorer?

View the block explorer <a href="https://explorer.chainweb.com/mainnet" target="_blank">here</a> which visualizes the mining, propagation and braiding of blocks across multiple Kadena chains in real time

<br />
#### Where can I find Kadena’s whitepapers?

Kadena has published whitepapers for the public protocol Chainweb, the private blockchain Kuro, and the smart contract language Pact which can be found <a href="https://www.kadena.io/whitepapers" target="_blank">here</a>

<br />
#### Is Kadena open source?

Yes, the open-source repository for the Kadena public blockchain is <a href="https://github.com/kadena-io/chainweb-node" target="_blank">here</a>

<br />
#### Why does Kadena’s public blockchain use proof of work?

Kadena uses proof of work for a few key reasons:

1. Evidence: PoW is the only “battle-tested” consensus protocol primitive.
2. Economic incentive alignment: PoW creates an economic incentive for the majority of the hashpower to validate and honestly support the entire network. It is an open research question if a non-PoW approach can reasonably achieve the same.
3. Regulation: In the eyes of certain financial regulators, proof of work miners are not considered money transmitters, making a probabilistic PoW mining system safer from a US regulatory perspective than a system with more “finality” like PoS.

<br />
#### How does Kadena scale?

Kadena’s public blockchain scales by providing a mechanism to asynchronously produce many blocks on different peer chains all at the same height, with each block requiring a fraction of the hash power of the total network. This configuration drastically increases the number of transactions per second over the total network.

<br />
#### How does Kadena deal with congestion?

Transaction costs will rise as the number of transactions rise on one chain. You can set up an account on a less congested chain, where transaction costs are cheaper, and move your tokens through a simple burn-receipt using on-chain SPV. Miners have economic incentive to cooperate with reconfiguring the network to a larger size when the entire network starts to become congested.

<br />
#### What does it mean to “braid multiple chains”?

Braiding chains together was first proposed for security purposes. In effect, chains are “braided” as each chain’s newly mined block incorporates the Merkle roots of its peer chains. By having multiple mined blocks at the same height each referencing each other’s past, the protocol decreases the duration of time where an attacker could get “lucky” against an honest network. Think of an attacker needing to flip 6 coins and get all heads (mine 6 blocks) vs. needing to flip 12 coins and get all heads (mine 6 blocks from two related chains). The latter is harder. This same intuition applies to Kadena’s multi-chain configuration.

<br />
#### How are tokens moved between different Kadena chains?

Tokens are moved across chains using a Simple Payment Verification (SPV) smart contract.

<br />
#### How do I run a node?

Official information for running a node is maintained at <a href="https://github.com/kadena-io/chainweb-node" target="_blank">this GitHub repository</a>, and supplementary community resources collected within this site’s [Public chain interaction](Public-Chain-Docs.html) page.

<br />
#### How do I become a miner?

Official information for mining KDA is maintained at <a href="https://github.com/kadena-io/chainweb-miner" target="_blank">this GitHub repository</a>, and supplementary community resources collected within this site’s [Public chain interaction](Public-Chain-Docs.html) page.

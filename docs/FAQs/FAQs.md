### **Accounts, Keys, and Addresses**

**Can I import and see the balance of an non-Chainweaver account that I may have created through mining?**
We will be providing more support for this user flow in the future. For now, once you have gone to the wallet section of Chainweaver and created an account, you can hit ”Receive” at the right side of the screen to bring up the Receive screen and choose “Option 2: Transfer from non-Chainweaver Account.” Then, input details of your non-Chainweaver account and receive the money from that account into the Chainweaver account. Please note that this transaction will charge a small amount of gas.

**What is the difference between an anonymous vs. vanity account?**
When you create an anonymous account, it creates an account locally that has the same name as the Public Key.  At this point, the account is not yet created on the blockchain. The account will be created on the blockchain once you use it to mine or coins are transferred from another account using transfer-create.

To ensure that you have control of your account, the workflow of creating a vanity account sends a transaction to the blockchain to create the account. All transactions cost gas, so you need to pay gas for the transaction.  In order to create a vanity account, you need an account on the blockchain that has coins so that you can use it to pay for gas for the vanity account creation.

We are planning to make further improvements to explain this difference  and also make it clear which accounts are and are not yet on the blockchain.

**If I create an account in Chainweaver, can I then use it for mining?**
Yes, once you create an account in Chainweaver, you can copy the public key by clicking the ellipses on the right side of the account row in the Wallet screen and use it to mine. However, mining (as you win blocks) will create your account on all chains. Chainweaver currently will not allow you to create the same account on multiple chains. With this user flow, you could have coins on all chains but would not be able to see them in Chainweaver. We are working on improvements so that you will be able to create the same account on all chains.

**Will there be a way to consolidate funds on different chains?**
For now, we are focused on creating the core building blocks of single-chain and cross-chain transfers. We expect tools that care of these things for you to evolve over time.

**What is a Kadena address?**
Kadena address is a concatenation of the account name, chain id, possibly the public key if the account name is different, and a checksum (in order to protect against loss of funds from typos).


### **Transactions (Send/Receive)**

**What does the “Receive” button do?**
The “Receive” button at the right side of the screen in main accounts section of the wallet screen shows you a Kadena address that you can then copy and send to the sender. The sender can then use it to send coins to your account. Currently, the button also allows you to receive money into a Chainweaver account from a non-Chainweaver account. 


### **Smart Contracts**

**Is the Smart Contracts screen the same as pact.kadena.io?**
Yes, the contracts screen has the same functionality as pact.kadena.io, with some minor changes for the Mac application.


**Security & Access**

**Where are my private keys stored?**
The private keys are stored in encrypted form in ~/Library/Application Support/io.kadena.chainweaver. The password is what decrypts the encrypted file on your disk.

**How does Recovery work?**
The 12-word recovery phrase is the only thing required to recover all your keys since the phrase is a deterministic generation of keys. Currently, there is no way to recover the vanity accounts or “Notes”; this is something that we are working on. We believe that recovery is a break-glass and often painful process. Still,we are working to improve this.


### **Platforms / Operating Systems**

**What operating systems does Chainweaver support?**
Currently, Chainweaver is only available for Mac. We are also working on a Linux application as a very high priority.  As we develop our roadmap, we will be looking at iOS and Android apps as well.

**Does Chainweaver support a hardware wallet?**
Hardware wallet support is on our roadmap, further down the line.

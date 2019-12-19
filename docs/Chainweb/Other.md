### **Kadena Developed**

 - [Block Explorer](https://explorer.chainweb.com/mainnet)
 
### **Community Developed**

 - [Active Node List](https://kadena.banteg.xyz/peers)

 - Bootstrap Node Database Backup
 --  [http://bigchungusmining.energy/db/](http://bigchungusmining.energy/db/) - OR -
 [http://node-dbs.chainweb.com/db-chainweb-node-ubuntu.18.04-latest.tar.gz](http://node-dbs.chainweb.com/db-chainweb-node-ubuntu.18.04-latest.tar.gz)

### Pact Validation Failure

> "Sender account has insufficient gas"

This validation failure could be the result of not having enough in your account to cover your transaction's gas fees. This is possible if you increased the gas price from the default price, or you have a REALLY small balance. The other possibility for this validation failure is that you didn't sign the transaction appropriately (i.e. the account specified in the "sender" field does not correspond with the account that signed the transaction and is being charged for gas).

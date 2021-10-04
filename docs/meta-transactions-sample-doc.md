# What are Meta-transactions?

Transactions play an essential role on Ethereum, but they require paying gas fees in ETH, which can discourage first time users from onboarding a Dapp

Meta-transactions solve that problem by enabling a third party to pay for a transaction fee on behalf of a user, thus greatly reducing friction.

The anatomy of a meta-transaction is quite straightforward: it is a transaction containing an executable signed message:

Meta-transaction



Here is a simplified flow demonstrating how meta-transactions can be implemented for onboarding users, following the standards of Open Gas Station Network.  



The User/DApp signs a message which includes function calls, arguments and the users signature. This does not require any gas.
The message is sent to an off-chain relayer. The relayer creates a signed transaction (with the user’s signature details) and sends it to the relay hub.
The relay hub verifies and funds the transaction and relays it to the recipient contract.
The recipient contract executes the method(s) on-chain on behalf of the user.

Although onboarding users won’t get 

 With meta transactions, users still use their signature to send and authenticate transactions. The difference is, once this happens, the transaction is now managed by the relayer who pays the gas and sends the transaction to the receiving address.


Projects supporting or implementing meta-transactions:
Burner wallet

Gas Station Network was built to support meta-transactions use on Ethereum, it offers a decentralized network of transaction relayers.
Burner Wallet Project: https://github.com/austintgriffith/burner-wallet

https://eips.ethereum.org/EIPS/eip-3074
https://eips.ethereum.org/EIPS/eip-2771
# What are Meta-transactions?
Transactions play an essential role on Ethereum, but they require purchasing ETH to pay for gas fees, which can discourage first time users from onboarding a Dapp.

Meta-transactions solve that problem by enabling a third party to pay for a transaction fee on behalf of a user, abstracting away gas fees from UX.

The anatomy of a meta-transaction is quite straightforward: it is a transaction containing an executable signed message.
![](images/meta-transactions-anatomy.png)


Here is a simplified flow demonstrating how meta-transactions can be implemented for onboarding users, following the standards of the Open Gas Station Network (simplified version).  



The User/Dapp signs a message from their Etherless account which includes function calls, arguments and the users signature. This does not require any gas.
The message is sent to an off-chain relayer. The relayer creates a signed transaction (with the user’s signature details) and sends it to the relay hub.
The relay hub verifies and funds the transaction then relays it to the recipient contract.
The recipient contract executes the method(s) on-chain on behalf of the user.

Meta transactions can facilitate onboarding, they can also enable users to pay gas in fiat or ERC20 tokens.



Resources:
Gas Station Network
Burner Wallet
EIP-3074
EIP-2771
ERC-4337


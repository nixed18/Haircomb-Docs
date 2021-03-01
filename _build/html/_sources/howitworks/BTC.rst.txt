Bitcoin Blockchain
**********************

Haircomb exists within the transaction data of the BTC blockchain. It does so by compressing information about Haircomb-related events into a 256bit hash, which it then converts to a P2WSH address. By sending BTC to this address, you have now recorded it on the BTC blockchain, and anybody who knows what they're looking for can go and find it. This methodology allows Haircomb to publicly record minimal information (only the proof that an event happened) while the rest of the details are transferred privately, off-chain. 

In order to prevent double spends, Haircomb uses a specific type of public/private key encryption, a Winternitz One Time Signature scheme that uses 21 private keys per public key. The use of this scheme also happens to make Haircomb quantum-proof. This will be discussed further in the Keys section.



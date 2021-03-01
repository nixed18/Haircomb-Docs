Cold Wallets
**************

Basic
---------

Cold wallets are the core storage unit of Haircomb. A cold wallet has a private key made up of twenty-one 256bit numbers, and a public key made of one 256bit number. In order to send money out of a cold wallet, you'll need to sign a transaction by sending 330 sats to 21 P2WSH addresses on the BTC chain. These addresses are different for every cold wallet and transaction combination, and are committed to prevent users from double-spending their COMB. When you generate a new key in the Haircomb program, you are creating a new cold wallet.


Advanced
------------

Structure
~~~~~~~~~~~~~~

A cold wallet's public key is generated from the 21 private keys using the following method:

1. Take the first private key, and hash it 59213 times.
#. Repeat for the remaining private keys. 
#. Take the results and concatenate them in numerical order (result_1 CAT result_2 CAT result_3 . . .)
#. Hash the value. The result of this hash is the wallet public key.


Transacting
~~~~~~~~~~~~~~

The process to determine the 21 P2WSH addresses that make up a cold wallet's transaction signature is demonstrated below.

Alice wants to send Bob all of her COMB.

1. Alice creates the transaction id; SHA256(Alice_Pubkey CAT Bob_Pubkey)
#. She then inserts the transaction ID into a function called CutCombWhere()
#. CutCombWhere will spit out 21 unsigned integers that total to 59213.
#. Alice hashes each private key X times, where X is 59213 - the key's corresponding CutCombWhere() number. These 21 numbers make up the signature of the transaction.
#. The hashed result is then concatenated with the whitepaper's hash and hashed again.
#. Alice now has 21 numbers which she then encodes to segwit and commits to the BTC blockchain.
#. After 6 confirmation, the COMB are no longer in Alice's cold wallet.

Now that Alice has sent the transaction, she needs to give Bob the information that he needs to receive the transaction.

1. Alice gives Bob the transaction ID components (her address and his address) and transaction signature, as well as a complete transaction history for the cold wallet to prove how many COMB it contained.
#. Bob validates the transaction history to make sure that Alice's wallet had the funds she said it did.
#. Bob checks to make sure that the transaction signature has been committed to the BTC blockchain.

If the signature is not committed to the BTC blockchain, Bob knows the transaction is invalid. But Bob isn't done yet, he still must check for double-spends, and confirm that the signature matches the public key.

1. Bob calculates the transaction ID from the addresses that Alice gave him.
#. He then runs the ID through CutCombWhere(), and gets the same 21 small numbers that Alice did.
#. Bob hashes each of the 21 signature numbers X times, where X is the number's corresponding CutCombWhere() number. After each individual hash, Bob hashes the result with the whitepaper hash and checks to see if the result has been committed on the BTC blockchain.
#. If Bob finds any results that have been committed before the current transaction was signed and committed, Bob knows that this address has already been burnt, and rejects the transaction.
#. After Bob has finished hashing each of the 21 chains he takes the last result of each chain, concatenates them, and hashes them. If the result is the same as Alice's public key, he knows the transaction signature is correct.

If the signature was committed, there was no double spend, and the transaction data correctly matched the signature, Bob now knows that he has the COMB Alice sent.

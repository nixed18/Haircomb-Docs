The Basics
**************

Location
--------------------

Haircomb exists within the transaction data of the BTC blockchain. It does so by compressing information about Haircomb-related events into a 256bit hash, which it then converts to a P2WSH address. By sending BTC to this address, you have now recorded it on the BTC blockchain, and anybody who knows what they're looking for can go and find it. This methodology allows Haircomb to publicly record minimal information (only the proof that an event happened) while the rest of the details are transferred privately, off-chain. 

In order to prevent double spends, Haircomb uses a specific type of public/private key encryption, a Winternitz One Time Signature scheme that uses 21 private keys per public key. The use of this scheme also happens to make Haircomb quantum-proof. This will be discussed further in the Keys section.

Terminology
---------------

SHA256
~~~~~~~~
Haircomb relies **heavily** on the SHA256 hash algorithm. To give a brief explanation, the algorithm takes any input and produces a 256bit number as an output. Not only that, but it does so in a completely irreversible way. The only way to determine what input generated a specific output is to actually try hashing the input and checking to see if the output is the one you're looking for. This one-way compression will come up often within this documentation, any time you see the term "hashed," it is specifically referring to using the SHA256 algorithm.

While it may not be important to understand exactly how the algorithm works, what is important is to remember that any time you see "hashed" or "SHA256(X)", it means that the value was converted into a 256bit integer, and that it is impossible to figure out what the input was without explicitly being told.


CAT
~~~~~

While reading this documentation you will often see the term CAT. It is short-form for the word "concatenate," which refers to sticking information together in sequential order. For example, A CAT B CAT C == ABC, or 1 CAT 2 CAT 3 == 123. Haircomb uses this process to encrypt information by concatenating two pieces of information, then hashing the result.


Commit
~~~~~~~~

"Commit" is another term you will frequently see. In this context, it refers to information that has been permanently stored on the BTC chain. Once information has been committed, there's no taking it back.


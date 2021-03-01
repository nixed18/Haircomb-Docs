Terminology
******************

SHA256
~~~~~~~~
Haircomb relies **heavily** on the SHA256 hash algorithm. To give a brief explanation, the algorithm takes any input and produces a 256bit number as an output. Not only that, but it does so in a completely irreversible way. The only way to determine what input generated a specific output is to actually try hashing the input and checking to see if the output is the one you're looking for. This one-way compression will come up often within this documentation, any time you see the term "hashed," it is specifically referring to using the SHA256 algorithm.

While it may not be important to understand exactly how the algorithm works, what is important is to remember that any time you see "hashed" or "SHA256(X)", it means that the value was converted into a 256bit integer, and that it is impossible to figure out what the input was without explicitly being told.

Hashchain
~~~~~~~~~~~~~~
A hashchain is the structure that results from taking a piece of information, hashing it, and then hashing the result. This can be repeated ad nauseam. Below you will find the first five links in the hashchain that begins with the number 1.

1. 1
#. 6b86b273ff34fce19d6b804eff5a3f5747ada4eaa22f1d49c01e52ddb7875b4b
#. e0bc614e4fd035a488619799853b075143deea596c477b8dc077e309c0fe42e9
#. d6a804981ea7ce374acc21c9a8bf82f50b684b0ea4bdf8b26a7a775291aaf7a6
#. ad376767fc04814220cc25c79b2777cd14704f23f1830318b5bd9eb97e4fedf6

You can try it out for yourself here: https://emn178.github.io/online-tools/sha256.html


CAT
~~~~~

The term CAT is short-form for the word "concatenate," which refers to sticking information together in sequential order. For example, A CAT B CAT C == ABC, or 1 CAT 2 CAT 3 == 123. Haircomb uses this process to encrypt information by concatenating two pieces of information, then hashing the result.


Commit
~~~~~~~~

"Commit" is another term you will frequently see. In this context, it refers to information that has been permanently stored on the BTC chain. Once information has been committed, there's no taking it back.


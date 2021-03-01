Liquidity Stacks
**************************

Overview
-----------

Lquidity Stacks are Haircomb's way of splitting up COMB. 

When you create a Liquidity Stack, its address is composed of 3 numbers:

1. The address of the person you'll be sending COMB to (the Receiving Address).
2. The amount of COMB you'll be sending to them. (the Amount).
3. The address where you want to remaining COMB to end up (the Change Address).

Rather than send COMB directly to another wallet, you can send it to the address of a Liquidity Stack, which will siphon off the amount you specify before sending the remaining to your Change Address. During a transaction, you'll enter in the place you want the funds to go, and how many funds you want to go there, and the wallet will create the Liquidity Stack for you. Once there is enough COMB in the Liquidity Stack  (equal to or greater than the amount you specified), the Liquidity Stack will trigger. The specified Amount of funds will go to the Receiving Address, and the remaining funds will go to the Change Address. If any more funds are ever sent to this Liquidity Stack, they will all go directly to the Change Address.

**Never send COMB to a Liquidity Stack if you don't have as much COMB as the listed Amount!** Liquidity Stacks only trigger when they're holding as much of or more COMB than their listed Amount, so your COMB will be stuck!


Mechanics
-----------

The format of the address is: SHA256(Change_Address CAT Receiving_Address CAT Amount)

If Alice has 10 COMB in AliceWallet1, and wanted to send 2 COMB to Bob, she'll send her COMB to a Liquidity Stack with an address that is composed using AliceWallet2, BobWallet, 2 COMB. Her COMB will enter the Liquidity Stack, and 2 COMB will be sent to BobWallet, while the rest of the COMB will be sent to AliceWallet2.

Liquidity Stacks can be chained together to send COMB to more than one person using a single transaction. This is done by setting the Change Address to another Liquidity Stack.

Alice has 10 COMB, and wants to send 2 COMB to Bob, and 3 COMB to Cindy. First, she makes the following Liquidity Stack:

LStack1 = SHA256(AliceWallet2, CindyWallet, 3 COMB)

If she payed into this stack, Cindy would get 3 COMB, but Bob wouldn't get any. Instead, she makes a different Liquidity Stack:

LStack2 = SHA256(LStack1, BobWallet, 2 COMB)

Alice pays 10 COMB from AliceWallet1 into LStack2. The Stack triggers, and sends 2 COMB to Bob, and the remaining 8 COMB to the Change Address: LStack1. Once the 8 COMB reach LStack1 they trigger the stack; 3 COMB are sent to CindyWallet1, and the remaining 5 COMB are sent to AliceWallet2.

By combining Liquidity Stacks, we can theoretically create a transaction that sends COMB to every single COMB wallet in existence, without any additional fees.
# There will be collected some tips for smart contract developing from chats

## Contents
1. [About bounce toncoins back](tips.md#1-about-bounce-toncoins-back)
2. [Spend less gas in huge smart contracts](tips.md#2-spend-less-gass-in-huge-smart-contracts)

###  [1. About bounce toncoins back](https://t.me/tondev/44958)

If you have the `throw_if` function (with code != 0) in recv_internal triggered and the bounce flag set([tblkch.pdf 4.2.5](https://newton-blockchain.github.io/docs/tblkch.pdf)), all coins will be sent back


### [2. Spend less gas in huge smart contracts](https://t.me/tondev/45956)

`touch()` is tip to the compiler how best to organize the stack. The command puts a variable at top of the stack ([func docs](https://ton.org/docs/#/func/stdlib?id=impure_touch))

example:
In this [code](https://github.com/ton-blockchain/wallet-contract/blob/main/func/wallet-v4-code.fc#L90) `cs~touch();` will place `cs` on top of the stack and then the interaction with the variable will be cheaper

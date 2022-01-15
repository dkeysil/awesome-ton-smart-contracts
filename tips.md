# There will be collected some tips for smart contract developing from chats

## Contents
1. [About bounce toncoins back](tips.md#1-about-bounce-toncoins-back)

###  [1. About bounce toncoins back](https://t.me/tondev/44958)

If you have the `throw_if` function (with code != 0) in recv_internal triggered and the bounce flag set([tblkch.pdf 4.2.5](https://newton-blockchain.github.io/docs/tblkch.pdf)), all coins will be sent back

### 2. Information about charging gas fees

This information is based on this [discussion](https://github.com/DKeysil/awesome-ton-smart-contracts/issues/1)

`accept_message` simply sets the gas limit to the maximal possible value (the gas that can be bought by both original contract balance and message value, or, more commonly, the maximal gas amount allowed to use in single transaction) and also sets gas credit to zero.

In the case of external messages you need to accept the message in order to make transaction appear in the block (or, more precisely speaking, you need to somehow set gas credit to zero). You can accept message at any time during the TVM execution, even after calling `send_raw_message` primitive. The only way the fees may be charged from the account is to put a transaction into the blockchain, so it's the reason why "transactions" with no `accept_message` are "free".

In the case of internal messages the initial gas limit is set equal to the amount of gas that can be bought by message value. `accept_message` raises that limit. Even without `accept_message` you can spend more coins than the message value by sending some other messages which carry value. 

Using `set_gas_limit` in internal messages does not limit the possibility of spending more TON than came with the message when sending other messages that carry value. You can use `raw_reserve` in addition to gas limit to limit spendable amount of coins.

FunC docs:
- [`accept_message`](https://ton.org/docs/#/func/stdlib?id=accept_message)
- [`set_gas_limit`](https://ton.org/docs/#/func/stdlib?id=set_gas_limit)
- [`raw_reserve`](https://ton.org/docs/#/func/stdlib?id=raw_reserve)

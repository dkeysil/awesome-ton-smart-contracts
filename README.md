
# awesome-ton-smart-contracts

> list of links to articles and tools which can help you to start developing smart-contracts for [TON](https://ton.org) blockchain

## [На русском](ru)

## [Some tips from chats](tips.md)

### FAQ

#### What is smart-contract?
> Self executing program hosted at blockchain. For example in the TON blockchain every wallet is smart-contract.
> Smart-contract have state and persistent storage, which can contain any sort of variables.
> Smart-contract can store data, move funds to other smart-contracts, compute something.

#### How to start using or developing smart-contracts?
There are several options to start:

1. [easy] Toncenter/tonweb JS library - https://github.com/toncenter/tonweb
    With that library you can easily start with predefined Wallet contracts: create wallet, transfer funds, use subscribtion plugin
2. [medium] Disintar/toncli CLI utility - https://github.com/disintar/toncli
   1. It has well done documentation (deploy wallet by 2 commands) - https://github.com/disintar/toncli/blob/master/docs/quick_starat_guide.md
3. [medium] Tonwhales/ton TS library - https://github.com/tonwhales/ton
    
    With that library you can do same, what you can do with tonweb, 
    but it also have [repo](https://github.com/tonwhales/ton-contracts) with additional contract
    and [NFT contract](https://github.com/tonwhales/ton-nft)
4. [hard] You can use FunC and Fift (special developed for TON) languages

    Try to start with this [article](https://habr.com/ru/post/494528/) and [this](https://telegra.ph/Hello-World-TON-smart-contract-for-15-minutes-11-20)
    
    If you feel that you like it read [this section](README.md#about-fift-and-func-which-are-used-to-develop-smart-contracts)

#### Chats:
* [en, ru] [Biggest TON Tech chat](https://t.me/tondev) - technical discussion about TON
* [en, ru] [Chat about smart-contract developing](https://t.me/tonsc_chat)
* [en] [Tonic discord channel for English-speaking TON developers](https://discord.gg/tWxm8nrKt8)

### About fift and func which are used to develop smart contracts:
1. [Fift official docs](https://newton-blockchain.github.io/docs/fiftbase.pdf)
2. [FunC official docs](https://ton.org/docs/#/func)
3. [Fift instructions in C++](https://github.com/newton-blockchain/ton/blob/9875f02ef4ceba5b065d5e63c920f91aec73224e/crypto/fift/words.cpp#L2723-L3110)

### About TL-B

TL-B (Type Language - Binary) serves to describe the type system, constructors, and existing functions. For example we can use TL-B schemes to build binary structures associated with the TON blockchain. Special TL-B parsers can read schemes to deserialize binary data into different objects. (definition from the [documentation](https://github.com/tonuniverse/TL-B-docs))

1. [Documentation with examples](https://github.com/tonuniverse/TL-B-docs)
2. [Some about TL-B are described in tvm.pdf](https://newton-blockchain.github.io/docs/tvm.pdf)

### Smart contracts examples:
1. [Official smart contracts (wallets, givers, etc.)](https://github.com/newton-blockchain/ton/tree/master/crypto/smartcont)
2. https://github.com/ton-blockchain/wallet-contract
3. Telegram contests, a lot of different smart contracts
    1. https://contest.com/blockchain
    2. https://contest.com/blockchain-2 & https://contest.com/blockchain-2-bonus
4. [Gambling smart contract](https://github.com/deNULL/ton-gamble)
5. [Auction smart contract](https://github.com/deNULL/ton-auction)
6. [Smart contract with text sending](https://github.com/akifoq/ton-samples/blob/master/text/main.fc)
7. [Example of simple token contract](https://github.com/akifoq/TonToken)
8. [Official draft fungible, non-fungible token contracts](https://github.com/ton-blockchain/token-contract)
    * [NFT standart discussion](https://github.com/ton-blockchain/TIPs/issues/62)
9. [Wallet v4 contract (Supports external plugins installation)](https://github.com/ton-blockchain/wallet-contract)
    * [Subscribtion plugin](https://github.com/ton-blockchain/wallet-contract/blob/main/func/simple-subscription-plugin.fc)
10. [TRC-20 (like ERC-20) token contract](https://github.com/cod1ng-studio/TRC20)
11. [Examples of using fift runvm to run transactions](https://github.com/disintar/toncli/tree/master/src/toncli/projects/external_code)

### Articles about smartcontracts:
1. Official guidelines - https://ton.org/docs/#/howto/smart-contract-guidelines
2. Develop, deploy and use lottery smart contract - https://habr.com/ru/post/494528/
3. Extend wallet smart contract and deploy it - https://telegra.ph/Hello-World-TON-smart-contract-for-15-minutes-11-20

### Deploy smart contract:
1. [Smart contract deployer](https://deployer.tonsc.org/) by t.me/ProjectManageRR
2. [TON CLI](https://github.com/disintar/toncli) by t.me/disintar
3. [Documented generate.fif](https://gist.github.com/tvorogme/fdb174ac0740b6a52d1dbdf85f4ddc63) by t.me/disintar
4. [Lite-client installation guide](https://ton.org/docs/#/howto/getting-started). Via lite-client you can send .boc file to deploy smart contract to blockchain

### IDE plugins and syntax highlighting
1. [Intellij Platform plugin](https://github.com/andreypfau/intellij-ton)
2. [neovim FunC syntax highlighting](https://github.com/PythoNyashka/neovim-ton-dev)
3. Visual Studio Code [fift syntax highlighting](https://marketplace.visualstudio.com/items?itemName=dotcypress.language-fift)
    and [FunC syntax highlighting](https://marketplace.visualstudio.com/items?itemName=raiym.FunC)


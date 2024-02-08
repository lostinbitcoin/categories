---
title: ライトニング・チャネル
taxonomy:
    category:
        - glossary
---

## Lightning Channel
2,100 sats

A Lightning channel is a connection between two parties, and the Lightning Network is composed of thousands of channels. Lightning transactions are sent back and forth over channels and are used to recalibrate the bitcoin balances of each party in this channel. All bitcoin in a channel belongs to one of the two parties. Lightning channels are called bidirectional payment channels because both parties can send and receive bitcoin across the channel. In order to open a Lightning channel, two parties, say Alice and Bob, cooperatively construct a 2-of-2 multisig address. Any bitcoin sent to this address requires two signatures, one from each party, in order to be spent. Imagine Alice and Bob open a channel and deposit 1 BTC each. If Alice now wishes to pay Bob 0.5 BTC, she signs a transaction spending from the multisig address. This transaction has two outputs: Bob will receive 1.5 BTC and Alice will receive 0.5 BTC. Since spending from the multisig address requires two signatures, this is not yet a valid transaction, and Alice cannot broadcast it to the Bitcoin network. Instead, she sends the partially-signed transaction, called a commitment transaction, to Bob, who keeps it but does not broadcast it. Alice has paid Bob 0.5 BTC, but Bob has not settled this payment to the Bitcoin blockchain. This is why Lightning transactions are so cheap: they do not require miners to confirm each transaction in a block. A Lightning channel can be closed at any point by publishing the latest unbroadcast commitment transaction. This transaction will send the bitcoin from multisig address to each party in the correct amount, representing the net flow of bitcoin across all of the Lightning transactions that occured on this channel.

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.

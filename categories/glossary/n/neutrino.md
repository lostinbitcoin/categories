---
title: ニュートリノ
taxonomy:
    category:
        - n
---

## Neutrino
2,100 sats

Neutrino is a proposed light client protocol which offers privacy and efficiency improvements over existing light client designs, notably Simplified Payment Verification (SPV).

A typical light client requests data about transactions and blocks in which it is interested from either a central server or other nodes in the Bitcoin network. Often, when a light client requests such information, they leak their addresses and transactions to the server, sacrificing privacy. Several schemes have been proposed and implemented by different wallets. So far, none have emerged as a standard.

In order to preserve a light client’s privacy, the Neutrino protocol has the server send all transaction outputs in a block to the light client, leaving the light client to decide whether there are any transactions of interest. If there are such transactions, the light client requests the full block to be sent, in order to trustlessly verify that the transaction of interest was included in the block. This scheme preserves privacy better but requires significantly more bandwidth and compute power than the existing SPV scheme.

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.

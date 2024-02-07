---
title: ペイジョイン (P2EP)
taxonomy:
    category:
        - p
---

## PayJoin (P2EP)
2,100 sats

PayJoin, also known as Pay-to-Endpoint (P2EP), is a special type of Bitcoin transaction where both the sender and receiver contribute inputs in order to break the common input ownership heuristic, an assumption used to strip privacy from bitcoin users.

The common input ownership heuristic is one of the most commonly used heuristics used in chain analysis. It assumes that, in a given transaction, all inputs were signed by the same entity. Until now, this has been a relatively safe assumption, as multisig usage remains low. The P2EP proposal was created in order to break this assumption and improve Bitcoin privacy.

Although P2EP’s syntax resembles Bitcoin’s many script types, P2EP is not a script. Rather, it is a protocol which allows two bitcoin users to transact in a privacy preserving manner. Using a peer-to-peer channel, such as an onion address, a sender and a receiver can exchange information about the UTXOs they would like to use as inputs in a transaction. They can then cooperatively construct and sign the transaction using the partially signed Bitcoin transaction (PSBT) standard defined in BIP 174. The resulting transaction will simply resemble a typical transaction with multiple inputs and multiple outputs.

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.

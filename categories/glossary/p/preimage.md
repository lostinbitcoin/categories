---
title: プリイメージ
taxonomy:
    category:
        - glossary
---

## Preimage
2,100 sats

A preimage is the data that is input into a hash function to calculate a hash. Since a hash function is a one-way function, the output, the hash, cannot be used to reveal the input, the preimage.

Any piece of data can be used as a preimage. For example, addresses are created by taking the hash of a public key. Likewise, a block header is the preimage for a block’s Proof-of-Work, which is a hash.

Hashes are often used as commitments to preimages, because the commitment to the preimage can be published without revealing the preimage. For example, if bitcoin is sent to a P2PKH address, which is the hash of a public key, that bitcoin is committed to a certain public key even though the public key is not known by anyone but the owner, who we will call Alice. When Alice wishes to spend the bitcoin, she publishes the preimage, the public key, along with a signature, proving their control of the corresponding private key. With those two pieces of information, anyone validating the blockchain can verify that the bitcoin actually belonged to that public key, and that Alice controls that public key.

The Lightning Network also uses preimages as proof that a Lightning invoice has been paid. In this context, the hashed time locked contract (HTLC) serves as the commitment, promising to pay a routing node a fee in exchange for routing the desired payment, while the preimage, the (unhashed) time-locked contract, is the proof that the commitment has been satisfied. HTLCs are sent from the payer node to the routing node, to the receiving node, who returns the preimage of the HTLC to the routing node, who uses the preimage to claim the fee they were promised.

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.

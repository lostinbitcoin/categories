---
title: 導出パス
taxonomy:
    category:
        - d
---

## Derivation Path
2,100 sats

A derivation path is a piece of data which tells a Hierarchical Deterministic (HD) wallet how to derive a specific key within a tree of keys. Derivation paths are used as a Bitcoin standard and were introduced with HD wallets as a part of BIP 32.
Each key in the tree of a HD wallet can be described by its derivation path, which contains information about a key’s depth and index—where it resides within the tree structure. The master key is simply refered to as ’m'.

For example, the first child of the master key has a derivation path of “m/0”, and the fifth child of that child key has a derivation path of “m/0/4”. The depth of each child is given by the number of levels—each separated by a slash—between itself and the master key, and the index of each child is its number at that level, starting with zero. The key at “m/0/4” has a depth of 2 and an index of 4.

Bitcoin Improvement Proposal 32 allows for 2^32 children keys to be derived by each parent key. Children numbered 0-2^31 - 1 are considered unhardened, meaning a parent public key can derive child public keys. However, for children numbered 2^31-2^32 - 1, parent public keys are incapable of deriving children. Only the parent private key is capable of deriving a child private key, which can then be used to derive the child public key. This specification allows for flexbility within the HD wallet standard. When a key is hardened, it is denoted with a prime symbol ‘.

For example, the first hardened child of the master key has a derivation path of “m/0’”, and that key’s fifth unhardened child has a derivation path of “m/0'/4”.

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.

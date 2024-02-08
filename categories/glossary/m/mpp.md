---
title: マルチパスペイメント (MPP)
taxonomy:
    category:
        - glossary
---

## Multi-Path Payment (MPP)
2,100 sats

A multipath payment (MPP) is a type of Lightning payment which is executed as an atomic set of smaller payments. These smaller payments are more reliable and easier to execute; they also offer privacy advantages, as a set of multipath payments is harder to track than a single payment. Multipath payments are atomic, meaning they must all succeed, or they all fail. This is done to avoid the confusion of partial payments.

Multipath payments solve a few issues faced by the Lightning Network. When a Lightning channel is established, it has a defined capacity. Each user can send only as much bitcoin as they have committed to the channel. Thus, larger payments strain the capacity of channels and can fail if capacity is insufficient. This problem is especially salient for routed payments, which traverse several channels to get from sender to receiver. In order to reduce the strain of large payments, Lightning implementations allow users or their Lightning wallets to break the payment up into smaller payments. Each payment can be routed across a different path, distributing the strain across many different channels.

The term multipath payment is a general term, and MPP is not fully implemented on the Lightning Network. There exist different proposals and implementations of this concept across the different Lightning implementations, including Basic MPP and Atomic Multipath Payments (AMP). These different versions attempt to solve several security and reliability issues with the basic concept of multipath payments.

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.

---
title: シュノア署名
taxonomy:
    category:
        - s
---

## Schnorr Signature
2,100 sats

Schnorr is a type of digital signature scheme similar to the ECDSA scheme used by Bitcoin since its inception. The Schnorr scheme presents several advantages over ECDSA, and is thus currently in the process of being implemented in Bitcoin via the Taproot upgrade.

Firstly, the Schnorr scheme is provably secure and non-malleable, two improvements over ECDSA. Secondly, compared to ECDSA signatures, Schnorr signatures take less time to verify. Schnorr signatures and public keys can be aggregated, meaning that multiple parties with unique private keys can sign the same message with much greater efficiency. Thanks to this feature, Schnorr signatures can be verified in batches instead of individually, further speeding up verification.

Key and signature aggregation also enable privacy gains by obscuring the number of signatures present on a transaction. Finally, Schnorr signatures are also smaller than ECDSA signatures, offering savings on fees for those spending Schnorr outputs.

When Bitcoin was invented, the Schnorr scheme was still patent-protected, and thus Satoshi Nakamoto decided to use ECDSA as the signature scheme for Bitcoin. The Schnorr patent has since expired, and Schnorr is currently in the process of being implemented in Bitcoin.

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.

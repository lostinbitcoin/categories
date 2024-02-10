---
title: 署名
taxonomy:
    category:
        - glossary
---

## Signature
2,100 sats

A digital signature is similar to a physical signature in theory, yet far more secure and trustworthy. Like its physical counterpart, a digital signature indicates approval of the data being signed. Unlike a physical signature, a digital signature cannot be copy-pasted because a signature is unique for each piece of data being signed.

For example, if you create a signature for the text “Hello”, this signature is invalid for the text “Hey”. This trait allows digital signatures to be publicized without risk of fraud.

There are three parts to a digital signature: the data being signed, the public key of the signer, and the signature itself. The data can be anything digital, including text, an image, an audio file, and more. The public key is a pseudonymous form of identity, informing the public that the owner of the corresponding private key has signed this message. Lastly the signature is mathematical proof that the owner of the public key and the corresponding private key signed the exact data provided.

The magic here is that the private key is required to create the signature, but not required to verify it. Anyone can verify that the signature is valid using only the public key. Furthermore, since the signature is generated using the hash of the data it is signing, verifiers can be sure that the data provided is unaltered since it was signed.

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.

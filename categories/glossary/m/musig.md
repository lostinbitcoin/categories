---
title: MuSig
taxonomy:
    category:
        - glossary
---

## MuSig
2,100 sats

MuSig（ミューシグ）は、[タップルート](https://lostinbitcoin.sakuraweb.com/glossary/taproot/)を活用して[マルチシグ](https://lostinbitcoin.sakuraweb.com/glossary/multisig/)に対応する[公開鍵](https://lostinbitcoin.sakuraweb.com/glossary/public_key/)と[署名](https://lostinbitcoin.sakuraweb.com/glossary/signature/)を作成するための[プロトコル](https://lostinbitcoin.sakuraweb.com/glossary/protocol/)です。この技術は、[シュノア署名](https://lostinbitcoin.sakuraweb.com/glossary/schnorr_signature/)と公開鍵の集約技術を使用しており、タップルートのアップグレードが有効化されることで利用可能になります。

MuSigの最大の特徴は、マルチシグトランザクションが単一署名の[トランザクション](https://lostinbitcoin.sakuraweb.com/glossary/transaction/)と区別がつかなくなる点です。従来のマルチシグでは、P2SH（Pay-to-Script-Hash）スクリプトを使用して各署名者の公開鍵と署名をブロックチェーン上で開示する必要がありましたが、MuSigではこれが不要になります。MuSigでは各参加者の公開鍵を1つの公開鍵に統合し、その公開鍵に対して全員で1つの署名を作成するためです。この結果、[ブロックチェーン](https://lostinbitcoin.sakuraweb.com/glossary/blockchain-2/)上では単一署名のトランザクションと見分けがつきません。

この特性によって、MuSigはプライバシーを大幅に向上させます。しかもこれはMuSigユーザーに限った話ではなく、MuSigを使用することで、単一署名トランザクションと区別がつかなくなるため、[チェーン分析](https://lostinbitcoin.sakuraweb.com/glossary/chain_analysis/)で利用される多くの推論手法（ヒューリスティック）が無効化されます。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.

---
title: MuSig
taxonomy:
    category:
        - glossary
---

## MuSig
2,100 sats

MuSig（ミューシグ）は、[タップルート](http://lostinbitcoin.jp.testrs.jp/staging/glossary/taproot/)を活用して[マルチシグ](http://lostinbitcoin.jp.testrs.jp/staging/glossary/multisig/)に対応する[公開鍵](http://lostinbitcoin.jp.testrs.jp/staging/glossary/public_key/)と[署名](http://lostinbitcoin.jp.testrs.jp/staging/glossary/signature/)を作成するための[プロトコル](http://lostinbitcoin.jp.testrs.jp/staging/glossary/protocol/)です。この技術は、[シュノア署名](http://lostinbitcoin.jp.testrs.jp/staging/glossary/schnorr_signature/)と公開鍵の集約技術を使用しており、タップルートのアップグレードが有効化されることで利用可能になります。

MuSigの最大の特徴は、マルチシグトランザクションが単一署名の[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction/)と区別がつかなくなる点です。従来のマルチシグでは、P2SH（Pay-to-Script-Hash）スクリプトを使用して各参加者の公開鍵や署名を記録する必要がありましたが、MuSigではこれが不要になります。MuSigでは各参加者の公開鍵を1つの公開鍵に統合し、その公開鍵に対して全員で1つの署名を作成するためです。この結果、[ブロックチェーン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/blockchain-2/)上では単一署名のトランザクションと見分けがつきません。

この特性によって、MuSigはプライバシーを大幅に向上させます。たとえば、従来のP2SHスクリプトを使用する場合、マルチシグトランザクションではすべての署名と公開鍵がブロックチェーン上に公開され、誰が取引に関与しているかが分かる場合がありました。しかし、MuSigを使用すると、単一署名トランザクションと区別がつかなくなるため、[チェーン分析](http://lostinbitcoin.jp.testrs.jp/staging/glossary/chain_analysis/)で利用される多くの推論手法（ヒューリスティック）が無効化されます。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.

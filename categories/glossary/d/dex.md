---
title: DEX (分散型取引所)
taxonomy:
    category:
        - glossary
---


## Decentralized Exchange (DEX)
2,100 sats

DEX（Decentralized Exchangeの略、分散型取引所）を利用すれば、取引所に資産の所有権を委譲したり、取引を検閲されてプライバシーを侵害されることなく[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin-2/)を他の資産に交換できます。DEXが[マネーロンダリング防止（AML）](http://lostinbitcoin.jp.testrs.jp/staging/glossary/aml/)の名目で、ユーザーから住所、氏名、電話番号、IDなどの個人情報を収集することはありません。

DEXの分散の度合いはさまざまです。単に[ノンカストディアル](http://lostinbitcoin.jp.testrs.jp/staging/glossary/non_custodial/)型というだけで、ユーザー間でトラブル発生時には仲裁に入る集権的な主体が運営するものもあれば、完全に分散化された[プロトコル](http://lostinbitcoin.jp.testrs.jp/staging/glossary/protocol/)として稼働するものもあります。通常DEXでは、資産の交換はユーザー間で直接行われるため、DEXが仲介者として資産を預かることはありません。

多くのDEXでは、ビットコインの売り手が売却するビットコインを2-of-3[マルチシグ](http://lostinbitcoin.jp.testrs.jp/staging/glossary/multisig/)アドレスに送り、その3つの[秘密鍵](http://lostinbitcoin.jp.testrs.jp/staging/glossary/private_key/)を売り手、買い手、DEXがそれぞれ1つずつ持ちます。売り手が買い手から支払いを受け取ると、両者がマルチシグアドレスにから買い手のアドレスにビットコインを移転する[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction/)に[署名](http://lostinbitcoin.jp.testrs.jp/staging/glossary/signature/)します。
もし売り手または買い手が不正を行った場合、被害者はDEXに異議を申し立て、DEXが保持する鍵でトランザクションに署名して紛争を解決します。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.

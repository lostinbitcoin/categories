---
title: ペイジョイン (P2EP)
taxonomy:
    category:
        - glossary
---

## PayJoin (P2EP)
2,100 sats

ペイジョインはPay-to-Endpoint（P2EP）と呼ばれる特殊なタイプの[トランザクション](https://lostinbitcoin.sakuraweb.com/glossary/transaction/)で、送信者と受信者の両者がトランザクションの入力に資金を提供する仕組みを指します。これによって、ビットコインユーザーのプライバシーを損なう原因となる「共通入力所有者ヒューリスティック」（※[チェーン分析](https://lostinbitcoin.sakuraweb.com/glossary/chain_analysis/)で用いられる[ビットコイン](https://lostinbitcoin.sakuraweb.com/glossary/bitcoin/)所有者の推測手法）を破ることができます。

「共通入力所有者ヒューリスティック」とはチェーン分析でよく使われる仮定の一つで、トランザクション内のすべての入力が同じ主体によって[署名](https://lostinbitcoin.sakuraweb.com/glossary/signature/)されていると推測するものです。これは[マルチシグ](https://lostinbitcoin.sakuraweb.com/glossary/multisig/)の利用率が低いこともあって、これまでは比較的信頼できる推測とされてきました。ペイジョインはこの前提を破り、ビットコインのプライバシーを向上させることを目的としています。

ペイジョインの構文はビットコインの多くの[ビットコインスクリプト](https://lostinbitcoin.sakuraweb.com/glossary/bitcoin_script/)形式と似ていますが、ビットコインスクリプトそのものではありません。むしろ、プライバシーを保ちながら2人のビットコインユーザーが取引できる[プロトコル](https://lostinbitcoin.sakuraweb.com/glossary/protocol/)です。送信者と受信者は[匿名性](https://lostinbitcoin.sakuraweb.com/glossary/anonymity/)の高いTorネットワークで使用されるオニオンアドレスのような[ピアツーピア (P2P)](https://lostinbitcoin.sakuraweb.com/glossary/p2p/)チャネルを利用して、トランザクションの入力に用いる[未使用トランザクションアウトプット（UTXO）](https://lostinbitcoin.sakuraweb.com/glossary/utxo/)の情報を交換します。その後、[BIP174](https://lostinbitcoin.sakuraweb.com/glossary/bip174/)で定義された部分署名ビットコイントランザクション（PSBT）標準を使用して、協力してトランザクションを構築し署名します。最終的なトランザクションは、複数の入力と出力を持つ通常のトランザクションと外見上は区別がつきません。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.

---
title: M-of-N
taxonomy:
    category:
        - glossary
---

## M-of-N
2,100 sats

M-of-Nとは、[マルチシグ](http://lostinbitcoin.jp.testrs.jp/staging/glossary/multisig/)における正確な設定条件を示す表現で、Mは必要な[署名](http://lostinbitcoin.jp.testrs.jp/staging/glossary/signature/)の数を、Nは署名に使用できる[公開鍵](http://lostinbitcoin.jp.testrs.jp/staging/glossary/public_key/)の総数を表します。マルチシグアドレスは、複数の[秘密鍵](http://lostinbitcoin.jp.testrs.jp/staging/glossary/private_key/)の署名が必要な特別な[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)アドレスです。 通常のシングルシグ設定（1つの秘密鍵のみを使用する設定）とは異なり、一部のビットコインユーザーは、1つの鍵が破られても資金を失わないように、このマルチシグ設定を利用します。

例えば、アリス、ボブ、チャーリーの3人が共同で会社を設立し、ビットコインを共同管理したいと考えているとします。この場合、1人だけで資金を不正に持ち出せないよう、それぞれが1つずつ公開鍵を提供して共有します。 また、会社の運営は多数決に基づくべきと決め、3つの公開鍵のうち2つの署名があれば資金を動かせるよう設定したと仮定します。この条件（M=2, N=3）はスクリプトとして記述され、これをハッシュ化することで、3人が会社の資金を送金するための[アドレス](http://lostinbitcoin.jp.testrs.jp/staging/glossary/address/)が生成されます。この場合の設定は「2-of-3マルチシグ」と表します。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.

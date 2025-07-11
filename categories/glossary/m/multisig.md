---
title: マルチシグ
taxonomy:
    category:
        - glossary
---

## Multisig
2,100 sats

標準的なビットコイン[トランザクション](https://lostinbitcoin.sakuraweb.com/glossary/transaction/)では、単一の[アドレス](https://lostinbitcoin.sakuraweb.com/glossary/address/)宛に[ビットコイン](https://lostinbitcoin.sakuraweb.com/glossary/bitcoin/)を送ります。このビットコインを使うには、アドレス生成に使われた[公開鍵](https://lostinbitcoin.sakuraweb.com/glossary/public_key/)の対の[秘密鍵](https://lostinbitcoin.sakuraweb.com/glossary/private_key/)による[署名](https://lostinbitcoin.sakuraweb.com/glossary/signature/)が求められます。

このような標準的なトランザクション以外にも、複数の秘密鍵による複数の署名を使用条件とするトランザクションを作成することも可能です。これにより、家族、会社、提携関係にある事業者などの間で、ビットコインを共同管理することが可能になります。

このような条件を付したトランザクションは、マルチシグネチャー（複数署名）、略してマルチシグと呼ばれます。[m-of-n](https://lostinbitcoin.sakuraweb.com/glossary/m_of_n/)マルチシグと表記されることも多く、これはマルチシグアドレス宛に送られたビットコインを使用するには、アドレス生成に使われたn個の秘密鍵のうち、少なくともm個の秘密鍵による署名が必要であることを表します。例えば「2-of-3」マルチシグでは、3つの公開鍵からアドレスを生成し、これら3つの公開鍵に対応する3つの秘密鍵のうち、任意の2つによる署名が揃えば、マルチシグアドレスにロックされたビットコインを使うことができます。

ほとんどのマルチシグトランザクションはP2SHとして実行され、アドレスは「3」から始まります。この場合、マルチシグアドレスの生成に用いる鍵を指定するスクリプトは、アドレスにロックされたビットコインが使われるまでブロックチェーンには記録されません。つまり、マルチシグの鍵の所有者は、どの鍵からアドレスを生成したかを忘れてしまうと、アドレスにロックしたビットコインを使えなくなってしまいます。P2SHで構築するマルチシグは、ロックしたビットコインを引き出して使用することから、RedeemScriptと呼ばれます。

具体例を見てみましょう。アリス、ボブ、チャーリーの3人は会社を設立し、ビットコインを共同管理したいと考えます。ビットコインの不正流用を防ぐため、3人はそれぞれが持つ公開鍵を1つずつ提供してマルチシグアドレスを構築します。3人で決めた多数決に基づく運営という会社方針を反映して、共同管理するビットコインの送金には、各々が提供した3つの公開鍵に対応する秘密鍵のうち、任意の2つによる署名を求めることにしました。この条件をスクリプトに変換し、ハッシュすることで、3人が共同管理するマルチシグアドレスが生成されます。これは2-of-3マルチシグの一例です。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.

---
title: コインジョイン
taxonomy:
    category:
        - glossary
---

## CoinJoin
2,100 sats

コインジョインは複数のユーザーが共同で実行する大口の[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction/)です。参加者が拠出した[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)を統合して均等分割した後、拠出相当を送り返します。どの参加者がどのアウトプットを受け取ったのか判別するのは困難で、[ブロックチェーン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/blockchain/)分析企業が用いるヒューリスティクスを無効にします。コインジョインに参加することで、ビットコイン（[UTXO](http://lostinbitcoin.jp.testrs.jp/staging/glossary/utxo/)）の帰属を曖昧にし、プライバシーを守ることができます。
[カストディアル](http://lostinbitcoin.jp.testrs.jp/staging/glossary/custodial/)型の[ミキシング](http://lostinbitcoin.jp.testrs.jp/staging/glossary/mixing/)とは異なり、コインジョインでは運営主体にビットコインを預ける必要はありません。ビットコインは常に参加者の管理下にあります。
実例を見てみましょう。コインジョイントランザクションのインプットは、参加者それぞれが拠出したビットコインです。それらを統合後に均等分割したアウトプットを、拠出数量に応じて参加者の[アドレス](http://lostinbitcoin.jp.testrs.jp/staging/glossary/address/)に返信します。たとえば、参加者5名がそれぞれ1[BTC](http://lostinbitcoin.jp.testrs.jp/staging/glossary/btc/)、2BTC、3BTC、4BTC、5BTCを拠出したとします。インプットは５つです。インプットの合計15BTCを1BTCずつ15のアウトプットに分割します。参加者は全員、1BTCのアウトプットを受け取ります。2BTC拠出した人は2つ、5BTCなら5つのアウトプットを受け取ります。拠出数量に関わらず、参加者全員が同額のアウトプットを受け取ることとなり、各アウトプットの所有者の特定が実質不可能となります。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.

---
title: アドレス
taxonomy:
    category:
        - glossary
---

## Address
2,100 sats

<div><button class="zap-button" data-npub="npub1x3x7spzvt6yflg4l825agplakkyv8h62h5jsl9qq7ghxlcr490wqz4qfw6" data-relays="wss://relay.damus.io,wss://relay.snort.social,wss://nostr.wine,wss://relay.nostr.band">Zap Me ⚡</button><a href="https://twitter.com/sishamo_moyashi">@sishamo_moyashi</a></div>

アドレスは[ビットコイン](https://lostinbitcoin.sakuraweb.com/glossary/bitcoin/)を受け取るために使用され、英数字から成る文字列として表されます。[公開鍵](https://lostinbitcoin.sakuraweb.com/glossary/public_key/)とアドレスはしばしば混同されますが、アドレスは公開鍵のハッシュであり、ビットコインを受け取るには公開鍵ではなくアドレスが使用されます。厳密に言うと、アドレスは単なる公開鍵のハッシュというわけではありませんが、技術的な話なので割愛します。

ビットコイン[ウォレット](https://lostinbitcoin.sakuraweb.com/glossary/wallet/)を使用すると、ユーザーは必要な数だけアドレスを生成できるだけでなく、指定したアドレスにビットコインを送信できます。アドレスに送られたビットコインは、そのアドレスを導出した[秘密鍵](https://lostinbitcoin.sakuraweb.com/glossary/private_key/)の所有者のみが使用できます。

注意：プライバシーを保護するために、アドレスの再利用は避けてください。ビットコインを受け取るたびに、ウォレットで新しいアドレスを生成することをおすすめします。

ビットコインアドレスはいくつかの異なる[スクリプト](https://lostinbitcoin.sakuraweb.com/glossary/bitcoin_script/)を表すことができます。アドレスはスクリプトタイプを伝えるためにエンコードされ、プレフィックスが付けられます。レガシーアドレスはBase58を使用します。レガシーアドレスが公開鍵のハッシュ、いわゆるP2PKHアドレスの場合は「1」で始まります。あまり多くはありませんが、スクリプトのハッシュである場合は「3」で始まります。[SegWit](https://lostinbitcoin.sakuraweb.com/glossary/segwit/)アドレスはすべてBech32でエンコードされ、プレフィックス「bc1」で始まります。ビットコインの送付先としてアドレスが入力されると、ウォレットはアドレスの種類を調べて適切なスクリプトを作成します。このスクリプトはscriptPubKeyと呼ばれ、送金額に追加されます。これら2つのデータ（金額とscriptPubKey）がアウトプットになります。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.

---
title: LedgerやTrezorからのCOLDCARDへの移行
taxonomy:
    category:
        - how-to
        - wallet
    post_tag:
        - intermediate
---

## COLDCARD ユーザーガイド

<button class="zap-button" data-npub="npub1uyf6ghmjy8p8mnt8jhutgh4jtjvzn7euwjf4yvpwuzwan5jl8xysnvsmuw" data-relays="wss://relay.damus.io,wss://relay.snort.social,wss://nostr.wine,wss://relay.nostr.band">Zap Me ⚡</button>

|  ![Category](/_images/category.png)  | LedgerやTrezorからのCOLDCARDへの移行 |  ![Tag](/_images/tag.png)  |  中級  | ![Time](/_images/timer.png)  |  20分  |
| ---- | ---- | ---- | ---- | ---- | ---- |

*本記事は [Coldcard 公式サイト](https://coldcard.com/)「[Migrate from Ledger or Trezor to COLDCARD](https://coldcard.com/docs/migrate-wallet)」を [@katakoto](https://twitter.com/katakoto)が翻訳、一部加筆したものです。*

# ユーザーガイド

## **LedgerやTrezorからのCOLDCARDへの移行**

![ColdCardMigrationGuide_1.jpg](/_images/ColdCardMigrationGuide_1.jpg)

**はじめに**

コールドストレージをレベルアップして **COLDCARD®**に移行しよう！

このチュートリアルでは、Ledger または Trezor [ハードウェアウォレット](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ha/#hardware_wallet)（移行元ウォレット）で生成された[ウォレット](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-a/#wallets)の[シード](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-sa/#seed)を、空の COLDCARD（移行先ウォレット）に保存する方法を説明します。

使用しているデバイスや、相談している相手によっては、ウォレットのシードの単語のことをリカバリーフレーズや、リカバリーシード、シードフレーズ、[ニモニック](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-na/#mnemonic)、バックアップフレーズなどと呼んでいるかもしれません。そうしたシードの単語リストが、これからあなたのCOLDCARDに転送されるものです。

**アルトコインはサポート対象外**

COLDCARDはアルトコインをサポートしていません。ハードウェアウォレットのシードをアルトコインでも使用していた場合は、移行するシードに紐づいたアルトコインのアカウントや資金を どのように保管するか決定する必要があります。

[動画: LedgerやTrezorからのCOLDCARDへの移行方法](https://youtu.be/0kbxP-VIMjc)

### **移行されないもの**

COLDCARDにシードを直接入力するため、移行後のCOLDCARDに保持される唯一の元のウォレット情報は、元のウォレットが生成したシードワードのリストのみです。

シードの移行には以下が含まれません：

- アルトコイン・アカウント情報
- 元のウォレットのPIN
- パスフレーズ（適用していた場合）
- カスタムまたは非標準の派生パス（適用していた場合）
- 元のウォレットの名前

COLDCARDへの移行後、既存の[パスフレーズ](https://coldcard.com/docs/passphrase)をシードワードに適用したり、[カスタム派生パス](https://coldcard.com/docs/paths)を指定したり、[COLDCARDにニックネームを設定](https://coldcard.com/docs/settings#set-nickname)することができます。

## **手順**

あなたは以下のことについて基本的な知識を持っている必要があります:

- あなたの移行元のウォレット
- あなたの移行元のウォレットが使用するアプリ (例: Trezor Suite や Ledger Live)
- [デスクトップやモバイルウォレット](https://coldcard.com/docs/compatible-wallets)のアプリ

## **必要なもの**

### **安全な場所と十分な時間**

シードワードを表示する際には常に、誰にも見られない安全な場所であることを確認してください。他の人やカメラにシードワードを見せないでください。シードワードは、あなたのウォレットに関する最も重要な情報であり、誰かがあなたのシードワードを持っていれば、あなたのビットコインは奪われてしまう可能性があります。

プロセスは複雑ではないですが、シードワードを入力する場合は、十分な時間を取って急がないようにしてください。24個のシードワードを使っている場合には、これは特に重要です。

### 移行元**ウォレットのアイテムと情報**

- シードワード（紙によるバックアップ、[金属バックアッププレート](https://bitcoinseedbackup.com/)など）
- 転送するシードで使用したパスフレーズ
- ビットコインの残高
- 受信アドレス

オプションですが、問題が発生した場合に役立つアイテム：

- 移行元ハードウェアウォレット
- 電源とデバイス通信用のUSBケーブル（通常はMicro USBまたはUSB-C）
- 移行元ウォレットのアプリが実行されているコンピューターまたはスマートフォン

### 移行先**COLDCARDのアイテム**

- シードが設定されていない空の[COLDCARD](https://store.coinkite.com/store/coldcard)
- USB接続の電源（[Mk3 = Micro USB](https://coldcard.com/docs/hardware)、[Mk4 = USB-C](https://coldcard.com/docs/coldcard-mk4)）：
    - ACアダプタに接続されたUSBケーブル
    - コンピューターに接続された[電源専用](https://store.coinkite.com/store/coldcard)USBケーブル
    - 9ボルトバッテリーに取り付けられた[COLDPOWER™](https://usbcoldpower.com/)アダプタ
- [Electrum](https://coldcard.com/docs/community-guides#electrum)またはお好みの[デスクトップウォレット](https://coldcard.com/docs/compatible-wallets)
- microSDカード、最大容量32GB（[産業用グレード推奨](https://store.coinkite.com/store/coldcard))

## 実行すること

### **始める前に**

### **あなたのCOLDCARDを確認してください**

使用するCOLDCARDに**シードが設定されていない**ことを確認してください。これは、あなたが新しく購入したCOLDCARDである場合、もしくはCOLDCARDのシードを破壊してある場合とがあります。履歴が不明な以前誰かに保持されていたり使用されていたCOLDCARDには、シードを移行しないでください。

空のCOLDCARDは、サインイン後に以下の選択肢を持つメインメニューを表示します：

- New Wallet
- Import Existing
- Help
- Advanced
- Settings

COLDCARDのシードが設定されると、メインメニューのオプションが変更されます。

PINが設定されていない新しいCOLDCARDをお持ちの場合は、[クイックスタートガイド](https://coldcard.com/docs/quick)の初期PINセクションまで従ってください。新しいウォレット(New Wallet)またはインポートセクション(Import Existing)に到達したら、このチュートリアルに戻ってください。新しいシードワードを選択 *しないでください。*

### **シードワードリストを確認してください**

リストは12、18、または24語である必要があります。そうでない場合は、間違いがある可能性があります。ソースを再確認してください。この問題に対するサポートは提供できません。

Ledgerデバイスをお持ちの場合は、Recovey Checkアプリを実行してエラーを特定することができる場合があります。

Trezorデバイスをお持ちの場合は、アプリ上でCheck Backup、またはAdvanced Recoveryを実行してエラーを特定することができます。

エラーを特定できない場合でも、デバイスにアクセスしてトランザクションを行うことができる場合は、COLDCARDで[new wallet]を作成し、ビットコインを新しいウォレットに送信してください。

正しいシードワードリストにアクセスする手段や、元のウォレットでトランザクションを完了する方法がない場合、ビットコインを回復することはできません。

### **シードワードを入力する**

1. COLDCARDを電源に接続し、PINを入力します。
2. `Import Existing`を選択します。
3. ワードリストの単語数を選択します。
4. 矢印を使って数字キー（**5** = 上、**8** = 下、**7** = ページアップ、**9** = ページダウン）を使って、Word 1の最初の文字を選択し、オプションを絞り込み、完全な単語を選択できるようにします。
    - **例**：あなたの単語は*keen*です。画面を下にスクロールして、`k-`が表示されたら、`k-`を選択してください。`kangaroo`、`kee-`、Kで始まる他の単語が表示されます。`kee-`を選択してください。残っているのは`keen`と`keep`だけです。`keen`を選択して、単語が入力されます。COLDCARDはアルファベットリストに戻り、Word 2が右上隅に表示されます。
5. 前のステップからのプロセスを繰り返して、単語リストの最後の単語を除いてすべて入力します。
6. 前の単語の入力に基づいて、COLDCARDが可能なオプションを計算して、リストの最後の単語を選択します。
7. COLDCARDが再起動するのを待ち、PINを入力します。

シードが設定されました。

### **パスフレーズに関する注意事項**

[パスフレーズ](https://coldcard.com/docs/passphrase)はパスワードではありません。ウォレットシードにパスフレーズを適用すると、完全に新しいウォレットが作成され、デフォルト/標準のウォレットに影響を与えません。デフォルト（パスフレーズなし）のウォレットとパスフレーズを設定したウォレットにビットコインがある場合は、[パスフレーズの入力](https://coldcard.com/docs/passphrase#enter-the-passphrase)の手順に従い、それぞれのウォレットに対して別々の検証を行ってください。

以前使用したパスフレーズは、シードが設定された後に適用できます。パスフレーズウォレットで操作しようとする前に、パスフレーズを適用することを忘れないでください。

### **移行検証**

[Address Explorer](https://coldcard.com/docs/address-explorer)と[ウォッチオンリーウォレット](https://coldcard.com/docs/glossary#watch-only-wallet)を使用して、受信アドレスの正しい導出パスが有効であることを確認できます。元のハードウェアウォレットアプリにアクセスできる場合は、使用済みの受信アドレスを表示したり、新しい受信アドレスを作成してアプリに表示される内容とAddress Explorerに表示される内容を比較できます。

現在、LedgerとTrezorの両方がデフォルトで`bc1q`アドレスを使用しています。用語の違いにより、アドレスタイプを先頭文字で参照することで混乱を減らすことができます。

参考のため、ハードウェアベンダーによるアドレス情報を含む一覧表を提示します。

| ウォレットメーカー | アドレス・タイプ(メーカー用語) | 先頭の文字 | 派生パス | 別名 (メーカー文書内) |
| --- | --- | --- | --- | --- |
| Trezor | SegWit | bc1q | m/84'/0'/0'/0/0 | BIP-84, P2WPKH, Bech32 |
|  | Taproot | bc1p | m/86'/0'/0'/0/0 | BIP-86, P2TR, Bech32m |
|  | Legacy SegWit | 3 | m/49'/0'/0'/0/0 | BIP-49, P2SH-P2WPKH, Base58 |
|  | Legacy | 1 | m/44'/0'/0'/0/0 | BIP-44, P2PKH, Base58 |
| Ledger | Native SegWit | bc1q | m/84'/0'/0'/0/0 | bech32 |
|  | Taproot | bc1p | m/86'/0'/0'/0/0 |  |
|  | SegWit | 3 | m/49'/0'/0'/0/0 | P2SH |
|  | Legacy | 1 | m/44'/0'/0'/0/0 |  |

### Address Exploler**で受信アドレスを確認する**

Address Explolerは、次の3つの一般的なアドレスタイプの受信アドレスを計算して表示します：

- `1`、またはレガシーアドレス
- `3`、またはラップSegwitアドレス
- `bc1q`、またはSegwitアドレス

その他のアドレスオプションは、上級者向けに提供されます（このチュートリアルの範囲を超えています）。

1. レコードまたは元のウォレットアプリを使用して、元のウォレットが生成した最初の受信アドレスを見つけます。
2. メインメニューから`Address Exploler`を選択します。画面の指示に従って読み進めます。
3. 表示される3つのアドレスタイプを注意深く調べ、元のウォレットが生成した最初の受信アドレスと比較します。一致するアドレスを選択します。
4. COLDCARDは最初の10個のアドレス（0〜9で番号付け）を表示します。これらのフルアドレスを使用した受信アドレスと比較します。アドレスが一致しているのを確認し、COLDCARDが元のウォレットで使用された派生パスと同じパスを使用していることを検証します。
5. COLDCARDにマイクロSDカードが挿入されていることを確認し、**1**を押してこれらのアドレスを`addresses.csv`として保存します。このファイルを使用して、ウォッチオンリーウォレットを作成してBitcoinの残高を確認します。

### **ウォッチオンリーウォレットで残高を確認する**

さらに確認する方法として、Electrum（または他のソフトウェアウォレット）でウォッチオンリーウォレットを作成し、ビットコインの金額が期待どおりであることを確認できます。

既にAddress Explorerを使用してマイクロSDカードにアドレスを保存していない場合は、ウォッチオンリーウォレットを設定するために今すぐ保存してください。

1. `addresses.csv`ファイルを含むマイクロSDカードをコンピュータのカードリーダーに挿入します。
2. [Electrum](https://electrum.org/#download)をダウンロードしてインストールします。
3. Electrumを開き、 `Create New Wallet`をクリックします。
4. テキストフィールドにウォッチオンリーウォレットの名前を入力し、 `Next`をクリックします。
5. `Import Bitcoin addresses or Public Keys`を選択します。
6. `addresses.csv`ファイルに移動し、`Open`をクリックします。
7. テキストボックス内のアドレスのリストを編集し、アドレスのみが残るようにします。引用符、インデックス番号、ヘッダ情報、派生パスは含めません。また、未使用のアドレスはカットしてください。
8. アドレスのリストが正しく編集されると、 `Next`ボタンがクリックできるようになります。リストが正しいことを再度確認し、 `Next`をクリックします。
9. ウォッチオンリーウォレットのパスワードを選択して入力します。
10. 表示されるビットコインの残高を確認してください。元のデバイスのアプリや他のソフトウェアウォレットで表示される金額と同じである必要があります。

受信アカウントとBTC残高を確認した後、移行が完了し、COLDCARDを使用できることを確信できます。

COLDCARDが初めての場合は、簡単なトランザクションを試すには、[初心者のためのビットコインの送受信](https://coldcard.com/docs/send-receive-btc)のチュートリアルを見てください！

---

### 翻訳者によるおまけ：

この記事を翻訳するにあたって、自分も所有しているTrezor Model Oneからの移行を実際に試してみました。

当初は単純に「移行と言っても、単に元のハードウェアウォレットで生成したシードフレーズを、Coldcardで打ち直す作業」という理解でいましたが、実際にやってみた所、いくつかつまづきそうなポイントがありましたので以下にまとめます。

### 使用していたBitcoinアドレスタイプの把握が何よりも大事

古いハードウェアウォレットで使用していたシードフレーズを、間違いなくColdcardに入力したはずなのに、あるはずのBitcoinが表示されない理由は、Bitcoinアドレスの違いによるものがほとんどです。

時に“化石のように進歩しない”と揶揄されるBitcoinですが、水面下では年々より安全で使いやすくなるための技術者による改善が続いており、その一つの成果としてBitcoinアドレスの変化があります。

解説記事内でも一覧表で示されていますが、現状では代表的なこの4種類を押さえておけば大丈夫です。

- **「１から始まるアドレス」**・・・通称レガシーアドレス。Bitcoin最初期から使われている。
- **「３から始まるアドレス」**・・・2012年のマルチシグ技術導入により、複数の秘密鍵による署名が可能となったアドレス。
- **「bc1qから始まるアドレス」**・・・2017年のSegwitと呼ばれる技術により、手数料の削減などが可能になったアドレス。
- **「bc1pから始まるアドレス」**・・・2021年のTaprootと呼ばれる技術により、さらなる手数料の削減、プライバシーの向上などが可能となった最新アドレス。普及率はまだ低く、対応しているウォレットやサービスもまだ少ない。

現在のTrezorやLedger、Coldcardで標準的に使われているアドレスは **”bc1q”** から始まるものになっているため、むしろ2017年以前からハードウェアウォレットでBitcoinをHODLしている古参ユーザーほど、移行時には気をつける必要があります。

実際、自分が使用していたTrezor Model Oneのデフォルトアドレスは、「３」から始まるレガシーSegwitという形式であったため、Coldcard移行後に正常に表示されない状況となりました。

また解説記事内ではElectrumを利用した確認方法が解説されていますが、これまでの[lostinbitcoinでの解説記事](https://lostinbitcoin.jp/how-to/coldcardguide03/)を参考にしてColdcardを利用している方には、Sparrow Walletを利用した方がより簡単です。

では、実際にやってみましょう。

### まずは、元のハードウェアウォレット上でアドレスタイプを確認

![ColdCardMigrationGuide_2.png](/_images/ColdCardMigrationGuide_2.png)

左欄の **「LEGACY SEGWIT ACCOUNTS」**、各アドレスの先頭が　**「３」**　であることから、　**レガシーSegwitアドレス**であることがわかります。

ここで先ほどの一覧表を確認します。

| ウォレットメーカー | アドレス・タイプ(メーカー用語) | 先頭の文字 | 派生パス | 別名 (メーカー文書内) |
| --- | --- | --- | --- | --- |
| Trezor | Legacy SegWit | 3 | m/49'/0'/0'/0/0 | BIP-49, P2SH-P2WPKH, Base58 |

メーカーによって呼び名が微妙に異なっており、非常に混乱しますが復元に必要な情報はすべてここにあります。

### Sparrow Wlletによる移行検証

この記事内の**シードワードを入力する**を参考にCOLDCARDにシードワードを入力後、デバイスをSparrow Walletに接続します。

Sparrow Walletが初めての方は、[この記事を参考](https://lostinbitcoin.jp/how-to/coldcardguide03-9/)に設定してください。

**“Import Keystore”** まで進んだ所で、アドレス形式を指定してあげます。▼をクリックすると3種類のアドレス形式が表示されます。

- Native Segwit (P2WPKH)
- Nested Segwit (P2SH-P2WPKH)
- Legacy (P2PKH)

![ColdCardMigrationGuide_3.png](/_images/ColdCardMigrationGuide_3.png)

ここでも見慣れないアドレス形式名が使われており困惑しますが、先ほどの表内の別名に注目すると自分のアドレスは**P2SH-P2WPKH**であることがわかります。

**Nested Segwit (P2SH-P2WPKH)** を選択し、処理を進めるとウォレットが復元され、過去の[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ta/#transaction)履歴やBitcoin残高も正しく表示されるようになるはずです。

Sparrow Walletを利用して、このままこのウォレットで送金のための署名を行うこともできます。

![ColdCardMigrationGuide_4.png](/_images/ColdCardMigrationGuide_4.png)

複数あるアドレス形式と、メーカーごとに違う呼び名・・・Bitcoinの一般普及などまだまだ遠い未来の話に思えますが、同じアドレス形式での移行を考えなければ、ユーザーにとっては良い点もあります。

それはこのアドレス形式には全て互換性があること。古いレガシーアドレスから、新しいSegwitアドレス、またはその逆であっても、ユーザーはその違いを意識することなくBitcoinを送金することができます。

ですから、それまで利用していたシードフレーズ、アドレス形式とトランザクション履歴をそのまま使いたいという要望が特にない場合には、新たなシードフレーズから生成した新しいアドレス宛に、Bitcoinを送金するのも一つの方法です。（※その際には、必ず少額の送金テストを行うようにしてください。）

むしろそうした方が、その後の送金手数料を抑えることにもなり、Segwitの恩恵も受けられるのでおすすめです。

さらに最近、古いツールやウォレットソフトなどを利用して作成したシードフレーズは、積極的に新しいものに変えるべき事件もありました。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">「マスタリング <a href="https://twitter.com/hashtag/Bitcoin?src=hash&amp;ref_src=twsrc%5Etfw">#Bitcoin</a> 」にも記載があるツールキットLibbitcoin Explorerに、ブルートフォース攻撃で秘密鍵を解析される脆弱性。<br><br>このライブラリを使っているウォレットソフトはあまりメジャーではないのでパニックになる必要はないけど、要警戒。<br><br>ハードウェアウォレット＋パスフレーズを推奨 <a href="https://t.co/REtWDlq8ZL">https://t.co/REtWDlq8ZL</a></p>&mdash; katakoto (@katakoto) <a href="https://twitter.com/katakoto/status/1689344621695086593?ref_src=twsrc%5Etfw">August 9, 2023</a></blockquote>

簡単に言うと、過去のツールにビットコインのシードフレーズを生成する処理に問題があって、攻撃者による推測が可能な状態であったということです。

シードフレーズの生成には本来、十分なランダム性が求められます。最近のソフトウェアウォレット・ハードウェアウォレットでは必ず256bitか128bitの鍵空間を利用しているはずですが、今回のように、何らかの理由で32bitの範囲内でシードフレーズが作られてしまうと、そうしたウォレットは全てハッカーに把握されているといっても過言ではありません。（そうしたウォレットへの攻撃の容易さは以下のツイートを参照してください。）

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">俺この&quot;よわよわ乱数発生器から作られた秘密鍵が、公開アドレス(公開鍵)から一瞬で割られる動画&quot;を見て衝撃を受けてたんだけど<br><br>なるほどそうした秘密鍵は、既に辞書化されてるから一瞬なんだな。(実際に総当たりしてない)という学びをAndreasさんの久々のYoutube動画から得た<a href="https://t.co/UDnYqrxYLG">https://t.co/UDnYqrxYLG</a> <a href="https://t.co/QQhsSbMceL">https://t.co/QQhsSbMceL</a></p>&mdash; katakoto (@katakoto) <a href="https://twitter.com/katakoto/status/1690231603291897856?ref_src=twsrc%5Etfw">August 12, 2023</a></blockquote>

自分がいつどのようなウォレットやツールを利用してシードフレーズを生成したのかを記憶していない人は、むしろこうした機会に積極的に、COLDCARDなど安全性が保障されたものに移行するべきでしょう。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">Ledger:内蔵のセキュアエレメントと呼ばれるチップでエントロピーを生成<br><br>Trezor:マイクロコントローラとパソコンの乱数生成器をミックス<br><br>ColdCard:物理的なノイズを測定して乱数を作る内蔵の真性乱数生成器(TRNG)を3個利用。デバイスのキーパッドやサイコロを使って自身でエントロピーを追加可能 <a href="https://t.co/S4JH4TMSuS">https://t.co/S4JH4TMSuS</a></p>&mdash; katakoto (@katakoto) <a href="https://twitter.com/katakoto/status/1649119295627231232?ref_src=twsrc%5Etfw">April 20, 2023</a></blockquote>

この移行作業の件でもそうでしたが、最近では古参であればあるほど逆にハマりやすい罠やリスクが増えています。参入時期に関わらずおごらず情報をアップデートし続け、今後も自身の資産をしっかり守って、楽しいBitcoinライフをお送りください。


![ColdCardMigrationGuide_5.jpg](/_images/ColdCardMigrationGuide_5.jpg)
<figcaption>"おごらず謙虚に、[Satoshi](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-sa/#satoshi) を積み重ねよ。" -MAT ODELL-</figcaption>



***
コンテンツの著作権は[Coinkite.com](https://coinkite.com/)に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to [Coinkite.com](https://coinkite.com/)

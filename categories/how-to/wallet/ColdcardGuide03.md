---
title: ハードウェアウォレットCOLDCARDで大事なビットコインを守ろう⓷～セットアップ編～
taxonomy:
    category:
        - how-to
        - wallet
    post_tag:
        - beginner
---

## COLDCARDをセットアップして基本的な使い方を覚えよう！

|  ![Category](/_images/category.png)  |  ハウツー、ビットコインを安全に管理するには |  ![Tag](/_images/tag.png)  |  初級  | ![Time](/_images/timer.png)  |  25分  |
| ---- | ---- | ---- | ---- | ---- | ---- |

*本記事は[@katakoto](https://twitter.com/katakoto) が制作、2022年9月に公開したものです。*

![ColdCardGuide03_1.JPG](/_images/ColdCardGuide03_1.jpg)

さあ前回の[購入編](https://lostinbitcoin.jp/how-to/coldcardguide02/)を経て、皆さまの手元に無事COLDCARDが届きましたでしょうか。

今回は実際にCOLDCARDをセットアップして、ビットコインの受け取り、送金までを解説したいと思います。

COLDCARDの一番の売りとして、日常的な操作において本体をパソコンやインターネットに直接接続することなく利用できる**”エアギャップ”運用**がありますが、今回の記事では、一番手軽なUSB-Cケーブルを用いた方法で説明します。Mk4では下記の4通りの方法での外界との接続が可能ですので、興味のある方はぜひ挑戦してみてください。

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Optionality.<br>As cold or as connected as you want.<br>Every connectivity option is disabled by default. <a href="[https://t.co/9vI2UPd4VQ](https://t.co/9vI2UPd4VQ)">[pic.twitter.com/9vI2UPd4VQ](http://pic.twitter.com/9vI2UPd4VQ)</a></p>— COLDCARD (@COLDCARDwallet) <a href="[https://twitter.com/COLDCARDwallet/status/1521225690691080192?ref_src=twsrc^tfw](https://twitter.com/COLDCARDwallet/status/1521225690691080192?ref_src=twsrc%5Etfw)">May 2, 2022</a></blockquote>

さて皆さんは今、待ちに待ったCOLDCARDを手にして、さっそく袋から取り出し実際に触ってみたくてうずうずしているかもしれません。でも、ここでひとまず深呼吸。

**”Don’t trust, Verify!”**（信用するな、検証しろ！）は、開封の段階からすでに始まっているのです。

### 不正開封防止袋チェック

![ColdCardGuide03_2.jpg](/_images/ColdCardGuide03_2.jpg)

COLDCARDは味気ないほどの簡易包装であなたの元に届いたかと思いますが、その袋には流通経路での攻撃者からの悪意ある攻撃を防ぐ、たくさんの工夫が施されています。

まずは袋に不審なダメージや一度開けられた形跡がないかをチェックしましょう。

袋の上部シールは、一度でも引き剥がすと**「VOID」**（無効）という文字が表示されるようになっています。

![ColdCardGuide03_3.jpg](/_images/ColdCardGuide03_3.jpg)

少しでも不審な点が見つかった場合は、写真を添えて[support@coinkite.com](mailto:support@coinkite.com) 宛にメールで連絡しましょう。

袋の中身は下記のようになっています。（2022年8月4日現在）

![ColdCardGuide03_4.jpg](/_images/ColdCardGuide03_4.jpg)

- COLDCARD本体＋プラスチック・カバー
- ウォレットバックアップカード
- ステッカー×２

この他に、出荷直前に袋から切り離して同梱されたプラスチック袋の切れ端が入っているはずです。ここに印刷されているシリアルナンバーが、袋表面に表示してあるシリアルナンバーと同じであることを確認してください。（この番号は、あとでまた本体の確認でも使います。）よりパラノイドな人は、袋と切れ端のミシン目が一致するのを確かめると良いそうです。

### 電源オン

いよいよ待ちに待った電源オンです。

USB-タイプCケーブルをCOLDCARD上部に接続し、USB側をパソコンやUSB充電器などに接続し電源を供給します。

最初の画面では、下図のような販売規約が表示されているはずです。

![ColdCardGuide03_5.png](/_images/ColdCardGuide03_5.png)

画面のスクロール/移動には、**数字キー**を利用します。上下左右への移動はそれぞれ**５，８，７，９**が対応。**☓**は**キャンセルボタン**、**✓**は**OK(実行)ボタン**として使います。

![ColdCardGuide03_6.png](/_images/ColdCardGuide03_6.png)

たいていメッセージの最後に、その後に進むためのボタンの指示が表示されているので、メッセージは**９キー**を何回か押して最後まで表示させましょう。

販売規約への同意は**✓ボタン**を押して先へ進めます。

最初のメニュー画面が表示されます。ここで最初に行うべきはシリアルナンバーの確認です。

**“Bag Number”**を選んで**✓ボタン**を押してください。

![ColdCardGuide03_7.jpg](/_images/ColdCardGuide03_7.jpg)

画面に表示されたシリアルナンバーが、同梱されたプラスチック袋の切れ端もしくは袋表面に表示してあるシリアルナンバーと同じであることを確認してください。
![ColdCardGuide03_8.jpg](/_images/ColdCardGuide03_8.jpg)

![ColdCardGuide03_9.jpg](/_images/ColdCardGuide03_9.jpg)

このシリアルナンバーはCOLDCARDのセキュアエレメント内に保存されており、ほぼ改変が不可能な値です。

お疲れさまでした。これによってCoinkiteの工場から一切の改変なくあなたの元に商品が届けられたことがVerifyされました。

### ファームウェア・アップグレード

次は、ファームウェアのアップグレードを行います。COLDCARDに限らずハードウェアウォレットの購入直後には、必ず行うことを推奨します。万が一、入手経路段階でファームウェアにマルウェアなどを仕込まれていた場合でも、公式から最新版のファームウェアを取得しアップグレードすることで、クラッカーによる攻撃を無効化することができます。

また、製品出荷後に発見された脆弱性などにもバグフィックスがなされている場合も多いので、面倒くさがらずに行いましょう。

実際、最近COLDCARD MK4から追加された新機能バーチャルディスク機能にバグが見つかり、最新版のアップデートでバグフィックスが行われています。

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Mk4 Firmware v5.0.6 Security Release<br><br>Virtual Disk feature has been updated w/ a bugfix to address potential security concerns, also new security hardening changes have been implemented. <br><br>Upgrade strongly recommended (Mk3 unaffected)<br><br>Learn more <a href="[https://t.co/rDHIeqgILZ](https://t.co/rDHIeqgILZ)">[https://t.co/rDHIeqgILZ](https://t.co/rDHIeqgILZ)</a></p>— COLDCARD (@COLDCARDwallet) <a href="[https://twitter.com/COLDCARDwallet/status/1553085800774090754?ref_src=twsrc^tfw](https://twitter.com/COLDCARDwallet/status/1553085800774090754?ref_src=twsrc%5Etfw)">July 29, 2022</a></blockquote>

> MK4ファームウェアv5.0.6セキュリティリリース
バーチャルディスク機能がバグ修正とともに更新され、潜在的なセキュリティの懸念に対処しました。また、新しいセキュリティ強化のための変更が実装されました。アップグレードを強く推奨します（Mk3は影響を受けません）
>

※ファームウェアアップグレードにはMicroSDカードが必要です。事前に準備しましょう。上記のバーチャルデスク機能を有効化すれば、MicroSDカード不要でアップグレードすることもできます。

#### アップグレード手順

1. **Advanced/Tools > Upgrade Firmware > Show Version** から現在のバージョンを確認する。
2. 公式サイト [coldcard.com/docs/upgrade](https://coldcard.com/docs/upgrade) にてMK4用最新バージョンを確認する。

    ![ColdCardGuide03_10.png](/_images/ColdCardGuide03_10.png)

3. リンクをクリックして、ファイルをダウンロード後、MicroSDカードに保存する。

※ここでももう誰のことも信じられないビットコイナー用に、ダウンロードしたファイルが本物であることを検証する”Don’t trust, verify”ステップが別途発生しますが、この説明では割愛します。詳細は[こちら](https://coldcard.com/docs/upgrade#dont-trust-verify-the-firmware)。

4. MicroSDカードをCOLDCARDに挿入し、`**Advanced/Tools > Upgrade Firmware > From MicroSD**`を選択。
5. **✓ボタン**を押すと、MicroSDカード内に保存したファイルが表示される。
6. ファイル名（この例では**2022-07-29T1816-v5.0.6-mk4-coldcard.dfu**)を選択し**✓ボタン**を押す。
7. 確認画面が表示されるので**✓ボタン**を押す。
8. アップグレード(Upgrading...)が開始するので、しばらく待つ。
9. アップグレード完了後、COLDCARDが再起動するので、再度、**Advanced/Tools > Upgrade Firmware > Show Version** から最新バージョンにアップデートしていることを確認する。

アップグレード手順を動画でまとめました。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">COLDCARD Firmware Upgrade動画（NGテイク）<br><br>NG理由：途中で赤子が泣き出したため。 <a href="https://t.co/WEQGZFQb0t">pic.twitter.com/WEQGZFQb0t</a></p>&mdash; katakoto (@katakoto) <a href="https://twitter.com/katakoto/status/1561138231302754304?ref_src=twsrc%5Etfw">August 20, 2022</a></blockquote>

### PINセットアップ

さあ、ここからがCOLDCARDセットアップの本番です。PINの設定に取り掛かります。PINは一度設定してしまうと、あなた以外の誰も知ることはできません。COLDCARDにはいわゆる”工場出荷状態にリセット”するための設定はないため、PINを忘却・紛失してしまった時点で、デバイスが使用不能になってしまいます。それゆえこの設定には少しばかりの緊張感が必要です。

### PINとは

- COLDCARDデバイスにアクセスするのに必要な暗証番号。
- PINは前半部分と後半部分の２つのパートからなる。
- それぞれのパートに２桁～６桁の数字で設定するが、ベストプラクティスは４桁＋４桁。

例：

```
12-34
1234-5678
872323-39843
12-345678
```

このPINの設定には、少しクセがあるので丁寧に解説します。

**“Choose PIN Code”**（PINコード選択）を選びます。
![ColdCardGuide03_11.png](/_images/ColdCardGuide03_11.png)

PINに関する解説文が表示されます。**✓ボタン**を押して進めます。

警告文が表示されます。**６キー** を押して進めます。
![ColdCardGuide03_12.png](/_images/ColdCardGuide03_12.png)

> **警告：**PINを忘れてしまった場合、COLDCARDには“PINを復元”や”工場出荷状態に復元”する機能は一切ありません。PINは絶対に忘れないようにしてください。このメッセージを最後まで読んだなら、６キーを押してください。
>

**PINの最初のパート**（推奨４桁）を入力し、**✓ボタン**を押します。

![ColdCardGuide03_13.png](/_images/ColdCardGuide03_13.png)

その後、**２つの英単語**が表示されます。この２つの単語は、**”アンチ・フィッシングワード”**と呼ばれ、あなたのCOLDCARDと入力したPINの組み合わせによって生成されるユニークなものです。他のデバイスで同じPINを入力しても絶対に同じにはなりません。

![ColdCardGuide03_14.png](/_images/ColdCardGuide03_14.png)

今後、COLDCARDを使う度にPINの最初のパートを入力した時点で、あなたは毎回この２つの英単語を目にすることになります。それが、あなたのCOLDCARDが知らない間に誰かにすり替えられたり、おかしな細工をされていない何よりの証となります。（つまり、この２つの単語と違った英単語が表示された場合は、何かがおかしいと判断できるわけです。）

最初のPINと、この２つの英単語をウォレットバックアップカードに記入してください。

PINとアンチ・フィッシングワードに問題がなければ、**✓ボタン**を押して進めます。

“Enter rest of PIN”（残りのPINを入力）画面で、**後半パートのPIN**（推奨４桁）を入力します。

![ColdCardGuide03_15.png](/_images/ColdCardGuide03_15.png)

問題なければ、**✓ボタン**を押します。

再度、PINの前半部分の入力を求められます。その後、アンチ・フィッシングワードが表示され、PINの後半部分を入力します。

![ColdCardGuide03_16.png](/_images/ColdCardGuide03_16.png)

正しく入力されれば、PINの設定は完了となります。

後半パートのPINもウォレットバックアップカードへの記入をお忘れなく。このステップを動画でまとめました。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">COLDCARD PINセットアップ<br><br>✅ PINは前半・後半の2パート設定する<br>✅ 推奨は4桁×4桁の数字<br>✅ 途中表示される2つの英単語はすり替え検知用<br>🚨 見慣れない英単語が表示されたら注意<br><br>Brute force攻撃に怯える方。1億通りのパターン試してどうぞ。13回連続で間違えるとCOLDCARDは文字通りぶっ壊れます💥 <a href="https://t.co/nRUpmoVizr">pic.twitter.com/nRUpmoVizr</a></p>&mdash; katakoto (@katakoto) <a href="https://twitter.com/katakoto/status/1561628453803151361?ref_src=twsrc%5Etfw">August 22, 2022</a></blockquote>


一度ここでCOLDCARDの電源を入れ直して、この
**”前半のPIN入力”→”アンチ・フィッシングワードを確認”→”後半のPIN入力”**
の流れを確認してみてください。

### ウォレット作成

PINの設定が終わり、ついに待ちに待ったBitcoinウォレットの作成に取りかかります。

この時点でCOLDCARDはまだ空っぽで、ウォレットとしては機能していません。

つまりPINとアンチ・フィッシングワードは、この後にウォレットを作成するために登場する**24個の英単語（シードフレーズ）**とは、一切何の関係もない独立した情報であるのを頭に入れておいてください。

では、始めましょう。

**“New Seed Words**（新しいシード単語）を選択し、**✓ボタン**を押します。

![ColdCardGuide03_17.png](/_images/ColdCardGuide03_17.png)

**“24 Word”**を選択し、**✓ボタン**を押すと**24個の英単語（シードフレーズ）**が表示されます。ウォレットバックアップカードに、順番通りに正しく記入しましょう。

![ColdCardGuide03_18.png](/_images/ColdCardGuide03_18.png)

ここでも**５・８キー**で上下にスクロールできます。

![ColdCardGuide03_19.png](/_images/ColdCardGuide03_19.png)

1～24までの英単語を正しく記録出来たら、**✓ボタン**を押します。

次に正しく記録できたかどうかの確認画面になります。質問されている番号の英単語を、表示されている3択から選んで、数字キーで回答してください。

![ColdCardGuide03_20.png](/_images/ColdCardGuide03_20.png)

全問正しく回答できた時点で、新しいウォレットが生成されます。

初回設定時には、新機能NFC（COLDCARDを携帯などにかざすだけで通信できる技術）を有効化するかどうかが聞かれます。**✓ボタン**を押せば**有効化**(enable)されます。

![ColdCardGuide03_21.png](/_images/ColdCardGuide03_21.png)

次に、USBポートを有効化して使用するかどうかが聞かれます。今回の解説では、次のSparrow WalletからCOLDCARDを読み込む必要がありますので、**有効化**(enable)しておきます。**無効化**(disable)しても、パソコンから電源をもらって起動することはできますので、エアギャップ運用にこだわる方は無効にしておくと良いと思います。**Xボタン**で**有効化**、**✓ボタン**を押せば、**無効化**されます。

![ColdCardGuide03_22.png](/_images/ColdCardGuide03_22.png)

両方の設定共に、後から**Settings > Hardware On/Off**にて変更が可能です。

**“Ready to Sign”**（署名の準備）が表示されれば、ウォレットは準備完了です。

![ColdCardGuide03_23.png](/_images/ColdCardGuide03_23.png)

### SparrowWalletセットアップ

お気づきでしょうか。この時点まであなたのCOLDCARDはまだ一度もインターネットに触れていないことに。Bitcoinのウォレットを使い始めるのには、Bitcoinネットワークどころかインターネットにすら接続する必要がないのです。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">「ユーザーのウォレット内のデジタルキーは、ビットコインのプロトコルから完全に独立しており、ソフトウェアによりブロックチェーンやネットへのアクセスなしに生成、管理が可能である。」<a href="[https://t.co/HxCJ6G5YzI](https://t.co/HxCJ6G5YzI)">[https://t.co/HxCJ6G5YzI](https://t.co/HxCJ6G5YzI)</a> <a href="[https://t.co/Djr0V4WCzl](https://t.co/Djr0V4WCzl)">[pic.twitter.com/Djr0V4WCzl](http://pic.twitter.com/Djr0V4WCzl)</a></p>— aantonop_quotes (@AantonopQuotes) <a href="[https://twitter.com/AantonopQuotes/status/1335446800363220994?ref_src=twsrc^tfw](https://twitter.com/AantonopQuotes/status/1335446800363220994?ref_src=twsrc%5Etfw)">December 6, 2020</a></blockquote>

実際、Bitcoinを受け取るだけであれば、COLDCARDに表示したQRコードを相手にスキャンしてもらうだけで済みます。それでもやはり実際にBitcoinを送金したり、ウォレット内の残高確認にはネットワークに接続する必要があり、そのためのインターフェースとしてBitcoinエコシステムにはCOLDCARDに対応した様々なソフトウェアが存在しています。

- [Electrum Wallet](https://electrum.org/) (上級者向け)
- [Wasabi Wallet](https://wasabiwallet.io/)（初・中級者向け）
- [Sparrow Wallet](https://sparrowwallet.com/)（初・中級者向け）
.

今回は、プライバシーにフォーカスした多機能ウォレットでありながら、わかりやすいUI/UXで初心者でも使いやすい**Sparrow Wallet**を利用して解説します。

#### インストール

公式サイト [sparrowwallet.com](https://sparrowwallet.com/download/) から自分のOSにあったバージョンをダウンロードし、インストールしてください。

![ColdCardGuide03_24.png](/_images/ColdCardGuide03_24.png)

最初の画面では、Sparrowはオンライン・オフラインモードを切り替えて使用できる旨の説明がなされています。ここでもインターネットと切り離して使用するエアギャップ運用への配慮がされています。

**“Next”**をクリックして先へ進めましょう。

![ColdCardGuide03_25.png](/_images/ColdCardGuide03_25.png)

ここから先の数画面では、Bitcoinネットワークへどのようにして接続するかの説明がなされています。これも自身のレベルやプライバシー要求に合わせて選びましょう。選択できるのは下記、3つのオプションからです。下に行くほど自分の情報を外部に漏らさない、プライバシー優先の選択になります。

- パブリック・サーバー・・・企業・団体が公開しているサーバー
- ビットコイン・コアノード・・・自分が運用してるBitcoin Coreノード
- プライベートElectrumサーバー・・・自分が運用しているElectrumサーバー

**“Next”**を押して説明画面を先に進めていきましょう。

![ColdCardGuide03_26.png](/_images/ColdCardGuide03_26.png)

下記の画面で **“Configure Server”**（サーバー設定）をクリックして、接続するサーバーを選択します。今回の記事では初心者向けに **”パブリック・サーバー”** を選択しますが、自分で[Umbrel](https://umbrel.com/)などを利用しBitcoinノードを運用している方は、ぜひご自身のサーバーへの接続にも挑戦してみてください。

![ColdCardGuide03_27.png](/_images/ColdCardGuide03_27.png)

好みの公開サーバーを選択してから、**”Create New Wallet”**（新規ウォレットを作成）をクリックします。

![ColdCardGuide03_28.png](/_images/ColdCardGuide03_28.png)

自分にとって分かりやすいウォレットの名前を付けましょう。その後、**”Create Wallet”**（ウォレットを作成）をクリックします。

![ColdCardGuide03_29.png](/_images/ColdCardGuide03_29.png)

この段階でCOLDCARDをパソコンに接続し、PINを入力してアンロックしておきます。

Sparrow Wallet上の画面で**”Connected Hardware Wallet”**（接続済みハードウェアウォレット）をクリック後、ポップアップ画面の**”Scan”**を押して、スキャンを開始してください。

![ColdCardGuide03_30.png](/_images/ColdCardGuide03_30.png)

![ColdCardGuide03_31.png](/_images/ColdCardGuide03_31.png)

接続済みのCOLDCARDが表示されますので、**”Import Keystore”**（キーストアの読み込み）をクリックして情報を読み込みます。

![ColdCardGuide03_32.png](/_images/ColdCardGuide03_32.png)

COLDCARDの検知に失敗する場合は、次の点を確認してください。

![ColdCardGuide03_33.png](/_images/ColdCardGuide03_33.png)

- COLDCARDのUSB機能がオン。( Settings > Hardware On/Off > USB Port > Default On)
- COLDCARDがパソコンに正しくUSB接続されている
- COLDCARDへのPIN入力が完了している

COLDCARDがスキャンされ、情報の読み込みが正しく完了するとKeystores欄に下記のような情報が表示されます。

**“Apply”**（適用する）をクリックして、COLDCARDから情報を取り込みましょう。

※この際に取り込まれるのは**XPUB**と呼ばれる情報のみです。秘密鍵は一切、外部に伝わることはないので安心してください。

![ColdCardGuide03_34.png](/_images/ColdCardGuide03_34.png)

Sparrow Wallet利用時のパスワード設定画面になります。パスワードが不要であれば、空欄のまま**”No Password”**で先に進みます。

![ColdCardGuide03_35.png](/_images/ColdCardGuide03_35.png)

Sparrow Walletのデフォルトでは、米ドルでビットコインの目安金額が表示されます。日本円に変えるには **File > Preferences** からFiatのCurrencyをJPYに設定してください。

![ColdCardGuide03_36.png](/_images/ColdCardGuide03_36.png)

### ビットコインを受け取る

今後ビットコインを受け取るには、もうこの段階からCOLDCARDをSparrow Walletに接続する必要はありません。これから一生かかっても使いきれないであろう無限のビットコインアドレスが既にあなたのものです。”無限”は言い過ぎました。86億個のビットコインアドレスが今やあなたのものになりました。

あらゆる取引が全て公開台帳に記録されるビットコイン・ネットワークにおいて、アドレスの使いまわしはプライバシーの観点から推奨されません。毎回、思う存分新しいアドレスを使って取引を行いましょう。

左のメニューから**”Receive”**（受け取り）を選択すれば、都度Sparrow Walletが自動で新しいアドレスを表示してくれます。

![ColdCardGuide03_37.png](/_images/ColdCardGuide03_37.png)

さっそく少額のBitcoinを取引所から、このアドレスに送金してみました。

着金するとポップアップウィンドウで通知が受け取れます。

![ColdCardGuide03_38.png](/_images/ColdCardGuide03_38.png)

### ビットコインを送金する

受け取る時と違って、ビットコインを他のアドレス宛に送金する際には、毎回COLDCARDの接続が必要になります。なぜならビットコインの送金には、必ずそのトランザクションにGOサインを出すための”署名”が必要であり、その”署名”には秘密鍵が必要になるからです。

そしてCOLDCARDにおいて秘密鍵は、本体の機密情報保護チップ内に保存されており、ユーザーが意図的に漏らさない限り、外の世界に知られることはありません。

つまり送金時には毎回、下記のステップが必要となります。

**Sparrow Wallet側で、送金のためのトランザクションを作成し、COLDCARDの秘密鍵で署名。**

これがハードウェアウォレットが、別名**”署名デバイス”**とも呼ばれる所以です。

![ColdCardGuide03_39.png](/_images/ColdCardGuide03_39.png)

では、設定していきます。

左のメニューから**”Send”**を選択します。

- “Pay to”に送金先アドレス
- ”Label”に記録用のラベル名
- ”Amount”に送金金額

をそれぞれ入力します。Bitcoinの単位はBTCかSats（1 sats=0.00000001 BTC）から選択できます。

ちょうどこの記事の執筆中に、ビットコインのプロジェクト開発者として有名な[**Joe Miyamoto**](https://twitter.com/joemphilips)氏が、昭和のかほり感じさせる替え歌でドネーションを欲してらっしゃいましたので、さっそくこのアドレス宛にビットコインを送り付けてみましょう。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">39wxJGuf7b1RRsc5ZnNXim2q67FFRHzoPN<br><br>この<br>アドレスに<br>鬼のように<br>デカいTXO<br>つけてく〜ださ〜い〜</p>— Joe Miyamoto (@joemphilips) <a href="[https://twitter.com/joemphilips/status/1559553743418720258?ref_src=twsrc^tfw](https://twitter.com/joemphilips/status/1559553743418720258?ref_src=twsrc%5Etfw)">August 16, 2022</a></blockquote>

Web3、NFT、DAO、そんな空虚なバズワードを掲げていれば、見ず知らずの野蛮人たちがお金を投げつけてくる世界とは違って、ビットコイン関連の開発は地味で地道なものなのです。トークンやNFTを一緒に売ってくれるセレブもラッパーもいないから、その流れはゆっくりで派手さはないけれど、人知れず世界に真に意味があるものを作ろうと日々尽力する彼らへのリスペクトをビットコインに替えて、あなたも是非に贈りましょう。

![ColdCardGuide03_40.png](/_images/ColdCardGuide03_40.png)

送金にかかる費用を設定する**Fee**（手数料）項目では、Rangeをスライドさせて手動で費用を設定できます。最近のビットコインネットワークはあまり混雑することなく空いているので、時間に余裕がある方は、ぜひ最小設定の1stas送金を試してみてください。この例では送金手数料約4.58円にて、1時間以内には着金しています。

**“Create Transaction”**（トランザクションの作成）をクリックして次に進みます。

**“Finalize Transaction for Signing”** （署名のためのトランザクションを確定）をクリックして、COLDCARDによる実際の署名に進みます。

![ColdCardGuide03_41.png](/_images/ColdCardGuide03_41.png)

この段階でCOLDCARDをパソコンに接続し、アンロックを終えておいてください。

**“Sign”**をクリックして次に進みます。

![ColdCardGuide03_42.png](/_images/ColdCardGuide03_42.png)

**“Sign”**をクリックすると、COLDCARD上の画面にトランザクションの詳細が表示されます。

![ColdCardGuide03_43.png](/_images/ColdCardGuide03_43.png)

画面上の送金額と送金アドレスに間違いがないことを確認したら、**✓ボタン**を押してください。

![ColdCardGuide03_44.jpg](/_images/ColdCardGuide03_44.jpg)

署名したトランザクションを、いよいよビットコインネットワークにブロードキャストします。このアクションによって初めて送金トランザクションが開始されます。

**“Broadcast Transaction”**（トランザクションをブロードキャスト）をクリックします。

![ColdCardGuide03_45.png](/_images/ColdCardGuide03_45.png)

おめでとうございます。あなたの送金トランザクションが無事、ビットコインネットワークに送信されました。

**Txid**（トランザクションID）をブロック・エクスプローラーにコピペして検索すれば、現在の送金ステータスを確認することが可能です。

![ColdCardGuide03_46.png](/_images/ColdCardGuide03_46.png)

![ColdCardGuide03_50.png](/_images/ColdCardGuide03_50.png)

[https://mempool.space/tx/6da1ed030467bcbe6d82cb63fa6bae5feeea02ce7d68f9bb67ffc1a7f071de67](https://mempool.space/tx/6da1ed030467bcbe6d82cb63fa6bae5feeea02ce7d68f9bb67ffc1a7f071de67)

大変お疲れ様でした。これでCOLDCARDを使ったBitcoin運用方法の説明は一通り終了となります。COLDCARDで安全・安心なビットコインライフをお送りください！

…あれ、何だろう。何かがまだ心に引っかかる…何かとても大切なことが触れられていないような…

![ColdCardGuide03_48.jpg](/_images/ColdCardGuide03_48.jpg)

このバックアップカードってのが盗まれたら何もかもが終わりなんじゃ？字ぃ汚いから大丈夫かな？


万が一COLDCARDが盗まれた or 壊れた場合、私のビットコインはどうなるの？


次回は、この辺りの不安を徹底的に解消すべく「COLDCARDバックアップ・リカバリ編」をお届けします。あなたのビットコインのセキュリティをもうワンレイヤーアップさせる"パスフレーズ"に関してもお話します。

![ColdCardGuide03_49.jpg](/_images/ColdCardGuide03_49.jpg)

***
[利用規約 A](https://lostinbitcoin.jp/copyright/#uaa)

---
title: 用語集
taxonomy:
    category:
        - glossary
---

### 日本一充実したビットコイン用語集を作りたい！

[River Financial の Bitcoin Glossary](https://river.com/learn/terms/) をベースに、日本語のビットコイン用語集を構築中です。用語集作りに参加して、**ビットコイン**を稼ぎませんか？

以下の英語の用語説明を日本語にしてください。忠実な翻訳でなくて構いません。AI翻訳にかけて内容を理解した上で、ご自身の言葉で説明してください。

日本語の提案はGitHubでプルリクエストとして受付中。プルリクエストがマージされたら、報酬をライトニング⚡️送金します。<br>
提案手順は[こちら](https://github.com/lostinbitcoin/categories/wiki)の「2. 用語集の用語説明の提案手順」をご参照ください。

--
### ビットコイン用語集
#### 索引　[あ](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-a/#a)　[か](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ka/#ka)　[さ](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-sa/#sa)　[た](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ta/#ta)　[な](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-na/#na)　[は](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ha/#ha)　[ま](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ma/#ma)　[や](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ya/#ya)　[ら](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ra/#ra)　</a>[わ](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-wa/#wa)　[英数字](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-number/#number)
--

### <a id="a"></a>あ

|  用語<br>英語表記<br>報酬  |  説明  |
| ---- | ---- |
|アドレス<br>Address<br>2,100 sats | <a id="address"></a>アドレスはビットコインを受け取るために使用され、英数字から成る文字列として表されます。公開鍵とアドレスはしばしば混同されますが、アドレスは公開鍵のハッシュであり、ビットコインを受け取るには公開鍵ではなくアドレスが使用されます。厳密に言うと、アドレスは単なる公開鍵のハッシュというわけではありませんが、技術的な話なので割愛します。</br>ビットコインウォレットを使用すると、ユーザーは必要な数だけアドレスを生成できるだけでなく、指定したアドレスにビットコインを送信できます。アドレスに送られたビットコインは、そのアドレスを導出した秘密鍵の所有者のみが使用できます。</br>_注意：プライバシーを保護するために、アドレスの再利用は避けてください。ビットコインを受け取るたびに、ウォレットで新しいアドレスを生成することをおすすめします。_</br>ビットコインアドレスはいくつかの異なるスクリプトを表すことができます。アドレスはスクリプトタイプを伝えるためにエンコードされ、プレフィックスが付けられます。レガシーアドレスはBase58を使用します。レガシーアドレスが公開鍵のハッシュ、いわゆるP2PKHアドレスの場合は「1」で始まります。あまり多くはありませんが、スクリプトのハッシュである場合は「3」で始まります。SegWitアドレスはすべてBech32でエンコードされ、プレフィックス「bc1」で始まります。ビットコインの送付先としてアドレスが入力されると、ウォレットはアドレスの種類を調べて適切なスクリプトを作成します。このスクリプトはscriptPubKeyと呼ばれ、送金額に追加されます。これら2つのデータ（金額とscriptPubKey）がアウトプットになります。|
|イニシャル・ブロック・ダウンロード (IBD)<br>Initial Block Download (IBD)<br>2,100 sats | <a id="ibd"></a>イニシャル・ブロック・ダウンロード（IBD）は、完全なビットコインブロックチェーンをゼロから構築するプロセスです。新しいノードをセットアップしてビットコインネットワークに参加すると、他のノードに接続してブロックをリクエストします。新しいノードは過去に生成された全てのブロックをダウンロードおよび検証してブロックチェーンを構築し、ネットワークと同期します。</br>ブロックは個別ノードから得ますが、異なるノードからのデータとクロスチェックできること、さらにはプルーフオブワーク・ブロックチェーンの性質から、IBDはトラストレスなプロセスです。IBDの速さはインターネットの帯域幅とコンピューターの仕様で異なり、場合によっては数日、数週間かかります。</br>IBDを開始すると、ノードはまず他のノードからすべてのブロックヘッダーを収集し、次に各フルブロックをリクエストします。これはIBDの効率を高め、ユーザーがより早くノードを使用できるようにするためです。ビットコインノードはブロックを1個1個ダウンロードおよび検証することでブロックチェーンを構築すると同時に、UTXOセット（すべての有効なビットコインの包括的なリスト）も構築します。UTXOセットはブロック内のトランザクションがUTXOを破棄および作成するたびに更新されます。|
|インフレーション<br>Inflation<br>2,100 sats | <a id="inflation"></a>インフレーション（インフレ）は、ある経済圏の物価全般が時間の経過とともに上昇する現象で、その国の通貨の購買力を低下させます。インフレは近代経済学の当然の帰結で、主に政府や中央銀行による恒常的な通貨供給量の拡大が引き金になります。<br>インフレはモノやサービスの価格で測られますが、通常は消費者物価指数（CPI）として知られる多種多様な商品の加重平均市場価格の変動で表されます。<br>インフレが極端に高い水準に達すると、ハイパーインフレーション（ハイパーインフレ）と呼ばれます。ハイパーインフレは通貨の価値を急減させ、経済を不安定にします。ハイパーインフレを制御できないと、最終的に経済は崩壊します。<br>CPIで示されるインフレは、資産価格のインフレと一致する傾向にありますが、常にそうとは限りません。現に新型コロナウィルスのパンデミックの際は、資産価格のインフレが消費財のインフレを大きく上回りました。これはモノやサービスの需要減少が、消費財へのデフレ圧力となったためです。<br>一般的に、適度なインフレは経済にとって好ましいとされています。物価が将来上昇すると思えば、人々は消費を前倒しするので、景気は刺激されます。しかし、インフレは時間とともに通貨が減価し続けることを意味するので、通貨の価値貯蔵手段としての機能を損ないます。|
|インフレーションヘッジ<br>Inflation Hedge<br>2,100 sats | <a id="inflation_hedge"></a>インフレが起きると通貨の購買力が低下します。インフレヘッジは、インフレによる財産の価値低下を防ぐことを目的としています。インフレヘッジとみなされる資産は、インフレが加速しても、その価値の維持または増加が期待できます。<br>ビットコインは希少性が高く、ドルや円など法定通貨のインフレが進むにつれて価値が高まるため、強力なインフレヘッジと考えられています。急速な通貨膨張、すなわち通貨供給拡大による物価上昇が進む中、ビットコインの本質的な希少性と、政府や中央銀行の影響力さえおよばない性質に注目する投資家や企業が増えています。<br>法定通貨の価値がインフレの影響で下がると、ビットコインの法定通貨建て価格は上昇する傾向があります。現金、預貯金、債券などで保有する財産が減価する中、ビットコインで保有する財産は増価します。つまり、ビットコインを持つことで、インフレによる法定通貨の減価リスクをヘッジできます。|
|ウォッチタワー<br>Watchtower<br>2,100 sats | <a id="watchtower"></a>信頼関係にない2者が運用するライトニングノード間に構築されたペイメントチャネルから成るライトニングネットワークには、二重支払いの問題があります。ウォッチタワーは二重支払い防止を目的に、特定チャネルを監視するサービスです。ウォッチタワーを請け負う第3者への信用が求められますが、ライトニングノード運用者はウォッチタワーを利用することで、チャネルパートナーによる二重支払いを防ぐことができます。<br>ライトニングネットワークは資金移動に未承認トランザクションを使うため、二重支払い問題を完全に解消することはできません。チャネルを開いた相手が悪意ある攻撃者であれば、過去のライトニング決済を無効にすべく、古い未承認トランザクションをブロードキャストして、二重支払いを試みるかもしれません。<br>この対策として、ライトニングネットワークにはジャスティス・トランザクションと呼ばれる仕組みがあります。ジャスティス・トランザクションを利用することで、二重支払いの被害者は被害金額の回復にとどまらず、攻撃者が正当な所有権を持つビットコインを含むチャネルの全残高を獲得できます。<br>ジャスティス・トランザクションは攻撃発生から一定時間内に実行する必要がありますが、全てのライトニングノード運用者が、自身のノードを常時監視して、期限内にジャスティス・トランザクションを実行できるとは限りません。ウォッチタワーを利用してジャスティス・トランザクションの実行をアウトソースすれば、ノード運用者はノードを監視していなくても、ノードがオフラインの時でも、タイムリーにジャスティス・トランザクションを実行できます。|
|ウォレット<br>Wallet<br>2,100 sats | <a id="wallet"></a>ウォレットは公開鍵と秘密鍵を生成して保存するソフトウェアで、ビットコインの送信、受信、および保管に使われます。ウォレットには、モバイルアプリ、デスクトップアプリ、ハードウェアデバイスがあります。ウォレットはこれらの実装の総称であり、セキュリティとプライバシーはウォレット毎に大きく異なります。</br>ウォレットは、ビットコインと暗号の複雑さを抽象化して隠すことで、ビットコインの送受信および保管を容易にしています。ウォレットを使えば、残高とトランザクション履歴の確認、ビットコインを受け取るためのアドレスの表示と共有が簡単に行えます。</br>ウォレット選択時にはセキュリティが高く、プライバシー対策が講じられたウォレットを選ぶこと、ウォレットをインストールしたデバイスの紛失または破損に備えて、ウォレットのバックアップを作成することが重要です。|
|オーファン (孤立) ブロック<br>Orphan Block<br>2,100 sats | <a id="orphan_block"></a>ビットコインブロックチェーンは、通常、約10分間隔で新規ブロックが生成されるよう設計されていますが、時々、2つのブロックがほぼ同時に生成されることがあります。一方のブロックがネットワークを構成するノードの約半数に伝播する間、もう一つのブロックが残りのノードに伝播するケースが考えられます。この場合、どちらのブロックも有効なため、ノードは両方を保持します。その結果、有効なビットコインブロックチェーンが２つ併存することになります。マイナーはどちらか一方のチェーンにブロックを追加していくので、最終的には、一方のチェーンが他方より長くなります。この時点で、全てのノードは長い方を正当なチェーンとみなして残し、短い方のチェーンを破棄します。この破棄されたチェーンに含まれるのが、オーファンブロックです。オーファンブロックは大抵1つですが、理論上、その数に上限はありません。リオルグと呼ばれるチェーン再編成が起きたり、有効な2つのチェーンが同じ長さで併存する期間が長期化すれば、オーファンブロックは増えます。<br>オーファンブロックを生成したマイナーは、マイニング報酬を失うので大きな経済的損失を被ります。そのため、ノード間のブロック伝播スピードを上げて、オーファンブロックの発生を最小化するのがネットワークの使命です。これがビットコインのブロックサイズに上限が設けられており、上限引き上げが受け入れられない理由の1つです。|
|オフチェーン<br>Off-Chain<br>2,100 sats | <a id="off_chain"></a>オフチェーンはビットコインブロックチェーンに登録されていないデータを表す用語です。オフチェーンデータには、ブロックチェーンに登録される前の未承認のビットコイントランザクション、ライトニングネットワーク上のデータ、またはサイドチェーンなどの他のブロックチェーン上のデータなどがあります。|
|オンチェーン<br>On-Chain<br>2,100 sats | <a id="on_chain"></a>オンチェーンはビットコインブロックチェーンに登録されているデータを指す用語で、オフチェーンとの対比で使われます。オフチェーンデータには未承認のビットコイントランザクションやその他のデータがありますが、オンチェーンデータはビットコイントランザクションに限定されます。|
|オラクル問題<br>Oracle Problem<br>2,100 sats | <a id="oracle_problem"></a>オラクル問題は、ブロックチェーン・ネイティブではないデータ、すなわち、ブロックチェーンの外部に存在するデータを、ブロックチェーン上のスマートコントラクトに取り込む際に不可避な問題で、現時点で解決策はありません。（オラクルは外部データの提供者を指します。）通常のビットコイントランザクションは、スマートコントラクトの一種で、公開鍵、署名、タイムスタンプ、ブロック高といったデータを使用します。これらのデータの有効性は、ビットコインブロックチェーンを介して客観的かつ、第三者を信頼することなくトラストレスに証明できます。<br>しかし、スポーツの試合結果、天気、株価などの外部データの有効性をトラストレスに検証して、スマートコントラクトに組み込むことは現時点では不可能です。コントラクト当事者や第三者が提供するデータの真正を保証する仕組みが確立されていないためです。現在、複数のプロジェクトが、オラクルに対する信頼を最小化するスキームの開発に取り組んでいます。|
---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.

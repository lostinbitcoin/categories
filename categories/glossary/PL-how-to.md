---
title: 用語集の翻訳・修正提案プルリクエストの送り方
taxonomy:
    category:<!--- wikiの「1-2-2. カテゴリ & サブカテゴリの一覧」から該当するものを選び、slugを入力（複数選択可） --->
        - xx
    post_tag:<!--- wikiの「1-2-3. タグの一覧」から該当するものを選び、slugを入力（複数選択可） --->
        - xx
---

## 初回作業の流れ
1. <b>GitHubアカウントの作成:</b> [GitHub](https://github.com/)のアカウントを持っていない場合は、GitHubでアカウントを作成します。
1. <b>プロジェクトのリポジトリを開く:</b> GitHub上にある[ロストイン・ビットコインのリポジトリ]( https://github.com/lostinbitcoin/categories/)（ファイルや変更履歴ためておくデータベースのようなもの）を開きます。
1. <b>フォークの作成:</b> リポジトリのページの右上にある「Fork」ボタンをクリックすると、自分のアカウントの下にロストイン・ビットコインのリポジトリのコピー（fork、フォーク）が作成されます。
1. <b>リポジトリの選択:</b>自分のリポジトリのリスト（https://github.com/[GitHubのユーザー名]?tab=repositories）から、前のステップでフォークしたリポジトリを選びます（https://github.com/[GitHubのユーザー名]/categories）。
1. <b>ブランチの作成:</b> ブランチのドロップダウンメニューをクリックします。新しいブランチ名（例えば、「XXXの翻訳」など）を入力すると、「Create branch: [ブランチ名]」と表示され、クリックするとブランチが作成されます。
1. <b>ファイルの編集:</b> 作成したブランチで翻訳したいファイルを選択し、「Edit」ボタンをクリックし、ファイルの内容を編集します。どのブランチで作業しているのかは、画面左のメニューで確認できるほか、ファイルのURLでも確認できます。 
1. <b>コミット</b>: 編集が終わったら、「Commit changes」ボタンをクリックして、メッセージを記入し、変更を保存（コミット）します。
1. <b>プルリクエストの作成</b>: 「Pull requests」タブをクリックして、「New pull request」ボタンをクリックします。変更を加えたブランチを選択し、内容を確認し、「Create pull request」ボタンをクリックします。
1. <b>プルリクエストの詳細を記入、送信</b>: プルリクエストのタイトルと詳細な説明を記入し、「Create pull request」ボタンをクリックすると、プルリクエストが送信されます。

## 初回以降の作業の流れ
1. 自分のアカウントの下にフォークしたリポジトリを、ロストイン・ビットコインのリポジトリに同期します。
1. 初回作業の「ブランチの作成」から「プルリクエストの詳細を記入、送信」までを行います。

|  ![Category](/_images/category.png)  | <!--- 選択したカテゴリslugに対応する名称を入力 ---> |  ![Tag](/_images/tag.png)  | <!--- 選択したタグslugに対応する名称を入力 ---> | ![Time](/_images/timer.png)  | <!--- コンテンツ消費にかかる時間を入力（記事は700文字/分で計算、動画は再生時間） --->分  |
| ---- | ---- | ---- | ---- | ---- | ---- |

<!--- 以下の例のように、オリジナルコンテンツの説明（著作権者、公開日時、公開媒体など）、邦訳文や日本語字幕を作成した場合は訳者、検証者を *斜体* で記載 --->
*本記事は[lostinbitcoin.jpの用語集](https://lostinbitcoin.jp/glossary/glossary-index/)の翻訳・修正提案プルリクエストをGitHubで送る方法を説明するもので、[@akipponn](https://twitter.com/akipponn) が草稿を執筆し、[@XXX](XXX) さんが一部加筆修正したものです。*

<!--- コンテンツの意図や要約文（省略可） --->
[lostinbitcoin.jpの用語集](https://lostinbitcoin.jp/glossary/glossary-index/)の用語の訳文の変更履歴の管理には、プログラムのソースコードのバージョン管理に利用されることの多いGitHubを利用しています。
本記事では、GitHub翻訳・修正提案を作成し、送信する方法を説明します。

<!--- 画像の表示法: 画像を /_images/ にアップロード後、alt属性と相対パスを入力 --->
[![](/_images/the_great_plague_of_shitconery_1.webp <!--- 相対パス --->)]
<!--- 画像にリンク先がある場合はalt属性を入力、そうでない場合はalt属性を空欄にする --->
[![Newsletters - Bitcoin Optech <!--- alt属性 --->](/_images/bitcoin_optech_newsletters.png)](https://bitcoinops.org/ja/newsletters/)

<!--- 画像やチャートのキャプション表示法 --->
<figcaption>キャプション</figcaption>


### 著作権等について <!--- A、Bのうち該当する利用規約を残し、他方を削除 --->
[利用規約 A](http://lostinbitcoin.jp.testrs.jp/staging/copyright/#uaa) <!--- クリエイター（邦訳コンテンツはオリジナルコンテンツのクリエイター）に利用許可を得ている場合 --->
[利用規約 B](http://lostinbitcoin.jp.testrs.jp/staging/copyright/#uab) <!--- クリエイター（邦訳コンテンツはオリジナルコンテンツのクリエイター）に利用許可を得ていない場合 --->

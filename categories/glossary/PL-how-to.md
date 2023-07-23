---
title: 用語集の翻訳・修正提案プルリクエストの送り方
taxonomy:
    category:<!--- wikiの「1-2-2. カテゴリ & サブカテゴリの一覧」から該当するものを選び、slugを入力（複数選択可） --->
        - xx
    post_tag:<!--- wikiの「1-2-3. タグの一覧」から該当するものを選び、slugを入力（複数選択可） --->
        - xx
---

## 初回の作業の流れ
1. <b>GitHubアカウントの作成:</b> GitHubのアカウントを持っていない場合はアカウントを作成します。
1. プロジェクトのリポジトリを開く: GitHub上のロストイン・ビットコインのリポジトリ（ファイルや変更履歴ためておくデータベースのようなもの）を開きます。 https://github.com/lostinbitcoin/categories/
1. Forkの作成: リポジトリのページの右上にある「Fork」ボタンをクリックします。これにより、自分のアカウント上にプロジェクトのコピー（fork、フォークといいます）が作成されます。
1. 自分のリポジトリのリスト（https://github.com/[GitHubのユーザー名]?tab=repositories）から、フォーク下リポジトリを選びます（https://github.com/[GitHubのユーザー名]/categories）。
1. ブランチの作成: 「master」ドロップダウンメニューをクリックします。新しいブランチ名（例えば、「XXXの翻訳」など）を入力すると、「Create branch: [ブランチ名]」と表示され、クリックするとブランチが作成されます。
1. ファイルの編集: 作成したブランチで翻訳したいファイルを選択し、「Edit」ボタンをクリックし、ファイルの内容を編集します。どのブランチで作業しているのかは、画面左のメニューで確認できるほか、ファイルのURLでも確認できます。 
1. コミット: 編集が終わったら、「Commit changes」ボタンをクリックします。メッセージを記入して、コミットします。
1. プルリクエストの作成: 「Pull requests」タブをクリックして、「New pull request」ボタンをクリックします。変更を加えたブランチを選択し、その内容を確認した後、「Create pull request」ボタンをクリックします。
1. プルリクエストの詳細を記入、送信: プルリクエストのタイトルと詳細な説明を書いてから、「Create pull request」ボタンを再度クリックします。

## 初回以降の作業の流れ

|  ![Category](/_images/category.png)  | <!--- 選択したカテゴリslugに対応する名称を入力 ---> |  ![Tag](/_images/tag.png)  | <!--- 選択したタグslugに対応する名称を入力 ---> | ![Time](/_images/timer.png)  | <!--- コンテンツ消費にかかる時間を入力（記事は700文字/分で計算、動画は再生時間） --->分  |
| ---- | ---- | ---- | ---- | ---- | ---- |

<!--- 以下の例のように、オリジナルコンテンツの説明（著作権者、公開日時、公開媒体など）、邦訳文や日本語字幕を作成した場合は訳者、検証者を *斜体* で記載 --->
*本記事は[lostinbitcoin.jpの用語集](https://lostinbitcoin.jp/glossary/glossary-index/)の翻訳・修正提案プルリクエストの送り方を説明するもので、[@akipponn](https://twitter.com/akipponn) が草稿を執筆し、[@XXX](XXX) さんが一部加筆修正したものです。*

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

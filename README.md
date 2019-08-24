# VocaMiner

## 概要
Vocaloidの楽曲をランダムで発掘してくれる簡易WEBサービスです。利用は無料です。

## 目的・方針
- 新しいボカロ曲・作者に出会いたい人を支援する。
- 簡単に使える事を最優先する。
- ニコニコ動画にはない価値を提供する。

## 使い方
[こちら](https://yumuta.github.io/vocaminer/)から最新バージョンを利用できます。


ご自身のデスクトップにダウンロードして個人利用されたいという場合は以下の手順で行ってください。
1. このリポジトリをローカルにクローン(またはzip保存)
2. nodeおよびnpm環境を用意
3. npm install & npm run start でサーバーが立ち上がります。
4. index.htmlをブラウザで開き、検索ボタンをクリック

server.jsから[ニコニココンテンツAPI](https://site.nicovideo.jp/search-api-docs/search.html)を叩くことで、ニコニコのデータベースから情報を取得するという仕組みです。つまりserver.jsはプロキシの役割です。


本番環境では[Glitch](https://glitch.com/)を間借りしてserver.jsを動かしています。
https://glitch.com/~rigorous-wholesaler

## 開発について
Yumuta・すだが中心となり、ゆるく開発しています。


- [Yumuta](http://yumuta.github.io) - 開発リーダー / サービス設計 / フロント実装
- [すだ](https://twitter.com/dozensofdars) - バックエンド実装 / アルゴリズム設計

## 開発に協力したい
ありがとうございます！Version 2.0リリース以降、Yumutaの対処できる範囲で、有志の方によるプルリクエストを是非受け付けたいと思っております。


参加条件：GitHubのアカウントを持っており、Gitの基本操作が出来る事。


使用言語：HTML, CSS, JavaScript (ES2015~), node.js


開発は**develop**ブランチをベースに行います。具体的には以下のフローとなります。
1. VocaMinerのリポジトリをフォーク
2. ローカルリポジトリにクローン
3. 最新の**develop**ブランチから新しくブランチを分岐してください
    - 追加または修正の内容がわかるようなブランチ名にする
    - 機能追加例：git checkout -b add-genre-to-search-option
    - バグ修正例：git checkout -b fix-typo
5. 適宜、リモートブランチにpushする
6. 変更が収束したら、**develop**にマージするプルリクエストを行ってください。
    - github上で行う
7. **PRのマージはYumuta自身が行います**

皆様が育ててくださったdevelopブランチは、適宜pre-releaseブランチにマージされます。pre-releaseブランチは本番環境向けの修正をコミットしたのちにmasterブランチにマージされ、新バージョンのリリースとなります。これらの作業はYumutaが行います。

## バージョン履歴
### Ver 2.0 (2019.8.24)
- 検索オプションを指定する機能追加
    - 投稿年
    - 再生数
    - キャラクター
- 検索アルゴリズム変更による「検索結果なし」の頻度の削減
- 画面デザイン変更
### Ver 1.1 (2019.3.9)
- nm*** 形式の動画への対応
### Ver 1.0 (2019.3.9)
- 最低限の機能を実装して公開
    - ミクオリジナル曲限定
    - 再生数0~30000からランダムに数字を一つ決めて、niconico APIをfetch
- Twitter投稿機能を設置


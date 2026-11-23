# Codex や ChatGPT Work の学習メモ

* 2026年11月
* 参考ブログ
    - [Codex on Bedrock や ChatGPT desktop on Bedrock を試してみる](https://zenn.dev/aws_japan/articles/4158efc6ca2b5d)
* 参考図書
    - https://book.impress.co.jp/books/1126101075

## ChatGPT のアプリの形態

* Desktop 版と Web 版
* ChatGPT Free プランでは Desktop　のみ使用可能。Web 版は使用できない。
* Web 版はローカルのファイルを操作できない。

## ChatGPT の種類

* ChatGPT: 短い会話用
* ChatGPT Work: 日々の日常業務
* ChatGPT Codex: アプリ開発

## ChatGPT Work のインストール

* Microsoft Store または OpenAI 公式サイトから


## on Bedrock との切り替え

* .env を別名にする
* config.toml の切り替え
* Desktop アプリで「サインアウト」して再度サインイン
* 新規チャットから始める

## on Bedrcok にした場合

* 左上に表示される内容が違う？

    - 普通: ChatGPT または Codex と表示される。ChatGPT を選択すると、中央上に chat か work のタブが表示される
    - Bedrock: ChatGPT Work または Codex と表示される。

* 組み込みブラウザーが使えない
    - 表示はできるが、操作できない

* OpenAI公式の Google Calendar プラグイン は、ChatGPT Work on Amazon Bedrock ではそのまま使えません。
公式プラグインは ChatGPT のアカウント認証および OpenAI 側のクラウドコネクタ経由で Google アカウントと OAuth 連携する仕組みのため、AWS認証（Bedrock経由）のみの環境では利用できない制限に該当します。
代わりに、MCP（Model Context Protocol）サーバーをローカルや自社環境に立てて接続することで、同様のカレンダー操作が実現できます。


## プラグイン

* 有料版の場合はプラグインを追加できる
* 無料版ではDeskTop盤のみ、限定的に使えるが、Google Calendarなどは使えない


## スキル

* 無料版では使えない

## ChatGPT Work のプロジェクト

* 作業に必要なファイルや作成物をまとめるフォルダ
* いわゆるワークスペースフォルダ
* コンテキストになるファイルや編集対象のファイル、作成したファイルを格納


## 全プロジェクトの共通のルール

* ChatGPT Work やCodexを使用するうえで全プロジェクトで共通のルールを設定したい場合
    - ChatGPT Work：［設定］→［パーソナライズ］でカスタマイズを有効にし、［カスタム指示］に共通ルールを書く。プロジェクト固有の指示がある場合はそちらが優先されるため、必ず適用したいルールはそのプロジェクトの指示にも入れる。 
      ローカルの Codex：Windows なら %USERPROFILE%\.codex\AGENTS.md を作り、共通ルールを書きます。リポジトリ内の AGENTS.md に異なる指示がある場合は、そちらが優先されます。

# AI-DLC with Codex

* Codex CLI は特に問題なし
    - サンドボックスの作成ができないのでサンドボックス外で実施となる

* デスクトップアプリのCodex では動作が不安定で実質使用できず
    - フックの信頼が反映されない
    - 作業記録を作るコマンドが Unknown scope: "express"になった。
      作業が記録できない状態になり CLI で実施するようなガイドが表示された。






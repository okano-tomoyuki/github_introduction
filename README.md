# Welcome to GitHub World!
GitHubはgitの仕組みを利用したバージョン管理用のプラットフォームサービスです。
このリポジトリでgitとはなにか、GitHubとは何かを学習しましょう。

## What is git?
GitHubについて理解をするためにはまずgitについて理解する必要があります。


``` mermaid
sequenceDiagram
# エイリアス
  participant cl as クライアント
  participant sv as サーバー
  participant db as データベース

  # データ取得コード
  cl ->>+ sv : データ取得要求
  sv ->>+ db : select発行
  db -->>- sv : select結果
  sv -->>- cl : データ取得要求結果

  alt 正常終了
    Note over cl : 取得データ表示
  else エラー
    Note over cl : エラー表示
  end
```

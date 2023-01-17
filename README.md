# Welcome to GitHub World!
GitHubはGitの仕組みを利用したバージョン管理用のプラットフォームサービスです。
このリポジトリでgitとはなにか、GitHubとは何かを学習しましょう。

参考サイト
- https://backlog.com/ja/git-tutorial/

## What is Git?
GitHubについて理解をするためにはまずGitについて理解する必要があります。Gitとは分散型のバージョン管理システムです。
まずはバージョン管理について考えてみましょう。

プログラムを複数人で開発する場合、各個人が開発したプログラムを共有しあう必要があります。
それだけなら共有フォルダなどで共有してしまえばよいのでは？と思うかもしれませんがそれだと問題があります。

一つ目の問題は常に最新化された情報が手に入るとは限らないという点です。
Aさんは共有フォルダから必要なソースコードをダウンロードして

二つ目の問題はプログラムの変更に対して5W1Hがわからないという点です。
5W1Hとは
- 何を(What)
- 誰が(Who)
- いつ(When)
- どこで(Where)
- なぜ(Why)
- どのように(How)

``` mermaid
%%{init: { 'theme': 'dark' ,'themeVariables': {
  'commitLabelColor': '#ffffff',
  'commitLabelBackground': '#ff0000'
} } }%%
gitGraph
  commit id: "プロジェクト作成"
  commit id: "犬クラス作成"
  commit id: "犬クラスに吠える機能実装"
  commit id: "犬クラスに食べる機能実装"
  branch develop
  checkout develop
  commit
  commit
  commit
  checkout main
  merge develop
```

``` mermaid
graph BT

  subgraph GitHub
    RemoteRepository
  end
  
  subgraph UserA 
    LocalRepository1
  end
  
  subgraph UserB
    LocalRepository2
  end
  
  LocalRepository1 --> RemoteRepository
  LocalRepository2 --> RemoteRepository
  
```

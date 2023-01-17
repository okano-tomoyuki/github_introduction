# Welcome to GitHub World!
GitHubはGitの仕組みを利用したバージョン管理用のプラットフォームサービスです。
このリポジトリでgitとはなにか、GitHubとは何かを学習しましょう。

参考サイト
- https://backlog.com/ja/git-tutorial/

## What is Git?
GitHubについて理解をするためにはまずGitについて理解する必要があります。Gitとは分散型のバージョン管理システムです。
バージョン管理とはどのようなものでしょうか？下記をご覧ください。

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

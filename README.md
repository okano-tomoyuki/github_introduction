# Welcome to GitHub World!
GitHubはgitの仕組みを利用したバージョン管理用のプラットフォームサービスです。
このリポジトリでgitとはなにか、GitHubとは何かを学習しましょう。

参考サイト
- https://backlog.com/ja/git-tutorial/

## What is git?
GitHubについて理解をするためにはまずgitについて理解する必要があります。


``` mermaid
graph BT

  subgraph Remote Repository
    GitHub
  end
  
  subgraph Local Repository 
    UserA
  end
  
  subgraph Local Repository
    UserB
  end
  
  UserA --> GitHub
  UserB --> GitHub
```

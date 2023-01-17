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
Aさんは共有フォルダから必要なソースコードをダウンロードして開発を行ったとします。
Aさんは犬についてのプログラムを書いているとして、犬の吠えるという機能を実装しようとしています。
苦労してプログラムを完成させ、いざ共有しようとするとすでに別のBさんという人が吠える機能についての
コードを完成させていました。これではAさんの努力は水の泡です。
Gitの仕組みを活用することで現在開発中のプログラムが常に最新の状態か確認することが可能です。
これでAさんの努力が今後無駄になることはないでしょう。

二つ目の問題はプログラムの変更に対して5W1Hがわからないという点です。プログラムの変更に対して
- 何を(What)
- 誰が(Who)
- いつ(When)
- どこで(Where)
- なぜ(Why)
- どのように(How)
といった付属の情報がないと後から開発作業に着手するユーザは何のことやらさっぱりわからなくなります。
例えばさっきの犬プログラムを考えてみましょう。新たに開発に参加したCさんは犬プログラムの改良に取り掛かっています。
そんなときプログラム中に以下のような箇所を見つけました。

```
void shout() {
  std::string msg="わんわん";
  std::cout << msg << std::endl;
}
```

Cさんは「アメリカだったら"bow wow"と吠えるだろうからこの吠える機能については受け取ったメッセージを出力するように修正しよう。」と以下のように変更しました。

```
void shout(std::string msg) {
  std::cout << msg << std::endl;
}
```
しかしこの変更の意図を知らないAさんは何でこのような変更をCさんが行ったのか理解できず、結果遠く離れたCさんに事情を聴いてやっと変更理由を理解できました。

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

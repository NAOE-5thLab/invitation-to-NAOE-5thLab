# invitation-to-[NAOE-5thLab](https://github.com/NAOE-5thLab)

船舶知能化領域のGitHubアカウントです。運用ルール等についてまとめておきます。



目次

[TOC]

## 運用ルール

基本的な使用ルールをまとめておきます。



### リポジトリ作成

一つの独立したアプリケーション（論文に使ったコードのまとまりとか）に対して一つのリポジトリを作成することを推奨します。

また、リポジトリが大量に作成されることが予想されるため、求めるリポジトリを見つけやすいように以下のルールを守っていただきたいです。

#### リポジトリ名の命名規則

ケバブケース（小文字の英数字を利用、単語の区切りは`-`を使用）の命名を推奨します。また、リポジトリ名だけで内容がわかるように可能な限り丁寧な名前にすることを推奨します。ただし、長すぎる名前は推奨しません。

例

- :o::`sample-git-repository`
- :x::`sample_git_repository`
- :x::`SampleGitRepository`
- :x::`sampleGitRepository`
- :x::`samplegitrepository`

参考

- [gitリポジトリの命名規則](https://zenn.dev/iwatos/articles/cb79814a4b31ed)



#### トピック（タグ）をつける

リポジトリが増えてくると、リポジトリ名をどれだけ工夫していても煩雑になってくる可能性があります。そのため、トピックをせってしておくことで、分類することができ、管理が容易になります。

例

- `stability`
- `system identification`
- `reinforcement learning`

参考

- [トピックでリポジトリを分類する](https://docs.github.com/ja/github/administering-a-repository/managing-repository-settings/classifying-your-repository-with-topics)
- [GitHub で管理している社内リポジトリをトピックで分類する (topics)](https://maku77.github.io/git/github/topics.html)



### リポジトリの運用

Gitを利用することで、自分及び共同開発者のコード変更履歴を全て残しておくことができます。しかし、その使い方を間違えると変更履歴が消えてしまうこともあります。このような事態を防ぐために、最低限守っておいた方が良いであろうルールを記載します。

**共有のレポジトリ**の場合は守ることを推奨しますが、**個人レポジトリ**の場合必ず守る必要はないです。自己責任でお願いします。

#### ブランチ

ブランチはプロジェクトを分岐させることで本体に影響を与えず開発を行うことができる機能です。また、目的別にブランチを切ることで並行して開発を行うことも可能です。

ブランチにはある名前が与えられますが、代表的なものにmainブランチがあります。リポジトリ作成すると最初に生成されるのがmainブランチです。そして、mainブランチから派生させる形で任意の名前のブランチを切ることができます。例えば、mainブランチからdevブランチを切ると、devブランチでコードの変更を行なったとしてもmainブランチに影響はありません。

##### ブランチの必要性

開発を行う上で、最初から思い通りのコードが組めるわけではなく、必ずと言って良いほどバグが発生します。そのため、バグのない完璧なコードにある機能を追加するため、変更を加えると完璧なコードは無くなってしまいます。そこで、ブランチを切ることで、完璧なコードを残しつつ、開発を行うことができます。そして、追加した機能を含め完璧なコードとなれば、元のブランチにマージしてしまえば良いです。

つまり、全てのブランチの元となるmainブランチでは、バグのない完璧なコードを維持することが重要です。また、mainブランチに影響を与えないようにブランチを切っておけば、大きなミスがあったとしてもmainブランチのものは助かります。

##### ブランチの切り方

ブランチの切り方に厳密なルールはないですが、ベストプラクティス的なルールは定められています。有名なものに**git-flow**と**github-flow**が存在します。興味のある方は調べてみてください。

- [A successful Git branching model (Git Flow)](https://nvie.com/posts/a-successful-git-branching-model/)
- [GitHub Flow](http://scottchacon.com/2011/08/31/github-flow.html)

ただ、個人の研究で使用する程度であればここまでする必要はないかもしれません。ですから、最低限の守った方が良いであろうルールを記載しておきます。

まず

- mainブランチで作業しない
- mainブランチから派生したブランチで作業する

が、最も重要であると思われます。また、

- mainブランチにマージする前に先輩や先生に確認してもらう

が可能であれば行う方が良いと思われます。バグやミスが残った状態でマージしてしまうと意味がないので。



### 研究コードの管理以外にも

ノウハウとかメモとか集めたリポジトリも作っておくといかも

- 何かについて調べたまとめ
- 新入生のチュートリアルをまとめておくリポジトリ
- 論文レビューのレポジトリとか





## GitHub Education

申請すればGitHub PROがもらえる。また、一緒にGitHub Student Developer Packが使える。GitHub Student Developer Packで、クラウドサービスとか使えるらしい（AWSもあるって書いてたけど見つからなかった）。Studentだとpro限定っぽいけどTeacher枠ならteamも使える。

参考

- [GitHub Education](https://education.github.com/)
- [Qiita:GitHub Educationのメリットと申請方法](https://qiita.com/Kobayashi2019/items/5adb9bde57691a770419)





## GitHub Organization

[NAOE-5thLab](https://github.com/NAOE-5thLab)は一般のアカウントとは異なるGitHub Organizationのアカウントである。GitHub Organizationについて少しまとめておく。

メリット

- 組織としてのリポジトリを各メンバーが自由に作成できる

### Organization の権限レベル [1]

組織アカウントのメンバーには、オーナー権限かメンバー権限が与えられる。それぞれ以下のような権限をもつ。

- オーナー権限
  - できないことは無い
- メンバー権限
  - リポジトリの作成
  - Team を作成する
  - プロジェクトボードを作成する
  - Organization の全メンバーおよび Team の表示
  - 参照可能なチームへの @メンション
  - *チームメンテナ*に指定できる
  - Organization のインサイトを表示する
  - パブリック Team のディスカッションを表示し、**すべての Team** に投稿する
  - ミット、プルリクエスト、Issue についてコメントを非表示にする
  - アカウントをスポンサーし、Organization のスポンサーシップを管理する

### Organization のリポジトリ権限レベル [2]

オーナー権限やメンバー権限とは別に、全てのメンバーにはリポジトリごとに閲覧や編集の権限が与えられる。主に、リポジトリ作成者にはadmin権限が与えられ、その他のメンバーには閲覧権限のみ与えられます。リポジトリ作成者から招待を得ることでそのメンバーのみ編集が可能となります。

- **Read**: プロジェクトを表示またはプロジェクトについてディスカッションしたい、コードを書かないコントリビューターにおすすめします
- **Triage**: 書き込みアクセスなしに、Issue やプルリクエストを積極的に 管理したいコントリビューターにおすすめします
- **Write**: プロジェクトに積極的にプッシュしたいコントリビューターにおすすめします
- **Maintain**: センシティブ、または破壊的なアクションにアクセスせずにリポジトリを管理する必要がある、プロジェクト管理者におすすめします
- **Admin**: セキュリティの管理やリポジトリの削除など、センシティブおよび破壊的なアクションを含めて、プロジェクトへの完全なアクセスが必要な人におすすめします

Reference

1. [Organization の権限レベル](https://docs.github.com/ja/organizations/managing-peoples-access-to-your-organization-with-roles/permission-levels-for-an-organization)
2. [Organization のリポジトリ権限レベル](https://docs.github.com/ja/organizations/managing-access-to-your-organizations-repositories/repository-permission-levels-for-an-organization)
3. [GitHubでリポジトリを組織管理するためのOrganizationとそのつくり方](https://tonari-it.com/github-organization/)




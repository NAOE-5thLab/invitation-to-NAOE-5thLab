# GitHub Organization

個人ではなく組織が管理するアカウント



メリット

- 組織としてのリポジトリを各メンバーが自由に作成できる
- 危険な操作（マージなど）の制限を行える



## Organization の権限レベル [1]

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



## Organization のリポジトリ権限レベル [2]

- **Read**: プロジェクトを表示またはプロジェクトについてディスカッションしたい、コードを書かないコントリビューターにおすすめします
- **Triage**: 書き込みアクセスなしに、Issue やプルリクエストを積極的に 管理したいコントリビューターにおすすめします
- **Write**: プロジェクトに積極的にプッシュしたいコントリビューターにおすすめします
- **Maintain**: センシティブ、または破壊的なアクションにアクセスせずにリポジトリを管理する必要がある、プロジェクト管理者におすすめします
- **Admin**: セキュリティの管理やリポジトリの削除など、センシティブおよび破壊的なアクションを含めて、プロジェクトへの完全なアクセスが必要な人におすすめします



## できること

### オーナー

自分で調べてください。

### メンバー

#### レポジトリの作成

個人レポジトリと同様に作成できる。ただし、Ownerを組織アカウントに変える必要がある。リポジトリを作成するとadmin権限が与えられ、自由に編集することができる。共同開発の場合はメンバーを招待する必要がある。

#### 各レポジトリの権限

デフォルトでは、関係のないレポジトリには閲覧権限しかない。しかし、作成したレポジトリや招待されたレポジトリはそれに応じた権限が与えられる。

#### フォークの使用

レポジトリの権限で「Write」権限を与えるとマージができるようになってしまう。これが危険だと思う場合は、フォークを行いプルリクエストを行い最終的なマージはリポジトリの責任者に任せることができる。



Reference

1. [Organization の権限レベル](https://docs.github.com/ja/organizations/managing-peoples-access-to-your-organization-with-roles/permission-levels-for-an-organization)
2. [Organization のリポジトリ権限レベル](https://docs.github.com/ja/organizations/managing-access-to-your-organizations-repositories/repository-permission-levels-for-an-organization)
3. [GitHubでリポジトリを組織管理するためのOrganizationとそのつくり方](https://tonari-it.com/github-organization/)


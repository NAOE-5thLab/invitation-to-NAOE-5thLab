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




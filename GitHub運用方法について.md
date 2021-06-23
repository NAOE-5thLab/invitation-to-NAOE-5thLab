6/25に言いたいこと

- プロジェクトの切り方を決めるためにslackのチャンネルに入ってもらうこと
- 五講全員で使えるので、統一したほうがオープン？
- アカウント名（今は、NAOE-5thLab）の相談





# GitHub運用方法

**動機**

一つのプロジェクトに複数のプロジェクトが入りすぎて管理しにくい状況になってきたため、運用方法を考え直すことにしました。

**目的**

- プロジェクトを分割して使いやすくする
- 複数人開発の場合はブランチの切り方をルール化する



## 運用方法

### 現状

- 管理形態：[AtsuoMAKI/5th-Lab ](https://github.com/AtsuoMAKI/5th-Lab)で全てのプロジェクトを管理
- ブランチ切り方：個人の作業を各ブランチで行い、勝手なタイミングでMasterに筋肉マージ
- リポジトリ概要

```
.
├── Berthing
│   ├── Berthing_by_TD3
│   ├── CMA_NN_Online_berthing
│   ├── CMA_Offline_Berthing
│   └── collision_detection_module
├── Docker
├── Hydro
│   ├── Environments_of_OpenAI_gym
│   ├── LargeRudderAngle
│   ├── MMG
│   ├── MMG_1p2r
│   └── MMG_C++_Vectwin
├── README.md
├── SI
│   ├── Animation
│   ├── CMA-ES
│   ├── Generative_Adversarial_Network
│   ├── NN_CMA-ES
│   ├── Neural_Network
│   └── traj_gp
├── Tracking
│   ├── CMA_NN_Tracking
│   ├── MDN_Tracking
│   ├── SMC_Tracking
│   ├── Servo_Mechanism_for_Velocity
│   └── TracikngControl_by_TD3
├── exp_data
│   ├── ESSO
│   ├── README.md
│   ├── TAKAOKI
│   └── berth_coordinate.png
├── model_ship
└── naming_rule
    ├── list_of_names.csv
    └── naming_rule.md
```

##### 何が良くないか

- クローンするのに全てのプロジェクトがついてくる
- 管理者が牧先生だけなので、何かと不便
- 誰かがリポジトリを壊すと仲良死する



### 今後の運用方法（案）

管理形態

- 研究室用のOrganizationアカウントを作成（誰でもいい）
  - メンバーを追加してから、オーナー権限を誰かに渡して、以降は生徒側で管理
  - 現在の運用でproやらTeamに申請する必要があるのかは疑問
    - GitHub Educationを使うとproとteamが無料で使える
    - プライベートリポジトリが無制限で使用できさえすればいい？
    - パッケージ公開することもない



ブランチの切り方

- これはプロジェクトごとによるが、初心者が困らない程度の基本ルールだけ決める方がいいかもしれない
  - 基本ルール（**ご相談**）
    - `main`では作業はしない。
      - リリースの概念がないので、論文に使用した時点でのコードをバージョンで管理するとか？
    - `develop`がメインの作業場にする。
    - 複数人数で開発する場合`feature`を使用する



プロジェクトをどのように分割するか（**ご相談**）
- 独立できる最小単位で分割する？
  - vectwinがEssoのMMGに基づいてるなら同じプロジェクトでもいい？
  - SIはそれぞれの手法は完全に独立しているので
- リポジトリ間の依存をどうするべきか？
  - NNのSIではプロジェクトで独立するためにMMG（バージョン不明）はコピペしている



### 現状のリポジトリからの分離方法

運用方法が決まったら和田さんに相談



### 運用が始まってから（ポリシー、規則みたいな）

- プロジェクト名の命名規則
  - 見やすさと検索しやすさの向上
- プロジェクトにトピック（タグ）をつける
  - 検索しやすさの向上
  - `SI`、`ML`、`STAB`みたいな



## 前から思っていたこと（意味ないかもしれないですが）

- ノウハウとかメモとか集めたプロジェクトがあるといいかも
  - 命名規則、Docker使い方とか
  - 何かについて調べたまとめとか
  - あとは、新入生のチュートリアルをまとめておくリポジトリとか
  - 論文レビューのレポジトリとか





# 付録

調べたことをまとめておきます。



## GitHub Organization

Organizationアカウントは個人ではなく組織が管理するアカウントになる。

- できること
  - リポジトリの作成・管理
    - 権限に応じて組織内のメンバーが編集可能
  - メンバーの追加・削除
    - オーナー権限所有者が管理できる
    - オーナー権限の譲渡も可能
  - Teamの作成・管理
    - チームごとにまとめて権限を管理することができる。
    - 少人数の場合必要ない

参考

- [Qitta:githubのorganizationアカウントの運営について](https://qiita.com/chari/items/ee16bf16715f4bbcbd9b)



## GitHub Education

申請すればGitHub PROがもらえる。また、一緒にGitHub Student Developer Packが使える。GitHub Student Developer Packで、クラウドサービスとか使えるらしい（AWSもあるって書いてたけど見つからなかった）。Studentだとpro限定っぽいけどTeacher枠ならteamも使える。

参考

- [GitHub Education](https://education.github.com/)
- [Qiita:GitHub Educationのメリットと申請方法](https://qiita.com/Kobayashi2019/items/5adb9bde57691a770419)



## ブランチの切り方の例 

- `main` : 安定動作版。このソースコードを実機に書き込んだり、また検証用シミュレータに取り込んでも問題が起こらないとされているバージョン。
- `release` : `develop`→`main`のmergeが大変なときに使う一時的なbranch。`main`へのmerge時に`develop`の更新を止めないようにするためにつくる。
- `develop` : `feature`で実装され、検証が終わったら`develop`にmergeされる。したがって、おそらく問題ないと思われているコードの最新版が集積される。
- `feature` : 機能開発branch。`develop`から切られ，`develop`にmergeされる。

<img src=./img/git-model.png width=80%>

参考

- [澤田さんにもらった参考](https://meltingrabbit.com/blog/article/2020052701/#h2-7)








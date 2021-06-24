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
- 誰かがリポジトリを壊すと仲良死する:scream:



### 今後の運用方法（案）

#### [GitHub Organization](https://github.com/NAOE-5thLab)の利用

Organizationアカウントは個人ではなく組織が管理するアカウントになる。

- できること
  - リポジトリの作成・管理
    - 全て組織内のメンバーがリポジトリを作成可能
    - リポジトリ作成者がそのリポジトリのadmin権限を持つ
    - リポジトリに組織メンバーを招待可能
  - メンバーの追加・削除
    - オーナー権限所有者が管理できる
    - オーナー権限の譲渡も可能
  - Teamの作成・管理
    - チームごとにまとめて権限を管理することができる
    - 少人数の場合必要ない

参考

- [Qitta:githubのorganizationアカウントの運営について](https://qiita.com/chari/items/ee16bf16715f4bbcbd9b)



##### メリット

- 全員が組織アカウントに自由にリポジトリを作成できる
- 管理者を複数人設定できる
- 制御班とか関係なく研究室内の全てのソースコードをまとめられて、全ての研究室メンバーの研究コードを見れる



#### 前から思っていたこと（意味ないかもしれないですが）

ノウハウとかメモとか集めたプロジェクトがあるといいかも

- 命名規則、Docker使い方とか
- 何かについて調べたまとめとか
- あとは、新入生のチュートリアルをまとめておくリポジトリとか
- 論文レビューのレポジトリとか



### もしこの運用が始まった場合

リポジトリ名とかの簡単なルールだけ決めようと思っています。それに従って作業をしていただくことになると思います。

- リポジトリ名の命名規則
- ブランチの切り方

など







## GitHub Education

申請すればGitHub PROがもらえる。また、一緒にGitHub Student Developer Packが使える。GitHub Student Developer Packで、クラウドサービスとか使えるらしい（AWSもあるって書いてたけど見つからなかった）。Studentだとpro限定っぽいけどTeacher枠ならteamも使える。

参考

- [GitHub Education](https://education.github.com/)
- [Qiita:GitHub Educationのメリットと申請方法](https://qiita.com/Kobayashi2019/items/5adb9bde57691a770419)


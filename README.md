# アプリ名
catマッチングアプリ
# 概要
保護猫の里親サイト　人間と猫のマッチングアプリケーション
# 制作背景（意図）
保護猫活動をしていて、猫を譲渡する際に既存の里親サイトを使用していました。しかし、既存の里親サイトで里親詐欺や虐待が実在するとニュースなどで知っていました。
そのためそのような犯罪から猫を守るため、犯罪を未然に防げる充実したアプリがあったらいいなという思いから作成しました。
# DEMO
### トップページ
https://gyazo.com/97a6370ed3388d0eab82ac9d13255b75
### 会員情報入力画面
https://gyazo.com/ec15f9bb657c52b02da98eac947579e2
### 新規猫情報入力画面
https://gyazo.com/74be6d06c90c9c0971143e269e29415f
# 工夫したポイント
トップページではペットショップでなく保護猫を選ぶ理由を記載して、写真を用いて目につくようにしました。
会員情報入力画面では猫を譲渡する側が最初から欲しい情報を入力必須にしました。身分証を入力必須にして里親詐欺や虐待防止に繋げます。
新規猫情報入力画面では猫の細かい情報を入力するように、例文を入力しました。
# 実装予定の内容
ユーザーの希望の猫がおすすめに出てくるように実装する予定です。
また猫を投稿する側にもお勧めのユーザーが出てくるようにします。
お互いのニーズにマッチした猫を安全に譲渡するお手伝いをします。
身分証は猫を譲渡する側には必要な情報なので、どのように安全に情報を開示するかが課題です。
# DB設計
### users テーブル

| Column                 | Type   | Options                   |
| ------------------     | ------ | ------------------------- |
| nickname               | string | null: false               |
| email                  | string | null: false, unique: true | 
| encrypted_password     | string | null: false               |
| last_name              | string | null: false               |
| first_name             | string | null: false               |
| last_name_kana         | string | null: false               |
| first_name_kana        | string | null: false               |
| family_structure       | string | null: false               |  
| raise_experience       | string | null: false               |
| ID                     | string | null: false               |
| picture_house          | string | null: false               |
| SNS_account            | string | null: false               |
| raise_environment      | string | null: false               |
| birthday               | date   | null: false               |

### adopt テーブル

| Column               | Type       | Options                 |
| ------               | ------     | ------------            |
| cat_title            | string     | null: false             |
| cat_description      | text       | null: false             |
| sex                  | integer    | null: false             |
| age                  | integer    | null: false             |
| operation            | integer    | null: false             |
| prefecture           | integer    | null: false             |
| apply_reason         | integer    | null: false             |


## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|group_name|text|null :false|
|user_id|integer|null: false|

### Association
- has_many :users


## usersテーブル

|Column|Type|Options|
|------|----|-------|
|id|integer|null :false|
|name|text|null: false|
｜email｜text｜null: false｜
|password|text|null: false|

### Association
- has_many :groups
- has_many :posts, through: :groups

## postsテーブル
|Column|Type|Options|
|------|----|-------|
|message|text|null :false|
|image|text|
｜group_id｜integer｜null: false, foreign_key: true｜
｜user_id｜integer｜null: false, foreign_key: true｜

### Association
- belongs_to :user
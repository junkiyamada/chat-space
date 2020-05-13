## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user


## usersテーブル

|Column|Type|Options|
|------|----|-------|
|id|integer|null :false|
|name|text|null: false|
｜email｜text｜null: false｜

### Association
- has_many :groups
- has_many :posts

## postsテーブル
|Column|Type|Options|
|------|----|-------|
|message|text|null :false|
|image|text|
｜created_at｜integer｜null: false｜

### Association
- belongs_to :user
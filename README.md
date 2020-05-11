## usersテーブル

|Column|Type|Options|
|------|----|-------|
|e-mail|string|null: false|
|password|string|null: false|
|name|string|null: false|

### Association
- has_many :messages
- has_many :groups_users
- has_many :groups,through: :groups_users

## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|

- belongs_to :user
- belongs_to :groups

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|name|string｜null: false, foreign_key: true|


### Association
- belongs_to :user
- has_many:messages,through: :groups_users

## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|text|string｜
|image|string|
|user_id|null: false, foreign_key: true|
|group_id|null: false, foreign_key: true|

### Association
-belongs_to :user
-has_many :groups

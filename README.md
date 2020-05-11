## usersテーブル

|Column|Type|Options|
|------|----|-------|
|e_mail|string|null: false|
|password|string|null: false|
|name|string|index: true,null: false|

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
- belongs_to :group

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|name|string｜null: false|


### Association
- has_many :messages
- has_many :groups_users
- has_many :users, through: :groups_users

## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|text|text｜
|image|string|
|user_id|references|null: false, foreign_key: true|
|group_id|references|null: false, foreign_key: true|

### Association
-belongs_to :user
-belongs_to :group

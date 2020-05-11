## usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer_index|null: false, foreign_key: true|
|group_id|integer_index|null: false, foreign_key: true|
|e-mail|text|
|pasward|text|
|name|text|
|group_name|
|chat_group|


## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer_index|null: false, foreign_key: true|
|group_id|integer_index|null: false, foreign_key: true|
|name|text|
|group_name|text|
|chat_log|datatime|

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer_index|null: false, foreign_key: true|
|group_id|integer_index|null: false, foreign_key: true|
|name|text｜
|group_name|text|
|chat_log|datatime|

### Association
- belongs_to :group
- belongs_to :user


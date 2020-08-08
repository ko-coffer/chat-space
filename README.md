# README

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|index: true, null: false, unique: true|
|mail|string|null: false|
|password|string|null: false|

## Association

- has_many :group
- belongs_to :group




## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|group_name|string|index: true, null: false, unique: true|
|user_id|integer|null: false, foreign_key: true|

## Association

- has_many :user
- belongs_to :user




## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user


## messagesテーブル

|Column|Type|Options|
|------|----|-------|
|image|text||
|text|text||
|user_id|references|null: false, foreign_key: true|
|group_id|references|null: false, foreign_key: true|
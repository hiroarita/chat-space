# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
USER Table
｜Column｜name｜email｜password｜
｜name｜string｜null：false｜
|email|string|null:false
|password|string|null:false

Association
has_many :messages
has_many :members
has_many :groups


MESSAGE Table
｜Column｜text｜image｜user＿ID｜group＿ID|
|text|text|
|image|string|
|user_id|integer|null:false,foreign_key: true|

Association
belong_to :user
belong_to :group


GROUP Table
|Column|name|
|name|string|null:false|

Association
has_many :messages
has_many :members

GROUP_USER Table
|Column|user_id|group_id|
|user_id|integra|null:false,foreign_key:true|
|group_id|integer|null:false,foreign_key:true|

Association
belongs_to :group
belongs_to :user

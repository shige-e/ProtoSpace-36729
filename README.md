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


## users テーブル

| Clounm            | Type     | Options       |
| ----------------- | -------- | --------------|
| email             | string   | NOT NULL      |
| password          | string   | NOT NULL      |
| name              | string   | NOT NULL      |
| profile           | text     | NOT NULL      |
| occupation        | text     | NOT NULL      |
| position          | text     | NOT NULL      |

### Association

- has_many :comments
- has_manu :prototuoes

## comments テーブル

| Clounm            | Type         | Options       |
| ----------------- | ------------ | --------------|
| text              | text         | NOT NULL      |
| use               | references   |               |
| prototype         |              | NOT NULL      |

### Association

- belonf_to :users
- belong_to :prototypes

## prototypes テーブル

| Clounm            | Type         | Options       |
| ----------------- | ------------ | --------------|
| title             | string       | NOT NULL      |
| catch_copy        | text         | NOT NULL      |
| concept           | text         | NOT NULL      |
| user              | references   |               |

### Asspciation

- belong_to :users
- has_many :comments

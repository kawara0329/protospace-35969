# テーブル設計

## users テーブル

| email              | string   | null: false |
| password           | string   | null: false |
| name               | string   | null: false |
| profile            | text     | null: false |
| occupation         | text     | null: false |
| position           | text     | null: false |

## comments テーブル

| text      | text       | null: false |
| user      | references | -------- |
| prototype | references | -------- |

## prototypes テーブル

| title      | string        | null: false |
| catch_copy | text          | -------- |
| concept    | text          | null: false |
| image      | ActiveStorage | null: false |
| user       | references    | -------- |

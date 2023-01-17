# テーブル設計

## users テーブル

| Column             | Type   | Options             |
| ------------------ | ------ | ------------------- |
| email              | string | null: false, key:UNI|　
| encrypted_password | string | null: false         |
| name               | string | null: false         |
| profile            | text   | null: false         |
| occupation         | text   | null: false         |
| position           | text   | null: false         |


## comments テーブル

| Column    | Type       | Options                        |
| -------   | ---------- | ------------------------------ |
| content   | text       | null: false                    |
| prototype | references | null: false, foreign_key: true |
| user      | references | null: false, foreign_key: true |

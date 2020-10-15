# README
## usersテーブル

| column     | type   | option     | 
| ---------- | ------ | ---------- | 
| email      | string | null_false | 
| password   | string | null_false | 
| name       | string | null_false |
| profile    | text   | null_false | 
| occupation | text   | null_false |
| position   | text   | null_false | 

## Association
- has_many :prototypes
- has_many :comments

## prototypeテーブル

| column     | type       | option     | 
| ---------- | ---------- | ---------- | 
| title      | string     | null_false | 
| catch_copy | text       | null_false | 
| concept    | text       | null_false | 
| image      |            |            | 
| user       | references |            |  

## Association
- belongs_to :users
- has_many :comments


## commentsテーブル

| column    | type       | option     | 
| --------- | ---------- | ---------- | 
| text      | text       | null_false | 
| user      | references |            | 
| prototype | references |            | 


## Association
- belongs_to :users
- belongs_to :prototype
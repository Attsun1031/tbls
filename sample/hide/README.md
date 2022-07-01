# testdb

## Description

Sample database document.

## Tables

| Name | Columns | Comment | Type | Labels |
| ---- | ------- | ------- | ---- | ------ |
| [CamelizeTable](CamelizeTable.md) | 2 |  | BASE TABLE |  |
| [comment_stars](comment_stars.md) | 6 |  | BASE TABLE |  |
| [comments](comments.md) | 7 | Comments<br>Multi-line<br>table<br>comment | BASE TABLE |  |
| [hyphen-table](hyphen-table.md) | 3 |  | BASE TABLE |  |
| [logs](logs.md) | 7 | Auditログ | BASE TABLE |  |
| [post_comments](post_comments.md) | 7 | post and comments View table | VIEW |  |
| [posts](posts.md) | 7 | Posts table | BASE TABLE | `green` `red` `blue` |
| [user_options](user_options.md) | 4 | User options table | BASE TABLE |  |
| [users](users.md) | 6 | Users table | BASE TABLE |  |

## Stored procedures and functions

| Name | ReturnType | Arguments | Type |
| ---- | ------- | ------- | ---- |
| CustomerLevel | varchar | credit decimal | FUNCTION |
| GetAllComments |  |  | PROCEDURE |

## Relations

![er](schema.svg)

---

> Generated by [tbls](https://github.com/k1LoW/tbls)
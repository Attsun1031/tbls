# comments

## Description

Blog comments

## Columns

| Name | Type | Default | Nullable | Children | Parents | Comment |
| ---- | ---- | ------- | -------- | -------- | ------- | ------- |
| user_id | INT64 |  | false | [comment_stars](comment_stars.md) | [posts](posts.md) [users](users.md) |  |
| post_id | INT64 |  | false | [comment_stars](comment_stars.md) | [posts](posts.md) |  |
| comment_id | INT64 |  | false |  | [posts](posts.md) |  |
| comment | STRING(MAX) |  | false |  |  |  |
| created | TIMESTAMP |  | false |  |  |  |
| updated | TIMESTAMP (allow_commit_timestamp=TRUE) |  | true |  |  |  |

## Constraints

| Name | Type | Definition |
| ---- | ---- | ---------- |
| PRIMARY_KEY | PRIMARY_KEY | PRIMARY KEY(comment_id, post_id, user_id) |
| INTERLEAVE | INTERLEAVE | INTERLEAVE IN PARENT posts ON DELETE CASCADE |

## Indexes

| Name | Definition |
| ---- | ---------- |
| comments_post_id_user_id_idx | CREATE UNIQUE INDEX comments_post_id_user_id_idx ON comments (post_id, user_id) |
| comments_post_id_idx | CREATE INDEX comments_post_id_idx ON comments (comment_id, post_id, user_id, comment), INTERLEAVE IN posts |

## Relations

![er](comments.png)

---

> Generated by [tbls](https://github.com/k1LoW/tbls)
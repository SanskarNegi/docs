---
title: Repository Pre-receive Hooks
intro: The Repository Pre-receive Hooks API allows you to view and modify enforcement of the pre-receive hooks that are available to a repository.
versions:
  ghes: '*'
topics:
  - API
miniTocMaxHeadingLevel: 3
allowTitleToDifferFromFilename: true
---

### オブジェクトの属性

| 名前                  | 種類       | 説明                     |
| ------------------- | -------- | ---------------------- |
| `name`              | `string` | フックの名前。                |
| `enforcement`       | `string` | このリポジトリでのフックの適用状態。     |
| `configuration_url` | `string` | 適用設定されているエンドポイントの URL。 |

*適用*可能な値は、`enabled`、`disabled`、`testing` です。 `disabled` は、pre-receive フックが実行されないことを示します。 `enabled` は、それが実行され、ゼロ以外の状態になるプッシュを拒否することを示します。 `testing` は、スクリプトは実行されるが、プッシュが拒否されないことを示します。

`configuration_url` は、このリポジトリ、その Organization のオーナー、またはグローバル設定へのリンクである場合があります。 `configuration_url` でエンドポイントにアクセスする権限は、所有者またはサイトアドミンレベルで決定されます。

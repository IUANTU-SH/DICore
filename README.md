DICore
=======

DICore 是一个快速的接口生成工具，使用 GraphQL 查询数据表。DICore 的目标是帮助你快速完成开发任务。

```graphql
{
    contact(id: 1) {
        name
        email
        friends {
            name
            email
        }
    }
}
```

结果

```json
[
    {
        "name": "cj",
        "email": "cj@iuantu.com",
        "friends": [
            {
                "name": "fallout",
                "email": "fallout@iuantu.com"
            }
        ]
    }
]
```

数据表

```
contact
+----+---------+--------------------+------------------+
| id | name    | email              | created_at       |
+----+---------+--------------------+------------------+
| 1  | cj      | cj@iuantu.com      | 2021-01-01 23:00 |
+----+---------+--------------------+------------------+
| 2  | fallout | fallout@iuantu.com | 2021-01-01 23:00 |
+----+---------+--------------------+------------------+
| 3  | cenxl   | cenxl@iuantu.com   | 2021-01-01 23:00 |
+----+---------+--------------------+------------------+

contact_contact
+----+------------+-----------+------------------+
| id | contact_id | friend_id | created_at       |
+----+------------+-----------+------------------+
| 1  | 1          | 2         | 2021-01-01 23:00 |
+----+------------+-----------+------------------+
| 2  | 2          | 1         | 2021-01-01 23:00 |
+----+------------+-----------+------------------+
```

## 特性

DICore 运行在 dotnet 环境下，使用 EFCore 实现数据库访问查询，使用 DynamicLinq 构造查询。

- 为数据表提供GraphQL 查询

## 路线

- 认证支持
- RBAC 支持

## 安装

## 使用

配置数据库连接

```
$ ./dicore
Listening on 5000
```

## 协议

Copyright 2021 IUANTU

Licensed under the MIT: https://opensource.org/licenses/MIT
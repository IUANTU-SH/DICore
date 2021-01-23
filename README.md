DICore
=======

DICore 是一个快速的接口生成工具，为数据表直接生成 GraphQL 查询。DICore 运行在 dotnet 环境下，使用 EFCore 实现数据库访问查询。

``` graphql
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

```
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

## 特性

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
# 数据模型设计

所有结构变更将通过 flyway 管理

### 1. 用户模块

#### 用户信息表

| 字段名称          | 属性           | 约束       | 默认值                                           | 描述                    |
|---------------|--------------|----------|-----------------------------------------------|-----------------------|
| id            | int          | not null | AUTO_INCREMENT                                | 主键                    |
| username      | varchar(50)  | not null |                                               | 用户名                   |
| nickname      | varchar(200) | not null |                                               | 用户昵称                  |
| password      | varchar(200) | not null |                                               | 密码密文                  |
| phone_number  | varchar(20)  |          |                                               | 手机号码                  |
| user_type     | varchar(20)  | not null |                                               | 用户类型(PRIVATE,COMPANY) |
| status        | varchar(20)  | not null | ACTIVE                                        | 用户状态(ACTIVE,DISABLED) |
| creation_time | timestamp    | not null | CURRENT_TIMESTAMP                             | 创建时间                  |
| update_time   | timestamp    | not null | CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP | 修改时间                  |

索引：username,user_type,creation_time

#### 企业信息表

#### 用户企业关联表

#### 管理员信息表
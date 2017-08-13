截止到目前，机器人已上线 4 个管理功能，如下表所示：

| 功能代号 | 功能名 | 所需权限 | 是否默认开启 |
| :---: | :---: | :---: | :--- |
| nospam | 反群发广告、垃圾信息、身份伪装等 | （可选自动移除）Ban Users, Delete Message | 是 |
| noblue | 自动删除蓝色机器人命令防止误触 | Delete Message | 是 |
| dynlink | 动态生成临时加群链接 | Invite Users with Link\(Add Users\) | 否 |
| ingroupvalidation | 加群防外星人附加验证（选择题） | Ban Users | 否 |

以上管理功能均可由群组创始人或创始人指定管理员决定开启或关闭：

开启：`/enable 功能代号`

关闭：`/disable 功能代号`

**由于管理功能状态与索引条目共同存放，管理功能的偏好设置仅对已索引群组有效。**

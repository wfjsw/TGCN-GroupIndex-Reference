**使用下列功能前，请先阅读 [隐私政策](/privacy_policy.md) 并将机器人设置为群组管理员**

截止到目前，机器人已上线 6 个管理功能，如下表所示：

| 功能代号 | 功能名 | 所需权限 | 是否默认开启 |
| :---: | :---: | :---: | :---: |
| noblue | 自动删除蓝色机器人命令防止误触(5秒后) | Delete Message | 是 |
| dynlink | 动态生成临时加群链接 | Invite Users with Link\(Add Users\) | 否 |
| antibot | 自动移除群员加的机器人（群主和管理员不受限制） | Ban Users | 否 |
| deljoin | 自动删除加群/退群消息 | Delete Message | 否 |
| antihalal | [防清真组件](/plugin_antihalal.md) 总开关 | Ban Users, Delete Message | 否 |
| antihalal.name| 防清真增强（检测显示名） | Ban Users, Delete Message | 否 |
| antihalal.sticker | 防清真增强（检测贴纸包名）| Ban Users, Delete Message | 否 |
| antihalal.nodb | 忽略数据库清真标记 | / | 否 |

以上管理功能均可由群组创始人或创始人指定管理员决定开启或关闭：

在**群组内**使用如下指令：

开启：`/enable@zh_groups_bot 功能代号`

关闭：`/disable@zh_groups_bot 功能代号`

**管理功能的偏好设置将对所有群组长期保存，不受索引条目影响。**


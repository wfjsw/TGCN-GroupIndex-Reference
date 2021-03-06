## 权限说明

1. 最佳运行权限：
  - Ban Users （封禁用户）
  - Delete Messages （删除消息）
2. 消息访问权限：
  - 此插件将会存储所有对清真判定规则呈阳性的消息，无论此插件是否开启。
  - 所有存储的消息将在机器人管理员之间共享
  
## 清真判定规则

1. 清真字符定义
  1. 阿拉伯语字符
  2. 波斯语字符
  3. 天城文字符
2. 阈值限制
  1. 符合以下条件的字符串或贴纸包标题将被认为清真
    1. 包含多于 12 个清真字符
    2. 除去空格后，清真字符占全部字符的 45%
  2. 包含以下关键字的字符串将被认为清真（增强判定）
    - `sharma` （来源：`android Discuss`、`91yun`）
    - `amarhs`
    - `pollsciemo` （[来源](https://t.me/geekschannel/844)）
    - `moham`
    - `ali.*reza`
    - `ahmed`
3. 数据捕获时机
  1. 新成员加群时，
     1. 判断是否在已知的清真列表
       - 如果符合并启用清真保护(`antihalal`)则对该群组封禁并给提示
       - 如果启用了 `antihalal.nodb` 则忽略此条
     2. 判断新成员显示名
       - 如果符合清真及增强判定条件则上报事件。
           - 如果启用清真增强保护(`antihalal.name`)则对该群组封禁并给提示
  2. 对每条消息
     1. 判断是否在已知的清真列表
       - 如果符合并启用清真保护(`antihalal`)则对该群组封禁并给提示
       - 如果启用了 `antihalal.nodb` 则忽略此条
     2. 如果符合清真条件则上报事件。
       - 如果启用清真保护(`antihalal`)则对该群组封禁并给提示
     3. 贴纸
       - 在启用了 `antihalal.sticker` 的情况下，检验贴纸包名称是否包含清真字符
4. 自动清场
  - 消息清真并启用了清真保护(`antihalal`)将会自动尝试删除所有清真的消息
5. 事后处理
  1. 对于每一条上报的信息，一组老阿訇将判断它们是否清真
    - 若清真，用户将永久被标记为已知清真
    - 若不清真，用户将永久被标记为不清真，**此后将永不再受此插件影响**。
  2. 对于没有被标记为已知清真、而错误触发自动判定的用户，群组管理员可以覆盖判定结果，并使其在本群不再受判定影响
    - 已知清真标记将覆盖此判断
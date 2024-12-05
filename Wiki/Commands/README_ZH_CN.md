### [<<<](../README_ZH_CN.md) Wiki

# 命令

### 目录
- [命令表](#命令表)
- [命令参数详情](#命令参数详情)

命令参数 `<>` 是必填项； `[]` 是选填项，且默认值会显示为 `[数值=默认值]`。

## 命令表
| 命令 | 例子 | 描述 | 仅管理员 | 聊天 | RCON |
|------|------|------|----------|------|------|
| `/reloadcfg` | `/reloadcfg` | 重新加载 PalGuard 配置文件。 | X | X | X |
| `/kick <玩家名称>` | `/kick Cheater007` | 根据玩家名称将其踢出服务器。 | X | X | X |
| `/kickid <steamID>` | `/kickid 76567890987654321` | 根据玩家的 Steam ID 将其踢出服务器。 | X | X | X |
| `/ban <玩家名称>` | `/ban Cheater007` | 根据玩家名称将其加入服务器黑名单。 | X | X | X |
| `/banid <steamID>` | `/banid 76567890987654321` | 根据 Steam ID 将玩家加入服务器黑名单。 | X | X | X |
| `/ipban <玩家名称>` | `/ipban Cheater007` | 根据玩家名称将该玩家的 IP 地址加入服务器黑名单。 | X | X | X |
| `/ipbanid <steamID>` | `/ipbanid 76567890987654321` | 根据 Steam ID 将该 Steam ID 的 IP 地址加入服务器黑名单。 | X | X | X |
| `/ipban_ip <IP>` | `/ipban_ip 127.0.0.1` | 将指定 IP 地址加入服务器黑名单。 | X | X | X |
| `/unban_ip <IP>` | `/unban_ip 127.0.0.1` | 将指定 IP 地址移出服务器黑名单。 | X | X | X |
| `/addadminip <IP>` | `/addadminip 127.0.0.1` | 将指定 IP 地址添加到管理员白名单。 | X | X | X |
| `/setadmin <steamID>` | `/setadmin 76567890987654321` | 临时授予/撤销玩家管理员权限。 | X | X | X |
| `/getip <steamID>` | `/getip 76567890987654321` | 获取玩家的 IP 地址。（玩家必须在线） | X | X | X |
| `/give <steamID> <物品ID> [数量=1]` | `/give 76567890987654321 LuxuryMedicines 42` | 给玩家一个物品，并可指定数量。 | X | X | X |
| `/giveitems <steamID> <物品ID>[:<数量>] ...` | `/giveitems 76567890987654321 LuxuryMedicines:42 Money:666 AssaultRifle_Default5` | 一次给玩家多个物品，并可以指定每个物品的数量，使用冒号分隔。 | X | X | X |
| `/giveme <物品ID> [数量=1]` | `/giveme Lotus_hp_02 999` | 给自己一个物品，并可指定数量。 | X | X | |
| `/delitem <steamID> <物品ID> [数量=1]` | `/delitem 76567890987654321 LuxuryMedicines all` | 从玩家身上删除物品，并可指定数量，默认删除一个物品。如果使用 `all`，将删除所有该物品。 | X | X | X |
| `/delitems <steamID> <物品ID>[:<数量>] ...` | `/delitems 76567890987654321 LuxuryMedicines Milk:all Money:5000` | 一次删除多个物品，并可指定每个物品的数量。使用 `all` 替代 `1` 删除所有该物品。 | X | X | X |
| `/give_exp <steamID> <数量>` | `/give_exp 76567890987654321 400000` | 给玩家指定数量的经验值。 | X | X | X |
| `/giveme_exp <数量>` | `/giveme_exp 400000` | 给自己指定数量的经验值。 | X | X | X |
| `/whitelist_add <steamID>` | `/whitelist_add 76567890987654321` | 将 Steam ID 添加到白名单中。 | X | X | X |
| `/whitelist_remove <steamID>` | `/whitelist_remove 76567890987654321` | 从白名单中移除 Steam ID。 | X | X | X |
| `/whitelist_get` | `/whitelist_get` | 获取所有已添加到白名单中的玩家列表。 | X | X | X |
| `/givepal <steamID> <PalId> <Level>` | `/givepal 76567890987654321 FengyunDeeper 55` | 给玩家一个帕鲁（如果玩家携带的帕鲁已满，将进入帕鲁终端）。 | X | X | X |
| [/givepal_j](givepal_j_ZH_CN.md) | `/givepal_j <steamID> <PalJSON>` | 给玩家一个帕鲁，具有提供的 JSON 属性。（如果玩家携带的帕鲁已满，将进入帕鲁终端）。有关更多信息，请详见 [PalJSON](../Files/PalJSON_ZH_CN#json-file-template)。 | X | X | X |
| `/exportpals <steamID>` | `/exportpals 76567890987654321` | 导出玩家的所有帕鲁到 `Pal/Binaries/Win64/palguard/pals/` 文件夹。有关更多信息，请详见 [PalJSON](../Files/PalJSON_ZH_CN#json-file-template)。 | X | X | X |
| `/jetragon` | `/jetragon` | 给你一个管理员级别的空涡龙（它超快...）。 | X | X | |
| `/catwaifu` | `/catwaifu` | 给你一个管理员级别的暗巫猫，增加你的角色属性。 | X | X | |
| `/giveegg <steamID> <EggID>` | `/giveegg 76567890987654321 PalEgg_Electricity_03` | 给玩家一个蛋，其中包含一个完全随机的帕鲁。蛋的类型只影响孵化时间，而不会影响其中的帕鲁。 | X | X | X |
| `/goto <X> <Y> <Z>` | `/goto 133.7 666 42` | 传送到指定位置。 | X | X | |
| `/pgbroadcast <Text>` | `/pgbroadcast Hello, Palworld!` | 向服务器中的所有玩家发送消息，消息可以包含空格。 | X | X | X |
| `/iwantplayerlist` | `/iwantplayerlist` | 打开 `服务器内可以查看其他玩家列表` ，直到下次服务器重启。 | X | X | X |
| `/getrconcmds` | `/getrconcmds` | 返回一个命令列表，列出所有可通过 RCON 使用的命令及其所需参数数量。例如：`getrconcmds:1;giveegg:2;give:2;` | X | | X |
| `/getnearestbase [X] [Y] [Z]` | `/getnearestbase 133.7 666 42` | 告诉你最近的基地所属的公会名称。**如果是 RCON 使用，则必须提供坐标。** | X | X | X |
| `/gotonearestbase [X] [Y] [Z]` | `/gotonearestbase 133.7 666 42`<br>`/gotonearestbase` | 传送到最近的基地。 | X | X | |
| `/killnearestbase [X] [Y] [Z]` | `/killnearestbase 133.7 666 42`<br>`/killnearestbase` | 销毁最近的基地。（使用时请小心）。**如果是 RCON 使用，则必须提供坐标。** | X | X | X |
| `/adminlogout` | `/adminlogout` | 退出管理员模式。 | X | X | X |
| `/toggleserverpvp` | `/toggleserverpvp` | 打开或者关闭 `服务器内PVP` 和 `玩家对玩家的伤害` ，直到下次服务器重启。 | X | X | X |
| `/give_relic <steamID> <数量>` | `/give_relic 76567890987654321 666` | 给玩家一个或多个翠叶鼠雕像。 | X | X | X |
| `/setguildleader <steamID>` | `/setguildleader 76567890987654321` | 让目标玩家成为他当前公会的会长。 | X | X | X |
| `/imcheater` | `/imcheater` | 将你标记为作弊者并采取措施（用于测试反作弊）。 | X | X | X |

<br>

## 命令参数详情
| 参数 | 描述 |
|------|------|
| 数量<br>等级 | 自然数（正整数）。 |
| X, Y, Z | 游戏世界中的坐标。 |
| [steamID](https://steamid.io) | Steam ID 是用来唯一标识 Steam 账户的标识符。Steam ID 可以转换为更新后的 steamID3 或 steamID64，也就是社区 ID 或好友 ID。通过该 steamID64，可以找到用户的 Steam 社区页面。 |
| 玩家名称 | 玩家可以在游戏过程中选择和修改的最多 24 个字符的名称。 |
| [IP](https://en.wikipedia.org/wiki/IP_address) | IP 地址（Internet Protocol 地址）是分配给连接到计算机网络（使用互联网协议进行通信）设备的数字标签，例如 192.0.2.1。IP 地址主要用于两种功能：网络接口识别和位置定位。 |
| [物品ID](https://pwmodding.wiki/docs/game-data/item-table) | 用于标识物品的唯一名称。 |
| [PalID](https://pwmodding.wiki/docs/game-data/monster-table) | 用于标识帕鲁的唯一名称。 |
| [EggID](https://pwmodding.wiki/docs/game-data/item-table) | 仅适用于蛋的物品 ID：<br>`PalEgg_Dark_01（暗黑帕鲁蛋）` 到 `PalEgg_Dark_05（巨大暗黑帕鲁蛋）`、`PalEgg_Dragon_01（龙蛋）` 到 `PalEgg_Dragon_05（巨大龙蛋）`、<br>`PalEgg_Earth_01（粗糙帕鲁蛋）` 到 `PalEgg_Earth_05（巨大粗糙帕鲁蛋）`、`PalEgg_Electricity_01（电气帕鲁蛋）` 到 `PalEgg_Electricity_05（巨大电气帕鲁蛋）`、<br>`PalEgg_Fire_01（发热帕鲁蛋）` 到 `PalEgg_Fire_05（巨大发热帕鲁蛋）`、`PalEgg_Ice_01（结冰帕鲁蛋）` 到 `PalEgg_Ice_05（巨大结冰帕鲁蛋）`、<br>`PalEgg_Leaf_01（新绿帕鲁蛋）` 到 `PalEgg_Leaf_05（巨大新绿帕鲁蛋）`、`PalEgg_Normal_01（平凡帕鲁蛋）` 到 `PalEgg_Normal_05（巨大平凡帕鲁蛋）`、<br>`PalEgg_Water_01（潮湿帕鲁蛋）` 到 `PalEgg_Water_05（巨大潮湿帕鲁蛋）`。 |
| [PalJSON](../Files/PalJSON_ZH_CN#json-file-template) | 包含帕鲁属性的 JSON 文本或文件。模板和更多内容请详见 [PalJSON](../Files/PalJSON_ZH_CN#template)。 |

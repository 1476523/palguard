### [<<<](../README.md) Wiki

#### English / [简体中文](./README_ZH_CN.md)

# Commands

### Table of Contents
- [Command Table](#command-table)
- [Command Argument Details](#command-argument-details)

Commands arguments that are wrapped by `<>` are required to perform it, arguments wrapped by `[]` are optional and have a default value shown as `[argname=DefaultValue]`.

## Command Table
|Command|Usage|Description|Admin Only|Chat|RCON|
|-------|-------|-----------|----------|----|----|
|`/reloadcfg`|`/reloadcfg`|Reloads the palguard config file.|X|X|X|
|`/kick <PlayerName>`|`/kick Cheater007`|Kicks a player by name from the server.|X|X|X|
|`/kickid <steamID>`|`/kickid 76567890987654321`|Kicks a player by steamID from the server.|X|X|X|
|`/ban <PlayerName>`|`/ban Cheater007`|Bans a player by name from the server.|X|X|X|
|`/banid <steamID>`|`/banid 76567890987654321`|Bans a player by steamID from the server.|X|X|X|
|`/ipban <PlayerName>`|`/ipban Cheater007`|IP Bans a player by name from the server.|X|X|X|
|`/ipbanid <steamID>`|`/ipbanid 76567890987654321`|IP Bans a player by steamID from the server.|X|X|X|
|`/ipban_ip <IP>`|`/ipban_ip 127.0.0.1`|Ban IP address from joining the server.|X|X|X|
|`/unban_ip <IP>`|`/unban_ip 127.0.0.1`|Reverts an IP address Ban.|X|X|X|
|`/addadminip <IP>`|`/addadminip 127.0.0.1`|Adds IP address to admin whitelist.|X|X|X|
|`/setadmin <steamID>`|`/setadmin 76567890987654321`|Temporarily grants/revokes admin from a player.|X|X|X|
|`/getip <steamID>`|`/getip 76567890987654321`|Gives you a player's IP address. (Must be online)|X|X|X|
|`/give <steamID> <ItemID> [Amount=1]`|`/give 76567890987654321 LuxuryMedicines 42`|Gives a player an item and if specified how many.|X|X|X|
|`/giveitems <steamID> <ItemID>[:<Amount>] ...`|`/giveitems 76567890987654321 LuxuryMedicines:42 Money:666 AssaultRifle_Default5`|Gives a player more than 1 item in one command and if specified how many of each seperated by a colon.|X|X|X|
|`/giveme <ItemID> [Amount=1]`|`/giveme Lotus_hp_02 999`|Gives you an item and if specified how many.|X|X||
|`/delitem <steamID> <ItemID> [Amount=1]`|`/delitem 76567890987654321 LuxuryMedicines all`|Deletes an item from a player and if specified how many. Default is `1` which will delete only 1 occurence of that item. Use `all` instead of `1` to delete all occurences.|X|X|X|
 |`/delitems <steamID> <ItemID>[:<Amount>] ...`|`/delitems 76567890987654321 LuxuryMedicines Milk:all Money:5000`|Deletes more than 1 item from a player in one command and if specified how many of each seperated by a colon. Use `all` instead of `1` to delete all occurences.|X|X|X|
|`/give_exp <steamID> <Amount>`|`/give_exp 76567890987654321 400000`|Gives a player the specified amount of EXP.|X|X|X|
|`/giveme_exp <Amount>`|`/giveme_exp 400000`|Gives yourself the specified amount of EXP.|X|X|X|
|`/whitelist_add <steamID>`|`/whitelist_add 76567890987654321`|Adds a steamID to the whitelist.|X|X|X|
|`/whitelist_remove <steamID>`|`/whitelist_remove 76567890987654321`|Removes a steamID from the whitelist.|X|X|X|
|`/whitelist_get`|`/whitelist_get`|Gets full list of whitelisted players.|X|X|X|
|`/givepal <steamID> <PalId> <Level>`|`/givepal 76567890987654321 FengyunDeeper 55`|Gives the player a Pal (if their party is full, it will go into their Pal storage).|X|X|X|
|[/givepal_j](givepal_j.md)|`/givepal_j <steamID> <PalJSON>`|Gives the player a Pal with the provided attributes in the json. (if their party is full, it will go into their Pal storage). See [PalJSON](../Files/PalJSON.md#json-file-template) for a deeper understanding.|X|X|X|
|[/deletepals](deletepals.md)|`/deletepals <steamID> <PalFilter>`|Deletes multiple pals from a player's palteam and palbox based on a filter, which can be configured through command arguments.|X|X|X|
|`/exportpals <steamID>`|`/exportpals 76567890987654321`|Export every Pal of a player to a json file at `Pal/Binaries/Win64/palguard/pals/`. See [PalJSON](../Files/PalJSON.md#json-file-template) for a deeper understanding.|X|X|X|
|`/jetragon`|`/jetragon`|Gives you an Admin-Jetragon Pal (it's faaas.... gone).|X|X||
|`/catwaifu`|`/catwaifu`|Gives you an Admin-Cat-Waifu that buffs your character stats.|X|X||
|`/giveegg <steamID> <EggID>`|`/giveegg 76567890987654321 PalEgg_Electricity_03`|Gives the player an egg **with a completely random Pal** inside. Egg type only affects the hatch time, but not the Pal inside.|X|X|X|
|`/goto <X> <Y> <Z>`|`/goto 133.7 666 42`|Teleports you to the provided location.|X|X||
|`/pgbroadcast <Text>`|`/pgbroadcast Hello, Palworld!`|Send message to all player in the server that can contain spaces.|X|X|X|
|`/iwantplayerlist`|`/iwantplayerlist`|Sets the `PalWorldSettings.bShowPlayerList` to `True` until the next server restart.|X|X|X|
|`/getrconcmds`|`/getrconcmds`|Returns a list of every command with the required arg count which is usable by RCON. Example: `getrconcmds:1;giveegg:2;give:2;`|X| |X|
|`/getnearestbase [X=Player.X] [Y=Player.Y] [Z=Player.Z]`|`/getnearestbase 133.7 666 42`|Tells you guild name which owns base nearest to your character. **If used by RCON, then all 3 arguments are required.**|X|X|X|
|`/gotonearestbase [X=Player.X] [Y=Player.Y] [Z=Player.Z]`|`/gotonearestbase 133.7 666 42`<br>`/gotonearestbase`|Teleports you to the nearest base.|X|X| |
|`/killnearestbase [X=Player.X] [Y=Player.Y] [Z=Player.Z]`|`/killnearestbase 133.7 666 42`<br>`/killnearestbase`|Destroys nearest base. (Use with caution). **If used by RCON, then all 3 arguments are required.**|X|X|X|
|`/adminlogout`|`/adminlogout`|Logs you out of admin mode.|X|X|X|
|`/toggleserverpvp`|`/toggleserverpvp`|Toggles the `PalWorldSettings.bIsPvP` and `PalWorldSettings.bEnablePlayerToPlayerDamage` between `True` and `False` until the next server restart.|X|X|X|
|`/give_relic <steamID> <Amount>`|`/give_relic 76567890987654321 666`|Gives the player one or more Lifmunk Effigies.|X|X|X|
|`/setguildleader <steamID>`|`/setguildleader 76567890987654321`|Makes target player the guild leader of the guild he currently belongs to.|X|X|X|
|`/imcheater`|`/imcheater`|Use this to test how your server response to a cheater.|X|X|X|

<br>

## Command Argument Details
|Argument| |
|--------|-|
|Amount<br>Level|A natural number (positive integer).|
|X, Y, Z|Floating numbers for a position in the GameWorld.|
|[steamID](https://steamid.io)|A steamID is a unique identifier used to identify a Steam account. A steamID can be converted to the newer steamID3 and to a steamID64, sometimes referred to as community ID or friendID. With this steamID64, a user's Steam community page can be found.|
|PlayerName|A 24 letter limited name a player can choose and change during gameplay.|
|[IP](https://en.wikipedia.org/wiki/IP_address)|An Internet Protocol address (IP address) is a numerical label such as 192.0.2.1 that is assigned to a device connected to a computer network that uses the Internet Protocol for communication. IP addresses serve two main functions: network interface identification, and location addressing.|
|[ItemID](https://pwmodding.wiki/docs/game-data/item-table)|A unique Name to identify the item you are looking for.|
|[PalID](https://pwmodding.wiki/docs/game-data/monster-table)|A unique Name to identify the Pal you are looking for.|
|[EggID](https://pwmodding.wiki/docs/game-data/item-table)|An ItemID that is limited to the eggs:<br>`PalEgg_Dark_01`-`PalEgg_Dark_05`, `PalEgg_Dragon_01`-`PalEgg_Dragon_05`,<br>`PalEgg_Earth_01`-`PalEgg_Earth_05`, `PalEgg_Electricity_01`-`PalEgg_Electricity_05`,<br>`PalEgg_Fire_01`-`PalEgg_Fire_05`, `PalEgg_Ice_01`-`PalEgg_Ice_05`,<br>`PalEgg_Leaf_01`-`PalEgg_Leaf_05`, `PalEgg_Normal_01`-`PalEgg_Normal_05`,<br>`PalEgg_Water_01`-`PalEgg_Water_05`|
|[PalJSON](../Files/PalJSON.md#json-file-template)|A json text or filename containing json that provided Pal attributes. Template and more can be found [here](../Files/PalJSON.md#template).|

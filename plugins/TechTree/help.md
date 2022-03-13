# 技術要求:

## 要求清單

| Config Key                                                   | 描述                           |
| ------------------------------------------------------------ | ------------------------------ |
| [entry](https://github.com/ASangarin/TechTree/wiki/Entry-Requirement) | 要求玩家解鎖另一個條目         |
| [items](https://github.com/ASangarin/TechTree/wiki/Item-Requirement) | 要求玩家擁有一定數量的原版物品 |
| [level](https://github.com/ASangarin/TechTree/wiki/Level-Requirement) | 要求玩家具有特定的經驗等級     |
| [exp](https://github.com/ASangarin/TechTree/wiki/Exp-Requirement) | 要求玩家擁有特定數量的經驗值   |



### entry

| Line Config Arg  | 描述                                     |
| ---------------- | ---------------------------------------- |
| `entry` (String) | 被引用條目的 ID                          |
| `tree` (String)  | 引用條目的樹（默認值：The Current Tree） |

例子

`\- 'entry{entry="example-entry",tree="other-tree"}'`

### items

| Line Config Arg.   | 描述                                                   |
| ------------------ | ------------------------------------------------------ |
| `type` (String)    | 所需的香草材料 （不區分大小寫）                        |
| `amount` (Integer) | The required amount of items. (Default = 1)            |
| `display` (String) | Replaces the {display} placeholder in the lore format. |
| `take` (Boolean)   | 解鎖時是否Get所需金額 (Default = true)                 |

例子

`\- 'items{type="DIAMOND",amount=5,display="Diamonds"}'`

### level

| Line Config Arg.   | 描述                                                         |
| ------------------ | ------------------------------------------------------------ |
| `levels` (Integer) | The required levels.                                         |
| `take` (Boolean)   | Whether or not the take the required amount when unlocked. (Default = true) |

例子

`\- 'level{levels=13,take=true}'`

### exp

| Line Config Arg.   | 描述                                   |
| ------------------ | -------------------------------------- |
| `levels` (Integer) | 所需的經驗值 （這是香草經驗值）        |
| `take` (Boolean)   | 解鎖時是否取到所需金額(Default = true) |

例子

`\- 'exp{exp=135,take=true}'`

## 外部插件獎勵列表

### Vault

| Line Config Arg.  | 描述                                                         |
| ----------------- | ------------------------------------------------------------ |
| `amount` (Double) | The required amount.                                         |
| `take` (Boolean)  | Whether or not to withdraw the required amount from players balance (Default = true) |

`\- 'money{amount=5.25,take=true}'`

# 獎勵清單

## 命令

| Line Config Arg.    | 描述                                 |
| ------------------- | ------------------------------------ |
| `format` (String)   | 要運行的命令                         |
| `console` (Boolean) | 是否從控制台運行命令(Default: false) |

可用於輸入玩家姓名 {player}

例子

`\- 'command{format="/say Test Command!",console=true}'`
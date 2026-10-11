# LenoGame —— 用 Leno 语言写的游戏合集

八个用 [LenoLang](https://gitee.com/cheng8214/LenoLang) 写的 GUI 游戏 / 动画，全部基于
`LenoSDL3` 框架（窗口、控件、Canvas 自绘）。

| 目录 | 入口文件 |
|---|---|
| `五子棋/` | `gomoku.leno` |
| `俄罗斯方块/` | `tetris.leno` |
| `塔防/` | `tower_defense.leno` |
| `扫雷/` | `minesweeper.leno` |
| `植物大战僵尸/` | `pvz.leno`（另有地图 / 动画编辑器 `anim_editor.leno`） |
| `飞机大战/` | `plane_war.leno` |
| `超级玛丽/` | `super_mario.leno`（`sm_types.leno` 为数据结构） |
| `鹈鹕动画/` | `pelican.leno` |

## 怎么跑

需要 Leno 编译器 + 标准模块（`leno_module/` 与 `leno.exe` 同目录）：

```
<Leno 目录>\leno.exe 五子棋\gomoku.leno
```

只做编译检查（不运行）：

```
<Leno 目录>\leno.exe -c 五子棋\gomoku.leno
```

## 依赖

- **编译器 / 虚拟机 / 标准模块**：LenoLang 发行版（本仓**不含**，见上方链接）
- **音频**：`LenoMusic` 模块（标准模块之一；塔防、植物大战僵尸等用到）
- **字体**：各游戏 `font/` 下的开源字体（随仓携带）

## 目录约定

- 每个游戏一个子目录，内含入口 `.leno` 与各自的资源（`png` / `ogg` / `mp3` / `font` / 关卡文本）
- 构建产物（`.lenocache/`、`*.lenomc`、`*.lenosymc`、`*.lenb`、`dist/`）**不入库**，已在
  `.gitignore` 里排除

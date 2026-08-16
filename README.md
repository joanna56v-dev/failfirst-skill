# FailFirst

**大多数 AI 帮你想得更周全，FailFirst 帮你真正开始。**

FailFirst 是一个面向“有想法，却迟迟没有开始”的人的 Agent Skill。

用户只需要说一句：

> 我想一个人去旅行。

> 我想换城市生活。

> 我想开始找工作。

FailFirst 会通过：

`5轮动态情境探索 -> 3轮个性化失败模拟 -> 重新理解真正的行动阻碍 -> 生成一个现实中的 First Move`

我们模拟失败，不是为了避免失败，而是为了让你发现：

> 即使失败，我也还有下一步。

## 它有什么不同

| 工具类型 | 核心问题 | 输出 |
|---|---|---|
| Planning AI | 我该怎么做？ | 计划 |
| Decision AI | 我应该选哪个？ | 建议 |
| Pre-mortem | 这件事会怎么失败？ | 风险规避 |
| **FailFirst** | **我为什么还没开始？** | **一个真实 First Move** |

FailFirst 不做心理诊断，不替用户做重大决定，也不会把失败模拟变成一份更长的准备清单。

## 安装

下载或克隆这个仓库，把 [SKILL.md](SKILL.md) 放到你的 Agent Skills 目录，并确保它位于 `failfirst` 文件夹根目录。

Codex 用户可以放到：

```text
~/.agents/skills/failfirst/
```

在仓库根目录执行：

```bash
mkdir -p ~/.agents/skills/failfirst
cp SKILL.md ~/.agents/skills/failfirst/SKILL.md
```

最终路径应为 `~/.agents/skills/failfirst/SKILL.md`，不要再嵌套一层仓库目录。

然后重启 Codex，或等待 Codex 自动检测 Skill 变化。

## 使用

在 Codex 中显式调用：

```text
$failfirst 我想开始找工作，但一直觉得自己还没准备好。
```

## Try it

```text
使用 FailFirst：

我想开始找工作，但一直觉得自己还没准备好。
```

```text
使用 FailFirst：

我想一个人去旅行，但一直没有真正订票。
```

```text
使用 FailFirst：

我想换个城市生活，但已经想了半年。
```

## 工作方式

FailFirst 不会一次抛出一套问卷。它每次只问一个具体情境问题，并根据用户上一轮的回答动态生成下一问。

完整逻辑见 [SKILL.md](SKILL.md)，动态对话片段见 [examples/examples.md](examples/examples.md)。

## License

[MIT](LICENSE)

# 内容创作者第二大脑 · Second Brain for Content Creators

**把你每天写的东西，自动沉淀成可复用的内容资产。**

一个跑在 Claude Code 上的技能包，适合日更写作者、内容创作者、独立创业者。

---

## 你的问题

你每天都在写。写出来不少好东西。然后它消失了。

三个月后你卡住了，你忘了自己三个月前已经解决过这个问题。最好的金句埋在旧文件里，故事和主题没有连起来，什么都没有复利。

## 它做什么

每次你发来一篇日记或文章，Claude 会：

- 用**最小改动**整理文章（你的语气原样保留）
- 提取出**故事、洞见、可执行动作、标志性表达**
- 存进 **4 个内容资产库**，随时可以调用
- 生成一张**可下载的洞见卡片**（HTML格式）
- 给你**教练反馈**——做得好的，值得留意的

积累下去，你会建出一个专属的原材料库，以后写东西直接从里面取。

## 工作流程

```
你写了一篇东西
      ↓
Claude 整理（先发你审核）
      ↓
提取资产 → 故事库 / 洞见库 / 动作库 / 风格表达库
      ↓
生成洞见卡片（HTML，可下载）
      ↓
教练反馈
```

---

## 安装

```bash
# 全局安装（所有 Claude Code 会话都可用）
mkdir -p ~/.claude/skills/second-brain
curl -o ~/.claude/skills/second-brain/SKILL.md \
  https://raw.githubusercontent.com/lhsyt/second-brain-skill/main/SKILL.md
```

安装后，把 `profile-template.md` 复制到你的工作目录，填写你的个人信息。

---

## 文件结构

```
你的项目/
├── profile-template.md         ← 填你的信息（写作 DNA）
├── 00-inbox/
│   └── insight-cards/          ← 生成的 HTML 洞见卡片
├── 03-resources/atoms/
│   ├── story-bank.md           ← 故事库
│   ├── insight-bank.md         ← 洞见库
│   ├── action-bank.md          ← 动作库
│   └── style-bank.md           ← 风格表达库
└── sources/                    ← 原始内容存档
```

---

## 触发词

| 你说 | Claude 执行 |
|------|------------|
| 「这是我的日记」/ 「今天的文章」 | 完整 6 步流程 |
| 「只要标题和文章」 | 只做整理，等你审核 |
| 「下一步」（审核后） | 执行资产提取+卡片+反馈 |
| 「按原文记录」 | 原文存档，直接提取资产 |
| 「分析一下」 | 只分析，不走流程 |

---

## 核心原则

> 最小改动。你的语气不变。系统负责整理。

Claude 不会重写你的文章。只修正语音识别错误，去除口头语重复，句式结构原样保留。让你的文章读起来像你的那些东西，一个字都不动。

---

## 使用要求

- [Claude Code](https://claude.ai/claude-code)（Claude 官方 CLI 工具）
- 工作目录里有填好的 `profile-template.md`

---

## License · 许可

MIT — 随意使用、fork、基于它做自己的版本。

---

*一个日更 400+ 天的创作者做的，因为自己需要它。*

---

## English Summary

A Claude Code skill that processes your daily writing and extracts reusable content assets (stories, insights, actions, signature phrases). Generates downloadable insight cards. Gives coach feedback. Minimal edits — your voice stays intact.

Install: `curl -o ~/.claude/skills/second-brain/SKILL.md https://raw.githubusercontent.com/lhsyt/second-brain-skill/main/SKILL.md`

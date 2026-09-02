# Paper Reader Skill

一个面向学术论文首次阅读的 Codex Skill。默认用中文快速建立论文的整体地图，重点是“先讲懂，再决定哪里值得深入”，而不是直接生成完整 review。

## 核心行为

首次阅读固定回答六个问题：

1. 题目为什么这样起？
2. 论文具体做了什么？
3. Introduction 的背景与 research gap 是什么？
4. 数据从哪里来？
5. 方法整体怎样运行？
6. 真正的贡献是什么？

默认首轮约 500–800 个中文字符，并保留必要的 English academic terms。

## 设计原则

- **Source First**：优先阅读用户提供或官方发布的论文全文。
- **Evidence Grounded**：严格区分论文明确表述与基于全文的归纳。
- **No Fabrication**：不编造数据规模、实验结果、模型设置、标注流程或发表信息。
- **Focused Follow-up**：后续只展开用户追问的部分，不重复完整六段。
- **First-pass, not Full Review**：首轮避免穷尽实验、ablation、limitations 和公式细节。

完整指令见 [SKILL.md](./SKILL.md)。

## 安装

将仓库克隆到 Codex skills 目录：

```bash
git clone https://github.com/Leoccino/paper-reader-skill.git ~/.codex/skills/paper-reader
```

重新打开 Codex 或开始一个新任务，使 Skill 被发现。

## 使用示例

安装后可以直接提供论文 PDF、URL、arXiv、DOI 或标题，例如：

```text
帮我读一下这篇论文。
```

```text
这篇论文的方法是什么？
```

```text
这个 research gap 到底成立吗？
```

若只提出一个具体问题，Skill 会直接回答该部分，而不会重新输出六部分概览。

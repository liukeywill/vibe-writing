# Vibe Writing · 通用写作与表达编辑

把想法写成文章，从一句需求开始。输入体裁和主题，即可生成完整初稿，按用途安排结构与语气。已有文章也能改写、压缩、换风格，或只检查表达问题。

## 适合什么任务

| 你的任务 | 使用入口 | 默认方式 |
|---|---|---|
| 通用文章成稿、改写或表达审查 | [Vibe Writing](https://github.com/liukeywill/vibe-writing) | 内部编辑后直接交稿 |
| 从研究方向逐阶段协作，自己把关关键决定 | [Vibe Research](https://github.com/liukeywill/vibe-research) | 每阶段交付并等待人工核查 |
| 按确定主题连续推进到完整论文及材料包 | [Auto Paper](https://github.com/liukeywill/auto-paper) | 在实际条件允许范围内连续执行 |

本技能负责文章和表达，不管理科研问题、文献筛选、研究设计或实验。已有论文只做语言编辑时保留术语、引用、数字和限定；语言自然不代表研究结论已核验。完整科研任务按上表选择对应入口，不会仅因文章带有学术主题就自动启动论文流水线。

## 使用方式

在支持 Skill 的 AI 助手中加载本目录，然后输入：

```text
$vibe-writing 体裁：公众号文章；主题：AI时代，普通人如何提升写作能力；1000字左右，语言通俗自然。
```

```text
$vibe-writing 改写以下文章，清理套话和生硬表达，保留事实和作者立场：……
```

```text
$vibe-writing 只审查以下文章，指出表达问题和修改方向，不重写全文：……
```

支持报道、公众号、评论、日常文书、故事等多种题材和文体。信息不足时使用必要占位符；不编造数据、引语、经历或新闻事实。需要提交的正式材料，请核对姓名、日期、来源等具体信息。

## 安装到 Codex

```bash
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo liukeywill/vibe-writing \
  --path . \
  --name vibe-writing
```

## 与研究技能的关系

Vibe Writing 不依赖 Research Core，也不强制安装两个科研 Skill。研究流程可以在证据与结论确认后使用表达编辑，但不能靠润色补证据、改研究立场或删除局限。实际调用其他 Skill 取决于用户任务和运行环境，三个入口可以分别安装。

## 文件与开源来源

- `SKILL.md`：写作、改写、审查流程。
- `references/genres.md`：文体适配。
- `references/writing-prompts.md`：阶段提示词。
- `references/humanizer.md`：中文适配与调用规则。
- `references/humanizer-original.md`：blader/humanizer 原版快照。
- `third-party/blader-humanizer-LICENSE.txt`：上游 MIT 许可证与版权通知。

中文自然化编辑集成 [blader/humanizer](https://github.com/blader/humanizer)，固定提交 `225a6f39ac85f76ee48dbad772ea4abe4ed6c9d8`，原版元数据版本 `3.1.0`，Copyright (c) 2025 Siqi Chen。原版规则和 MIT 通知随目录保留；体裁加主题成稿、中文文体约束及交付方式属于 Vibe Writing 的整合与适配。

早期中文编辑模块参考 [ksufer/humanizer-zh-skill](https://github.com/ksufer/humanizer-zh-skill)，提交 `b6fd6105cdab487814bbe479735b897f3461573e`；当前实际执行依据为 blader/humanizer。第三方许可证适用于相应第三方内容，本次同步不另行指定新增内容的整体许可证。

“去AI味”指编辑语言和结构问题，不判断作者身份，也不承诺任何检测器分数。写作和改写不会自动发送、投稿或发布。

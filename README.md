# AI Newsletter Skill

一个用于生成中文 AI 日报的 Codex Skill。它会检查固定官方来源，整理 X、Hacker News 和 Reddit 的高价值讨论，并完整输出 GitHub Trending daily 页面中的仓库。

## 功能

- 按用户时区扫描过去 24 小时的信息。
- 检查 OpenAI、Anthropic、Google、Meta、DeepSeek、Kimi、Qwen 等固定官方来源。
- 收集 X、Hacker News 和 Reddit 的 AI 相关高价值话题。
- 在直接访问受限时继续使用公开索引、API 和原帖引用寻找可验证内容。
- 完整抓取 GitHub Trending daily 页面，保留所有仓库及原始顺序。
- 验证发布时间、标题、数据和原始链接。
- 以“开发者日报 + 研究者观察”的中文风格输出。

## 目录结构

```text
ai-newsletter-skill/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
└── references/
    ├── output-template.md
    └── sources-and-selection.md
```

## 安装

将仓库克隆到 Codex Skills 目录：

```powershell
git clone https://github.com/WeiLoading/ai-newsletter-skill.git `
  "$HOME\.codex\skills\ai-newsletter"
```

也可以下载仓库 ZIP，解压后将目录重命名为 `ai-newsletter`，放入：

```text
~/.codex/skills/
```

安装后的关键路径应为：

```text
~/.codex/skills/ai-newsletter/SKILL.md
```

重新启动 Codex 或新建对话，使 Skill 被重新发现。

## 使用

生成今天的完整日报：

```text
使用 $ai-newsletter 生成今天完整的日报
```

生成指定日期的日报：

```text
使用 $ai-newsletter 生成 2026年6月10日的完整日报
```

## 配置

- 在 `references/sources-and-selection.md` 中维护固定官方来源、关注方向和筛选规则。
- 在 `references/output-template.md` 中维护日报结构、数量要求和输出前检查项。
- 在 `SKILL.md` 中维护核心执行流程和不可违反的规则。
- 修改 `agents/openai.yaml` 可以调整 Codex 中显示的名称、简介和默认提示词。

更新来源或规则后，应确认：

1. `SKILL.md` 中引用的文件仍然存在。
2. “特别关注”只包含配置的官方来源。
3. X、Hacker News 和 Reddit 的原始链接要求没有被削弱。
4. GitHub Trending 仍要求完整抓取并保持原始顺序。
5. 输出模板中的 GitHub 仓库总数与实际条目数一致。

## 说明

日报质量取决于运行环境可用的网页搜索、浏览器和平台访问能力。Skill 要求在单一访问方式失败后继续尝试公开索引、API 或其他可验证来源，但不会为满足数量要求而编造内容。

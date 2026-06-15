# Output Template and Final Checks

## Required Layout

```markdown
# 🔥 AI Newsletter | YYYY年M月D日

> 检索窗口：用户时区 YYYY年M月D日 HH:mm 至 YYYY年M月D日 HH:mm
> GitHub Trending 数据来自 HH:mm 左右的 daily 页面实时快照。

## 一、📡 特别关注

### 1. 官方内容标题

**摘要：**  
说明官方发布或更新了什么。

**为什么值得关注：**  
说明产品、研究、开发者或行业影响。

**链接：**  
官方原文链接

## 二、💬 X 今日讨论话题

### 1. 话题标题

**讨论内容：**  
概括原帖及其讨论重点。

**为什么值得关注：**  
提炼能力变化、产品问题、需求或趋势。

**原帖链接：**  
X 原帖链接

## 三、📊 Hacker News 今日讨论话题

### 1. 话题标题

**讨论内容：**  
概括外部内容及 HN 社区的主要观点或争议。

**为什么值得关注：**  
说明开发者、架构、产品或行业价值。

**原帖链接：**  
HN item 链接

## 四、📌 Reddit 今日讨论话题

### 1. 话题标题

**讨论内容：**  
概括帖子及评论区的重要反馈。

**为什么值得关注：**  
说明用户痛点、实践经验、技术变化或潜在需求。

**原帖链接：**  
Reddit 原帖链接

## 五、⭐ GitHub Trending 今日推荐 repo

> 以下为抓取时 GitHub Trending daily 页面中的全部 N 个 repo，保持页面原始顺序，未进行筛选。

### 1. owner/repo

**当前 stars：**  
抓取时显示的 stars

**摘要：**  
说明项目是什么。

**为什么值得关注：**  
说明开发者需求、技术趋势或工具变化。非 AI 项目可以写明依据完整抓取规则保留。

**原 repo 链接：**  
GitHub 原 repo 链接
```

If there is no verified official update, replace all Special Attention entries with:

`今天特别关注模块没有检索到新的内容。`

## Count Rules

- Special Attention: unlimited; include every qualifying official update.
- X: at least seven high-quality items when available; no maximum.
- Hacker News: at least seven high-quality items when available; no maximum.
- Reddit: at least seven high-quality items when available; no maximum.
- GitHub Trending: every repository shown on the current daily page.

## Final Checklist

- [ ] The date and exact rolling window are correct.
- [ ] Special Attention contains only configured official sources.
- [ ] Every fixed official source was checked.
- [ ] Every qualifying official update was included.
- [ ] X, HN, and Reddit each contain at least seven verified high-quality items when available.
- [ ] Strong items beyond seven were not arbitrarily discarded.
- [ ] Cross-platform duplicates remain in their respective sections.
- [ ] Every entry has an original URL.
- [ ] Renewed older content is explicitly labeled.
- [ ] Search-index time is not presented as publication time.
- [ ] GitHub includes the complete current page in original order.
- [ ] GitHub stars are from the current capture.
- [ ] The stated GitHub repository total equals the number of rendered repository entries.
- [ ] GitHub repository numbering is continuous from 1 through the stated total.
- [ ] No unsupported titles, numbers, dates, or conclusions remain.
- [ ] No extra overview, potential-signal, action-advice, or sources section was added.

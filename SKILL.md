---
name: ai-newsletter
description: Use when generating a daily or date-specific AI newsletter, monitoring official AI sources, collecting high-value X, Hacker News, and Reddit discussions, or reporting the complete current GitHub Trending daily list.
---

# AI Newsletter

## Overview

Produce a verified Chinese AI newsletter prioritizing high-signal product, research, developer, and early-trend insight.

## Required References

Read `references/sources-and-selection.md` and `references/output-template.md` before researching.

## Workflow

### 1. Establish the Time Window

- Get the current time and user timezone.
- For “today,” use a rolling 24-hour window ending now.
- For a named date without a time, use 00:00 through 23:59:59 in the user timezone.
- State absolute start and end times.
- Distinguish publication, indexing, repost, HN submission, and renewed-discussion times.

### 2. Check Every Fixed Official Source

- Inspect every configured source and verify dates on original pages or metadata.
- Include every verified release or update in the window; never impose a count limit.
- Keep this section exclusive to configured official sources.
- If none qualify, print exactly `今天特别关注模块没有检索到新的内容。`
- Never use the renewed-discussion exception for official content.

### 3. Research Each Community Independently

- Research X, Hacker News, and Reddit separately.
- Return at least seven high-quality topics per community when verifiable material exists.
- Continue beyond seven when more high-quality topics exist.
- Do not pad weak material.
- Preserve cross-platform duplicates and each platform’s angle.
- If access fails, exhaust the documented fallbacks. Never drop an entire community because one method failed.

### 4. Capture GitHub Trending Exactly

- Read `https://github.com/trending?since=daily` at generation time.
- Extract every repository, including non-AI repositories, in exact page order.
- Record stars, original URL, capture time, and repository count.
- Never substitute cached, historical, searched, or remembered repositories.

### 5. Verify Before Writing

- Confirm eligibility, title, claim, URL, numbers, and dates.
- Label eligible older material as renewed discussion.
- Omit any item whose identity, date, or central claim remains uncertain.

### 6. Write and Self-Check

- Write in Chinese while retaining official English proper names.
- Use a concise “developer daily + researcher observation” voice.
- Explain what happened and why it matters.
- Integrate analysis into each item; add no unrequested sections.
- Count rendered GitHub entries after drafting; the stated total and numbering must match.
- Follow `references/output-template.md` exactly.

## Non-Negotiable Rules

| Risk | Required behavior |
|---|---|
| Official boundary drift | “特别关注” contains only configured official sources. |
| X access failure | Use documented fallbacks; do not abandon X. |
| Community undercount | Aim for at least seven; explain only after exhausting discovery methods. |
| Duplicate event | Keep it in each platform section with that platform’s angle. |
| Stale GitHub data | Reject it or label it historical; never present it as current. |
| GitHub filtering | Output every repository in original order. |
| Unsupported detail | Omit it rather than infer or fabricate it. |

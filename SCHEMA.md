# Wiki Schema

## Domain
法律咨询（Legal Consultation）——覆盖中国法律体系的基础理论、常见法律问题解答、典型案例分析，以及律师和律所信息。

## Conventions
- 文件命名：使用小写字母、中划线（不用空格），如 `contract-law.md`、`law-firm-allbrighthonor.md`
- 每个 wiki 页面以 YAML frontmatter 开头（见下方）
- 使用 `[[wikilinks]]` 链接其他页面（每个页面至少 2 个外链）
- 更新页面时，必须更新 `updated` 日期
- 新页面必须添加到 `index.md` 对应板块
- 所有操作必须追加到 `log.md`

## Frontmatter
```yaml
---
title: 页面标题
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | summary
tags: [来自下方分类体系]
sources: [raw/articles/source-name.md]
---
```

## Tag Taxonomy
法律咨询 wiki 的标签分类（使用前须先在此定义）：

- **法域分类**：民法、刑法、行政法、商法、劳动法、知识产权法、婚姻家庭法
- **实体类型**：person（自然人）、company（企业法人）、government（政府机构）、court（法院）、law-firm（律所）
- **概念术语**：right（权利）、obligation（义务）、liability（责任）、contract（合同）、crime（犯罪）、tort（侵权）
- **程序类型**：litigation（诉讼）、arbitration（仲裁）、mediation（调解）、negotiation（谈判）
- **文书类型**：判决书、裁定书、调解书、合同、协议、律师函
- **元标签**：comparison（对比分析）、timeline（时间线）、case-study（案例）、faq（常见问题）、dispute（争议）

## Page Thresholds
- **创建页面**：某实体/概念在 2+ 来源中出现，或在一个来源中处于核心位置
- **追加现有页面**：新来源提及已有内容时，更新现有页面而非创建重复
- **不创建页面**：仅在脚注中一次性提及的次要名称、过于细节的临时信息
- **拆分页面**：页面超过 200 行时，拆分为子主题并互相链接
- **归档页面**：内容完全被新信息取代时，移至 `_archive/`，从 index.md 移除

## Entity Pages（实体页）
每个值得关注的实体单独一页，包含：
- 概述 / 基本信息
- 关键事实与日期
- 与其他实体的关系（使用 [[wikilinks]]）
- 来源引用

## Concept Pages（概念页）
每个法律概念或主题单独一页，包含：
- 定义与解释
- 当前法律状态与适用范围
- 争议问题或学术讨论
- 相关概念（[[wikilinks]]）

## Comparison Pages（对比页）
并排分析，包含：
- 对比对象及对比原因
- 对比维度（建议使用表格）
- 分析结论或综合判断
- 来源

## Update Policy
新信息与现有内容矛盾时：
1. 查看日期——较新的来源通常取代旧来源
2. 确有矛盾时，注明双方观点及各自来源日期
3. 在 frontmatter 中标记：`contradictions: [page-name]`
4. 在 lint 报告中提示用户审核

## Log Rotation
当 `log.md` 超过 500 条时，将其重命名为 `log-YYYY.md`，重新开始新的 `log.md`。

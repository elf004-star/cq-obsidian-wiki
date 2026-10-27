# Wiki Schema

## Domain
法律与制度研究（Law, Policy, History & Politics）——覆盖：
1. **法律**：中国法律体系基础理论、法条文本、典型案例分析、常见法律问题解答
2. **政策**：政策文件、治理逻辑、监管改革、政策演变
3. **历史**：历史事件、制度沿革、历史人物与决策背景
4. **政治**：政治制度、权力结构、比较政治、选举与代表制度

**底线原则**：所有论断必须锚定于真实法条、官方文件或可靠来源；无法核实的标注 `[待核实]`，绝不虚构。

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
digest: 一句话核心结论（≤60字，用于 index 与检索）
status: current | superseded | archived   # 现行 / 已被取代 / 已归档
layer: overview | standard | deep          # 页面深度层级
valid_from: YYYY-MM-DD                     # 法律生效日 / 事件发生日
valid_until: YYYY-MM-DD                    # 失效日，现行则留空
supersedes: [page-name]                    # 本页取代了谁
superseded_by: [page-name]                 # 本页被谁取代
---
```

---

## 分层摘要规范（Layered Digest — 核心机制）

wiki 是一本**活页笔记本**：随时可插入新活页、随时把过时活页下沉。为了让「按需深入」可行，每页必须有四层摘要，**上层永远能独立读通，下层才展开细节**。

| 层级 | 位置 | 篇幅 | 作用 |
|---|---|---|---|
| **L0 索引层** | `index.md` 中该页的一行 | ≤40 字 | 扫一眼知道这页讲什么 |
| **L1 摘要层** | 页面顶部 `## 摘要` | 3–5 条 bullet | 只读这一段就能回答「是什么／关键条款／为什么重要」 |
| **L2 章节层** | 每个 `##` 章节末尾 `### 要点` | 2–3 条 bullet | 定位到某一章时，不必读完整章正文 |
| **L3 细节层** | 章节正文 / 独立深挖页 | 不限 | 条文原文、案例细节、争议观点 |

**写作规则：**
1. **先写 L1 再写 L2** —— 摘要不是事后提炼，是写作前的结论先行。
2. **每个 `##` 章节必带 `### 要点`**，否则视为未完成页面（lint 会标记）。
3. **超过 200 行 → 拆分**：保留 overview 页（L0+L1+L2），细节移入 `<topic>-deep-dive.md`（L3），双向链接。
4. **按需深入**：用户问细节时才读 L3；若某次 L3 讨论产生了新结论，**回写到对应页面**（而不是留在对话里消失）。
5. `digest` 字段与 index 行保持一致，二者同时更新。

**章节模板：**
```markdown
## 摘要
- 核心定位：……
- 关键条文／事实：……
- 时效状态：现行有效（YYYY-MM-DD 起）／已修订
- 为什么重要：……

## 一、基本概况
正文……
### 要点
- ……
```

---

## 时效与下沉规则（Staleness & Downshifting — 核心机制）

法律会修、政策会变、历史评价会翻案。**发现过时信息不是删除，而是「下沉」**——保留可追溯的历史层级，让当前结论永远浮在最上层。

### 触发下沉的信号
- 法条被修订、废止或被新法取代
- 政策文件被新版替代／试点转正式
- 出现权威新史料、新判决推翻旧理解
- 司法观点/指导案例改变（如指导性案例被废止）

### 下沉动作（按顺序执行）
1. **不删除**：把旧内容整段移入 `## 历史沿革（已失效／已被修正）` 章节，注明原生效期间与修正依据。
2. **改状态**：frontmatter 写 `status: superseded`、`superseded_by: [[新页]]`、`valid_until: YYYY-MM-DD`。
3. **抬新结论**：新条文／新结论写入 L1 摘要与对应章节，旧结论降为 L3。
4. **标索引**：`index.md` 该行加 `⚠️ 已修订（YYYY-MM）` 前缀。
5. **记日志**：`log.md` 写 `## [YYYY-MM-DD] downshift | 页面名 — 原因`。
6. **整页失效**（如整部法律废止）→ 移入 `_archive/`，从 index 移除，其余页面的 wikilink 改为纯文本 + `(已废止)`。

### 定期核查
- `_meta/staleness-watch.md` 维护「需定期复查时效」清单（改动频繁的法律、政策、在审案件）。
- 每次 session 开始，若距上次 lint > 30 天，先跑一次时效核查再开始新任务。
- 核查结果写入 `_meta/staleness-watch.md` 与 `log.md`。

---

## Tag Taxonomy
标签分类（使用前须先在此定义）。标签须全部小写。

### 法域分类
- **民法**、**刑法**、行政法、**商法**、劳动法、**知识产权法**、婚姻家庭法
- **基本法律**：全国人大制定，效力仅次于宪法（如公司法、刑法、民法典等）
- **行政法规**：国务院根据宪法和法律制定的行政法规
- **法典**：重要法典（如民法典）
- **刑事法律**：刑法及相关法律
- **犯罪与刑罚**：刑法核心概念
- **公司法**、**公司**、**商标**、**著作权**
- **消费者权益**、**个人所得税**、**个人所得税法**、**居民纳税人**、**非居民纳税人**
- **土地管理**、**individual-income-tax**、**resident-tax**、**non-resident-tax**
- **npc**、**rule-of-law**

### 实体类型
- person（自然人）、company（企业法人）、**government**、**court**、law-firm
- **legislature**、**administration**、**executive**、**supervision**、**state-power**、**supreme-power**
- **judiciary**、**adjudication**
- **entity**

### 概念术语（法律）
- right、obligation、liability、contract、**crime**、tort
- **constitutional-law**、**fundamental-law**、**legal-hierarchy**
- **administrative-law**、**commercial-law**、**tax-law**
- **civil-rights**、**minority-rights**、**suffrage**
- **anti-corruption**、**legal-supervision**、**procuratorate**、**prosecution**
- **litigation**、**adjudication**、**fiscal-supervision**
- **electoral-law**、**local-peoples-congress**
- **land-management**、**farmland-protection**、**land-expropriation**、**rural-land**
- **trade-secret**、**commercial-bribery**、**fair-competition**、**anti-unfair-competition**
- **state-owned-assets**、**audit-law**
- **ethnic-autonomy**、**autonomous-region**
- **hksar**、**one-country-two-systems**、**basic-law**

### 政策与治理
- **policy**（政策）、**policy-analysis**、**public-policy**、**governance**、**regulation**、**regulatory-reform**
- **policy-document**（政策文件）、**white-paper**、**five-year-plan**（五年规划）、**reform**（改革）
- **economic-policy**、**social-policy**、**industrial-policy**、**fiscal-policy**

### 历史
- **history**、**historical-event**、**timeline**、**institutional-evolution**（制度沿革）
- **modern-china**（近代中国）、**imperial-china**（古代／帝制）、**republic-era**（民国）、**reform-era**（改革开放）
- **dynasty**、**historical-figure**、**primary-source**（一手史料）

### 政治与制度
- **political-system**、**political-institution**、**state-structure**、**comparative-politics**
- **political-party**、**election**、**legislative-process**、**separation-of-powers**
- **authoritarianism**、**democratization**、**political-economy**、**federalism**、**central-local-relations**

### 文书类型
- 判决书、裁定书、调解书、合同、协议、律师函

### 元标签
- **type:entity**、**type:concept**、**type:comparison**、**type:query**
- **concept**、**entity**、comparison、timeline、case-study、faq、dispute
- **needs-review**（待核实）、**disputed**（存在争议）、**source-quality**（来源质量）

## Page Thresholds
- **创建页面**：某实体/概念在 2+ 来源中出现，或在一个来源中处于核心位置
- **追加现有页面**：新来源提及已有内容时，更新现有页面而非创建重复
- **不创建页面**：仅在脚注中一次性提及的次要名称、过于细节的临时信息
- **拆分页面**：页面超过 200 行时，按「分层摘要规范」拆为 overview + deep-dive
- **归档页面**：内容完全被新信息取代时，按「时效与下沉规则」处理

## Entity Pages（实体页）
每个值得关注的实体单独一页，包含：
- 概述 / 基本信息（L1 摘要）
- 关键事实与日期
- 与其他实体的关系（使用 `[[wikilinks]]`）
- 来源引用

## Concept Pages（概念页）
每个法律概念或主题单独一页，包含：
- 定义与解释
- 当前法律状态与适用范围
- 争议问题或学术讨论
- 相关概念（`[[wikilinks]]`）

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
4. 若为法律/政策时效性变化 → 走「时效与下沉规则」，而非简单覆盖
5. 在 lint 报告中提示用户审核

## Log Rotation
当 `log.md` 超过 500 条时，将其重命名为 `log-YYYY.md`，重新开始新的 `log.md`。

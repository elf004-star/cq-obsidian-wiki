# Wiki Log

>  chronological record of all wiki actions. Append-only.
> Format: `## [YYYY-MM-DD] action | subject`
> Actions: ingest, update, query, lint, create, archive, delete
> When this file exceeds 500 entries, rotate: rename to log-YYYY.md, start fresh.

## [2026-04-13] create | Wiki initialized
- Domain: 法律咨询（Legal Consultation）
- Structure created with SCHEMA.md, index.md, log.md
- Directories: raw/articles/, raw/papers/, raw/transcripts/, raw/assets/, entities/, concepts/, comparisons/, queries/

## [2026-04-13] ingest | 中华人民共和国宪法
- Source: http://www.npc.gov.cn/c2/c30834/201905/t20190521_281393.html
- Created: raw/articles/npc-constitution-2018.md
- Created entities: national-people-congress.md, state-council.md, supreme-peoples-court.md, supreme-peoples-procuratorate.md
- Created concepts: constitution.md, legal-system-hierarchy.md, citizens-basic-rights.md
- Updated: index.md, log.md

## [2026-04-13] ingest | 民法典、公司法、商标法、著作权法、消费者权益保护法
- 批量收录5部中国基本法律
- 民法典：raw/articles/civil-code-2020.md，概念页：concepts/civil-code.md
- 公司法：raw/articles/company-law-2023.md，概念页：concepts/company-law.md
- 商标法：raw/articles/trademark-law-2024.md，概念页：concepts/trademark-law.md
- 著作权法：raw/articles/copyright-law-2020.md，概念页：concepts/copyright-law.md
- 消费者权益保护法实施条例：raw/articles/consumer-protection-law-implementation-2024.md，概念页：concepts/consumer-protection-law.md
- 更新：index.md
## [2026-04-14] ingest | 更新法律条文全文入库
- 批量更新5部法律条文原始文本（原有文件仅为来源链接，现已替换为完整正文）
- 公司法（2023修订）：raw/articles/company-law-2023.md（13KB）

## [2026-04-14] ingest | 选举法、香港基本法、民族区域自治法、国务院组织法（2024修订）
- 收录4部新法律原始文本至 raw/articles/
- 创建 entities/hk-basic-law.md（香港基本法实体页）
- 创建 concepts/election-law.md（选举法概念页）
- 创建 concepts/regional-ethnic-autonomy-law.md（民族区域自治法概念页）
- 更新 entities/state-council.md（新增2024年组织法内容）
- 更新 index.md、log.md

## [2026-04-14] create | 修复断链 — 新增2个缺失页面
- Created: entities/state-commission-supervision.md — 国家监察委员会（2018年设立，与检察院合署）
- Created: concepts/procuratorate-system.md — 检察系统完整体系（公诉、法律监督、公益诉讼）
- Updated: index.md（Entities + Concepts 板块）
- Updated: log.md


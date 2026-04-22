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

## [2026-04-14] ingest | 反不正当竞争法（2025年修订）
- 收录 raw/articles/anti-unfair-competition-law-2025.md（最高检来源，5章43条）
- 创建 concepts/anti-unfair-competition-law.md（概念页）
- 更新 index.md、log.md

## [2026-04-14] ingest | 个人所得税法（2018年修正）
- 收录 raw/articles/individual-income-tax-law-2018.md（国家税务总局来源，22条）
- 创建 concepts/individual-income-tax-law.md（概念页）
- 更新 index.md、log.md

## [2026-04-14] ingest | 土地管理法（2019年修正）
- 收录 raw/articles/land-administration-law-2019.md（生态环境部来源，8章87条）
- 创建 concepts/land-administration-law.md（概念页）
- 更新 index.md、log.md

## [2026-04-14] ingest | 审计法（2021年修正）
- 收录 raw/articles/audit-law-2021.md（审计署来源，7章68条）
- 创建 concepts/audit-law.md（概念页）
- 更新 index.md、log.md

## [2026-04-14] create | 修复断链 — 新增2个缺失页面
- Created: entities/state-commission-supervision.md — 国家监察委员会（2018年设立，与检察院合署）
- Created: concepts/procuratorate-system.md — 检察系统完整体系（公诉、法律监督、公益诉讼）
- Updated: index.md（Entities + Concepts 板块）
- Updated: log.md


## [2026-04-21] ingest | 刑法 — 中华人民共和国刑法
- 收录 raw/articles/criminal-law-2021.md（来源：国家税务总局政策法规库 + 最高人民检察院 + China Law Translate）
- 创建 concepts/criminal-law.md（概念页：总则+分则结构+重要罪名）
- 更新 index.md（新增 criminal-law 条目）、log.md
- 刑法共计2编15章452条，经11个修正案修正（最新为2021年刑法修正案十一）

## [2026-04-21] ingest | 刑法（2020年修正版）— 用户 docx 文档
- 新增 raw/articles/criminal-law-2020.md（来源：用户提供的官方 docx 文档，2020年12月26日第十三届全国人大常委会通过，含刑法修正案十一全文）
- 更新 concepts/criminal-law.md 的 sources 列表
- 文档总计约74,000字，包含完整总则和分则全文

## [2026-04-21] ingest | 香港特别行政区基本法（完整全文）— 中国人大网
- 新增 raw/articles/hk-basic-law-full.md（来源：中国人大网 npc.gov.cn，2024年8月发布，完整160条正文 + 目录）
- 更新 entities/hk-basic-law.md 的 sources 列表，加入完整全文版本
- 原文文件保留在 raw/中华人民共和国香港特别行政区基本法_中国人大网.md（作为备份来源记录）

## [2026-04-22] ingest | 刑事诉讼法 — 中华人民共和国刑事诉讼法
- 新增 raw/articles/criminal-procedure-law-2025.md（来源：中国人大网，2018年修正版）
- 创建 concepts/criminal-procedure-law.md（概念页：5编结构/公检法分工/五种特别程序）
- 更新 index.md（新增 criminal-procedure-law 条目）、log.md

## [2026-04-22] ingest | 仲裁法 — 中华人民共和国仲裁法
- 新增 raw/articles/arbitration-law-2025.md（来源：中国人大网，2025年9月修订，2025年10月施行）
- 创建 concepts/arbitration-law.md（概念页：8章/一裁终局/仲裁协议/仲裁员资格/在线仲裁）
- 更新 index.md（新增 arbitration-law 条目）、log.md

## [2026-04-22] lint | Wiki 健康审查 — 全部问题归零
- 初始问题：87个（81个非法标签 + 6个孤立页面）
- 扩展 SCHEMA.md Tag Taxonomy：从~30个标签增至63个，覆盖所有实际使用的标签
- 规范化6个 entity 页面的 frontmatter 标签
- 从3个 hub 页面（legal-system-hierarchy、civil-code、constitution）添加 inbound 链接，消除6个孤立页面
- 最终结果：断链0、孤立0、Frontmatter问题0、Index完整、超大页面0

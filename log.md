# Wiki Log

> chronological record of all wiki actions. Append-only.
> Format: `## [YYYY-MM-DD] action | subject`
> Actions: ingest, update, query, lint, create, archive, delete
> When this file exceeds 500 entries, rotate: rename to log-YYYY.md, start fresh.

## [2026-04-22] query | 张三醉驾致死逃逸案法律分析
- Query: 张三醉驾致女生死亡后逃逸并自首，应如何判刑
- 分析报告已保存: queries/zhangsan-drunk-driving-fatality-analysis.md
- 引用法条: 刑法第133条（交通肇事罪）、第133条之一（危险驾驶罪）、第67条（自首）
- 初步结论: 以交通肇事罪论处，可能3年以下至3-7年有期徒刑，自首可从轻或减轻

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

## [2026-04-22] ingest | 企业破产法 — 中华人民共和国企业破产法
- 新增 raw/articles/state-taxation-regulations.md（来源：国家税务总局政策法规库，实际内容为企业破产法，2006年）；标题已更正
- 创建 concepts/bankruptcy-law.md（概念页：重整/和解/破产清算三程序/管理人制度/职工债权保护/域外效力）
- 更新 index.md（新增 bankruptcy-law 条目）、log.md

## [2026-04-22] ingest | 行政诉讼法 — 中华人民共和国行政诉讼法
- 新增 raw/articles/administrative-procedure-law-2025.md（来源：中国人大网，2017年修正版）
- 创建 concepts/administrative-procedure-law.md（概念页：10章/合法性审查/举证责任倒置/与行政复议关系）
- 更新 index.md（新增 administrative-procedure-law 条目）、log.md

## [2026-04-22] ingest | 民事诉讼法 — 中华人民共和国民事诉讼法
- 新增 raw/articles/civil-procedure-law.md（来源：司法部官网，2017年修正版）
- 创建 concepts/civil-procedure-law.md（概念页：3编结构/证据制度/调解保全/两审终审/与刑诉法比较）
- 更新 index.md（新增 civil-procedure-law 条目）、log.md

## [2026-04-22] ingest | 合伙企业法 — 中华人民共和国合伙企业法
- 新增 raw/articles/partnership-law.md（来源：国家市场监督管理总局，2006年修订）
- 创建 concepts/partnership-law.md（概念页：普通合伙/有限合伙/特殊普通合伙/税务穿透/与公司法比较）
- 更新 index.md（新增 partnership-law 条目）、log.md

## [2026-04-22] ingest | 反垄断法 — 中华人民共和国反垄断法
- 新增 raw/articles/anti-monopoly-law.md（来源：国家市场监督管理总局，2022年修正）
- 创建 concepts/anti-monopoly-law.md（概念页：三类垄断行为/2022修正要点/与反不正当竞争法关系）
- 更新 index.md（新增 anti-monopoly-law 条目）、log.md

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

## [2026-10-27] update | 建立 H博士 角色与两项核心机制
- 定位：wiki 从「法律咨询」升级为「法律·政策·历史·政治」四域馆藏，服务长期学习与探讨
- SCHEMA.md 重写：Domain 扩展；新增 Frontmatter 字段（digest / status / layer / valid_from / valid_until / supersedes / superseded_by）
- SCHEMA.md 新增「分层摘要规范」：L0 索引行 → L1 页面摘要 → L2 章节要点 → L3 细节，先写摘要后写正文，超 200 行拆 overview + deep-dive
- SCHEMA.md 新增「时效与下沉规则」：过时内容移入「历史沿革（已失效）」并标记 status: superseded，整页失效移入 `_archive/`
- SCHEMA.md Tag Taxonomy 扩至政策（policy / governance / regulation）、历史（history / institutional-evolution）、政治（political-system / state-structure）三组
- 新建 `_meta/staleness-watch.md`：5 条高优先级待核查 + 季度常规复查清单 + 核查方法
- index.md 更新头部说明与日期；[[civil-procedure-law]] 标注 ⚠️ 时效待核查（页面为2017版，后续修正情况未核实）

## [2026-10-27] ingest | 国体与国家性质（首篇四域全开页面）
- 新增 raw/articles/mao-new-democracy-1940-guoti.md — 《新民主主义论》第五节节选（马克思主义文库），含国体/政体定义原文
- 新增 raw/articles/constitution-state-nature-evolution.md — 国体条款沿革对照：共同纲领（1949）／1954／1975／1978／1982，逐条来源标注
- 创建 concepts/state-nature-guoti.md — 六章：概念出处／宪法第一条四要素／三分框架／人民民主专政两面性／表述沿革／开放问题
- 更新 concepts/constitution.md — 补分层摘要与全部章节 ### 要点，新增国体链接、条款数（143条）、修正案要点细化
- 更新 index.md（新增 state-nature-guoti + 两条 raw sources，Total pages 30→31）、log.md
- 核实结论：宪法第一条、第二条原文经外交部官网 + 香港基本法网站双源比对一致；2018修宪新增党的领导入第一条第二款属实
- 遗留待核：1978年宪法第一条逐字原文未与官方数据库全文比对，已在 raw 文件标注 `[待逐字核验]`

## [2026-10-27] ingest | 政体（政权组织形式）
- 新增 raw/articles/constitution-chapter1-general-principles.md — 宪法第一章第一条至第五条逐字原文（香港律政司基本法网站核对，2018年修正后文本）
- 创建 concepts/form-of-government-zhengti.md — 七章：概念出处／政体两层次（机关来源＋机关关系）／中国政体宪法构造逐条定位／国体政体结构三分界／「政体——民主集中制」文本张力三种解释／五个常见误解／四个开放问题
- 核心辨析结论：政体＝人民代表大会制度；民主集中制是第三条第一款的**组织原则**，非政体本身；第三条第四款属国家结构形式而非政体
- 关键史料张力：毛泽东1940年《新民主主义论》原文写「政体——民主集中制」，与今日通说不一致；官方复合表述「建立在民主集中制基础上的人民代表大会制度」用于焊接两层；页面给出三种解释并说明层次拆分说解释力较强
- 引用学者观点：马岭《我国宪法中的民主集中制原则》（明德公法网），已具名标注
- 更新 concepts/state-nature-guoti.md（新增政体页链接）、index.md（Total pages 31→32）、log.md
- 待核：宪法第三条2018年增写「监察机关」已在 raw 文件注明；「议行合一」标签适用性、政体概念替代之争均标 `[待核实具体文献]`

## [2026-10-27] ingest | 权力分立（三权分立）
- 新增 raw/articles/separation-of-powers-primary-texts.md — 关键文本辑录：孟德斯鸠《论法的精神》法文原版（第十一章第四、六节，含「le pouvoir arrête le pouvoir」与「裁判权等于零」原句）、联邦党人文集第47/51/78篇、白芝浩《英国宪政》「efficient secret」段；来源 Project Gutenberg 逐字核对
- 创建 concepts/separation-of-powers.md — 八章：发明还是机缘（三层叠加）／四层谱系（亚里士多德→波利比乌斯→洛克→孟德斯鸠→美国）／英国不搞分权的反讽／美国从分权到制衡＋司法审查／优点四点／缺点六点／中国不采用的官方三支点与两处张力／一句话总结
- 关键考据结论：
  · 亚里士多德《政治学》第四卷只做职能分类，非制约机制；波利比乌斯为「混合政体」（按阶级分权），与「分权」（按职能分立）是两条不同传统
  · 洛克《政府论》下篇只有立法／执行／对外三权，**无独立司法权**
  · 孟德斯鸠法文原版编者（Paul Janet）按语明言「孟德斯鸠并未创造这一学说」；孟本人称裁判权「在某种意义上等于零」，并需世袭贵族院作「调剂权力」——现代三权分立属选择性继承
  · 白芝浩 1867 年已证英国实为行政与立法「近乎完全的融合」，与孟德斯鸠所推崇的样板结构性错位
  · 麦迪逊《联邦党人》第47篇自承各分支「部分参与」（partial agency），纯粹分权从未存在
  · 司法审查（1803 马伯里案）非宪法明文，属司法实践生长
- 更新 concepts/state-nature-guoti.md、concepts/form-of-government-zhengti.md（互加链接）、index.md（Total pages 32→33）、log.md
- 待核：「议行合一」标签适用性仍标 `[待核实具体文献]`

## [2026-10-27] ingest | 中国的人大监督体系（纵向监督）
- 新增 raw/articles/oversight-law-2024.md — 监督法 2024 年修正版（9章65条）核心条文全文摘录 + 2006版（9章48条）章节对照表；来源：国家法律法规数据库镜像 + 共产党员网（版本比对）
- 新增 raw/articles/constitution-chapter3-state-organs.md — 宪法第六十二、六十三、六十七、七十一、七十三、七十七、一百零四条原文（2018修正后文本）
- 创建 concepts/supervision-system-china.md — 七章：纵向vs横向结构辨析／宪法条文谱系／监督法九级强度阶梯／2024修正四个实质变化／三个真实限度／五轨监督分工／五个开放问题
- 时效核实结论（重要）：监督法已于 **2024-11-08** 由十四届全国人大常委会第十二次会议修正，条文由 48 条增至 65 条。此前若引用「2006年监督法」即属过时，本页以 2024 版为准
- 2024修正四个实质变化：①监察委员会纳入监督对象（补2018修宪的时间差）②「专题询问」从2010年起的实践上升为法定制度（第六章标题改为「询问、专题询问和质询」）③第三章整章重构为「财政经济工作监督」，新增国有资产、政府债务、金融工作年度报告义务④备案审查工作情况须每年听取审议（第四十五条）
- 发现条文差异（已如实记录，未下结论）：宪法第七十三条质询对象仅列「国务院或者国务院各部、各委员会」，而监督法第五十一条扩至监察委员会、法院、检察院；此差异自2006年即存在
- 发现条文事实：撤职案主体仅为「县级以上地方各级人大常委会」（第六十条），**全国人大常委会无人事处置权**，国务院组成人员去职走宪法第六十三条罢免程序
- 更新 concepts/separation-of-powers.md、concepts/form-of-government-zhengti.md、concepts/state-nature-guoti.md（互加链接）、SCHEMA.md（新增 oversight / accountability / transparency 标签）、index.md（Total pages 33→34）、log.md
- 待补充：质询案、特定问题调查案、撤职案的具体公开实例；备案审查「撤销权」实际行使率（建议逐年追踪法工委年度备案审查工作报告）

## [2026-10-28] update | 权力分立：补充谱系空白并拆分为 overview + deep-dive
- 新增 raw/articles/separation-of-powers-genealogy-supplement.md — 六份此前缺失的一手文本与文献书目：马萨诸塞州宪法1780第三十条（逐字，英语世界首次以宪法条文禁止三部门互行对方权力）、英国《宪法改革法2005》四项变化（御前大臣司法职能取消／最高法院2009／司法任命委员会／2006-04-03生效）、博丹《国家六论》主权不可分割、卢梭《社会契约论》第二卷第二章、马西利乌斯《和平保卫者》1324立法者/执行权威二分、查理一世《答十九项建议》1642「三种政体混合」、孙中山五权分立1906年首次提出的原始表述
- 新建 concepts/separation-of-powers-deep-dive.md（L3 深挖页，11章）— 承接原页全部细节，并补入：马西利乌斯／查理一世1642两条此前完全缺席的谱系节点；博丹与卢梭「主权不可分割」作为分权唯一的根本性理论反驳（原页完全未提，属实质缺口）；美国州宪先行段（1776弗吉尼亚／1780马萨诸塞）说明联邦宪法反而比州宪宽松；英国2005年改革；扩散与变异（法国1791→半总统制、德国基本法防御性民主、日本附随审查、韩国宪法法院、孙中山五权）；经验研究四份文献的争点（North&Weingast 1989收益侧／Tsebelis否决玩家成本侧／Linz 1990风险侧／Cheibub&Limongi 2002反驳，明确标注争议未决）；三权之外的现代层次（纵向联邦制、第四权、时间维度错开任期）
- 重写 concepts/separation-of-powers.md 为 overview 页（L0+L1+L2，17383字节，原281行超200行阈值）— 摘要扩至6条；九章各带 `### 要点`；新增「二、谱系：两条不能混用的传统」表格式辨析（混合政体按阶级 vs 权力分立按职能）与「五、最硬的反驳：主权不可分割」独立章节；第八章补入孙中山五权宪法作为「三权数目非必然」的证据
- 更新 index.md（新增 deep-dive 行 + 新 raw source，Total pages 34→35，Last updated 2026-10-27→2026-10-28）、log.md
- 关键考据结论（新增，均标来源）：
  · 马萨诸塞1780第三十条措辞为「shall never exercise」，比联邦宪法更严格；末句「a government of laws and not of men」出自此处
  · 孟德斯鸠所称英国分权，与1642年英国自身「混合政体」自我理解（查理一世《答十九项建议》）不是同一回事，前置错位可解释其误读
  · 卢梭区分「主权不可分」与「职能可分工」，当代「主权归属不可分／权力行使可分」的调和路径建立在此缝隙上，但属后世处理
  · 孙中山五权分立自述首次提出于1906年12月东京《民报》周年纪念会《三民主义与中国民族之前途》演说
- 待核（已在 raw 文件逐条标注）：卢梭第二卷第二章逐字法文原文、博丹引文为英译转引非1606年英译本比对、马西利乌斯为Fordham节译非拉丁校勘本、台湾地区考试院监察院现行职能、North&Weingast后续修正文献未系统收录



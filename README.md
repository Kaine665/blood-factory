# 血汗 Agent（blood-factory）

一个能对任意产品自动执行供应链劳动调查、产出证据型报告的 agent。

## 为什么做这个

AI 降低了生产成本，扩大了利润空间，但增量没有被社会共享，而是被资本方截留。
看不见的剥削无法被讨论——**透明是一切博弈的前提**。

血汗 agent 回答三个问题：

1. **链路**：一个产品从原材料到上架，经过了哪些公司，各做了什么
2. **分工**：每一环拿走了零售价的百分之几
3. **血汗**：每一环的劳动状况——工资、工时、社保、劳动争议、与企业宣传的矛盾

## 产品原则

- **定位**：调查弹药生成器，服务写报告的人（记者、KOL、研究者），不是消费者 App
- **立场**：呈现证据 + 标注矛盾，不打分、不下结论；所有信息标注置信度
- **边界**：只用公开数据（财报、行政处罚、招聘信息、媒体报道、公开爆料）；
  第一阶段只做国内链路；不做举报/维权平台
- **诚实**:查不到就明说查不到，"链路在此处断裂"本身也是事实；
  证据显示某环节不血汗时，照实写

## 验证命题

agent 能否完成人类调查记者数周的工作？

## 复刻本项目

完整方法论已沉淀为独立手册：[PLAYBOOK.md](PLAYBOOK.md)。
任何人 + 任何能联网检索的 LLM，照手册可产出同等证据标准的报告；
含信源操作指引（及坑）、置信度判定、报告模板、对照范式库、跨法域信源对照表。

## 调查报告

| 日期 | 产品 | 报告 |
|---|---|---|
| 2026-06 | 蜜雪冰城 4 元冰鲜柠檬水 | [reports/2026-06-mixue-lemonade.md](reports/2026-06-mixue-lemonade.md) |
| 2026-06 | 特斯拉 Model Y 上的福耀玻璃 | [reports/2026-06-fuyao-modely.md](reports/2026-06-fuyao-modely.md) |
| 2026-06 | 胖东来"自由·爱"白酒（⚠️ 对照组） | [reports/2026-06-pdl-ziyouai.md](reports/2026-06-pdl-ziyouai.md) |
| 2026-06 | 永辉"咏悦汇小酌"酱香酒（转型中间态） | [reports/2026-06-yonghui-yongyuehui.md](reports/2026-06-yonghui-yongyuehui.md) |
| 2026-06 | 蔡司眼镜镜片（基金会企业 × 跨法域镜像） | [reports/2026-06-zeiss-lenses.md](reports/2026-06-zeiss-lenses.md) |
| 2026-06 | 宁德时代动力/储能电池（上市链主 × 高研发制造） | [reports/2026-06-catl-battery.md](reports/2026-06-catl-battery.md) |
| 2026-06 | SK hynix HBM/存储芯片（高薪血汗 × 强工会利润分享） | [reports/2026-06-sk-hynix-hbm.md](reports/2026-06-sk-hynix-hbm.md) |
| 2026-06 | NVIDIA AI GPU / Blackwell（无厂链主 × 代理薪酬口径） | [reports/2026-06-nvidia-ai-gpu.md](reports/2026-06-nvidia-ai-gpu.md) |
| 2026-06 | 腾讯微信/游戏/云/AI 平台（完整薪酬口径 × 高薪本部） | [reports/2026-06-tencent-wechat-platform.md](reports/2026-06-tencent-wechat-platform.md) |
| 2026-06 | 淘宝/天猫 + 阿里云（薪酬总额缺口 × 出表边界变化） | [reports/2026-06-alibaba-taobao-platform.md](reports/2026-06-alibaba-taobao-platform.md) |
| 2026-06 | 抖音/TikTok（私企估算 × AI 账单与抢人激励） | [reports/2026-06-bytedance-douyin-platform.md](reports/2026-06-bytedance-douyin-platform.md) |

### 专题对比

| 主题 | 文档 |
|---|---|
| 永辉 × 胖东来：学生与老师的分配账本 | [reports/cross-company/2026-06-compare-yonghui-pdl.md](reports/cross-company/2026-06-compare-yonghui-pdl.md) |
| 劳资分配排行榜：资本拿得比劳动多多少 | [reports/cross-company/2026-06-labor-capital-ranking.md](reports/cross-company/2026-06-labor-capital-ranking.md) |
| 员工人均收入排行榜（人民币口径） | [reports/cross-company/2026-06-employee-income-ranking.md](reports/cross-company/2026-06-employee-income-ranking.md) |
| 员工收入 ÷ 当地基本需求覆盖倍数榜 | [reports/cross-company/2026-06-income-vs-basic-needs-ranking.md](reports/cross-company/2026-06-income-vs-basic-needs-ranking.md) |
| 字节 × 阿里 × 腾讯：互联网巨头的劳动账本 | [reports/cross-company/2026-06-china-internet-giants.md](reports/cross-company/2026-06-china-internet-giants.md) |

## 跨案例指标

单篇报告讲故事，跨案例指标沉淀数据资产。每个案例完成后回填一行到
[reports/cross-company/cross-metrics.md](reports/cross-company/cross-metrics.md)（血汗指标体系 v0.1）：

- **A 分配类**：劳资分配比（净利润÷全员薪酬）、人均创利 vs 人均薪酬、薪酬阶梯倍数、单品劳/资含量
- **B 边界类**：报表外劳动者规模、ESG 承诺覆盖率
- **C 强度类**：班制、月休、推算月工时、最低时薪证据
- **D 保障类**：社保、合同、司法记录
- **E 修辞类**：公司捐赠占净利比、宣传-证据矛盾点

## 报告结构（标准四段式）

1. **链路还原**——每环公司名 + 证据来源
2. **价值分配**——零售价拆解，每个数字附来源和置信度
3. **劳动证据墙**——薪资、工时、社保、劳动争议，每条附原始链接
4. **矛盾点**——企业宣传 vs 证据的对照表

### 置信度标注

规范形式为文字标记（emoji 仅作可选装饰，部分环境不显示）：

- **【直接】**：官方披露（财报/招股书）、行政处罚、司法判决、企业官方自述、严肃媒体实地调查（🟢）
- **【间接】**：招聘信息、个人公开爆料、行业报道、无审计的创始人自述（🟡）
- **【推断】**：基于公开数据的计算，附假设条件（🔵）
- **【缺口】**：查过但查不到，必须显式标出（⬜）

### 必查项清单（每份报告逐项核查）

1. **财报附注三件套**：应付职工薪酬（工资总额）/ 员工人数 / 董监高薪酬。
   三者交叉可得出"净利润 vs 全员薪酬""薪酬阶梯倍数""报表边界内外的人数差"等核心结构性数字。
   港股注意：业绩公告可能不单独列示董事酬金，需查年报全文。
   另查附注内**辞退福利**科目——裁员规模的财务指纹（永辉案例确立）
2. **司法判决检索**：[工劳网劳动争议判决文书库](https://search.laborinfocn2.com/lawcases)
   （约 180 万份判决书，覆盖 2008~2023，弥补裁判文书网收缩）。
   检索目标公司及核心子公司名；判决书可将工时/派遣/工伤等爆料升级为司法认定事实（🟢）。
   局限：2023 年后无数据；天眼查/企查查司法风险页需登录，暂不可用作 agent 入口
3. 招聘网站在招岗位（薪资、工时、排班的稳定信源）
4. 行政处罚记录（少数能直接定性的证据类型）
5. 企业 ESG 报告 / 官网宣传（矛盾点对照的原材料）

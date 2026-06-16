# Amazon Product Manager Skill 中文说明

这是一个给 Codex / AI Agent 使用的 Amazon 产品经理决策 skill。

它不是爬虫，也不是“自动出爆品”的工具。它更像是一套可复用的 AI 产品经理工作流，用来把 Amazon 选品、市场筛选、Launch、利润修复、库存风险和 Go / No-Go 决策变得更结构化。

## 适合谁

- 做 Amazon / 跨境电商的中小卖家
- 需要用 AI 做选品、市场调研、竞品分析的人
- 想把零散判断整理成固定决策流程的产品经理或运营
- 正在构建 Codex / AI Agent 工作流的人

## 它能做什么

- 判断某个市场、品类、价格带是否值得进入
- 对多个产品方向做 `Enter Market` / `Watch Market` / `Avoid Market` 判断
- 对单个产品做 `Go` / `No-Go` / `Test First` 决策
- 分析竞争、利润、广告、库存、合规和执行风险
- 输出市场筛选 memo、产品选择 memo、Launch 计划、利润修复计划、库存风险复盘和清货/继续决策

## Agent 入口

如果你想直接使用“产品 PM 工作流 Agent”，可以从这里开始：

```text
agents/product-manager-workflow-agent/AGENT.md
```

这个 Agent 会围绕核心 skill 自动判断问题类型，例如市场筛选、产品选择、竞品应对、上线规划、利润修复、增长复盘、库存风险或止损决策，并输出结论、证据、假设、风险、下一步验证动作和指标门槛。

## 典型使用方式

安装后，在 Codex 中这样提问：

```text
Use $amazon-product-manager to evaluate whether I should enter the coffee capsule holder market on Amazon US.

My constraints:
- Small brand
- Limited launch budget
- Can source bamboo, ceramic, or light metal products
- Target price: $15-$35

Output:
- Enter Market / Watch Market / Avoid Market decision
- First product wedge
- Evidence needed
- Main risks
- 7-day validation plan
```

你也可以用中文：

```text
使用 $amazon-product-manager 帮我判断 Amazon US 的 coffee capsule holder 市场是否值得进入。

我的约束：
- 小品牌
- 首批预算有限
- 可做竹木、陶瓷或轻金属材质
- 目标售价 $15-$35

请输出：
- Enter Market / Watch Market / Avoid Market 决策
- 最适合的小切口
- 还缺什么证据
- 主要风险
- 未来 7 天验证计划
```

## 安装方法

把 skill 文件夹复制到你的 Codex skills 目录。

Windows PowerShell:

```powershell
$src = ".\skills\amazon-product-manager"
$dst = "$env:USERPROFILE\.codex\skills\amazon-product-manager"
New-Item -ItemType Directory -Force -Path (Split-Path $dst) | Out-Null
Copy-Item -Recurse -Force $src $dst
```

macOS / Linux:

```bash
mkdir -p ~/.codex/skills
cp -R skills/amazon-product-manager ~/.codex/skills/amazon-product-manager
```

安装后重启 Codex。

## 输入数据建议

这个 skill 不自带私有数据。你可以自己提供：

- 关键词和搜索量
- ASIN 列表
- 竞品价格、评分、评论数
- Review 痛点摘要
- COGS、FBA 费用、广告数据
- 库存、退货率、毛利率
- 你的预算、团队能力、供应链约束

数据越完整，决策越可靠；数据不完整时，skill 会把假设和缺口写出来。

## 输出风格

它会尽量先给结论，再给证据：

```text
Decision: Test First

Why:
- Demand signal is plausible but keyword depth is still unclear.
- Review barrier is moderate.
- Margin depends on whether landed cost can stay below target.
- First batch should be small because PPC tolerance is limited.

Next actions:
1. Validate top 20 ASIN price/review/rating distribution.
2. Estimate COGS + FBA + referral fee.
3. Build keyword map and break-even ACoS.
```

## 隐私提醒

不要把这些内容提交到公开仓库：

- `.env` 文件
- 账号密码、cookie、浏览器 session
- 付费工具导出的原始数据
- 客户订单、广告后台、供应商报价
- 未脱敏的截图、Excel、JSON 原始数据

## 当前状态

这是早期版本。后续计划会继续补：

- 中文案例
- 市场筛选模板
- 利润修复 checklist
- QYPM 6-7 / 6-8 工作流提炼
- 更多脱敏示例

欢迎提 issue 或建议。

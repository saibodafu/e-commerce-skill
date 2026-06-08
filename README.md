# e-commerce-skills｜电商详情页 Skill

在 Claude Code、Codex、WorkBuddy 等支持 skills 的工具中运行：

```text
/install-skill saibodafu/e-commerce-skill/ecommerce-content-wireframe
/install-skill saibodafu/e-commerce-skill/ecommerce-detail-page-visual-design
```

这是一个用于电商详情页策划、内容线框稿和逐屏视觉设计的 skill 包。

当前可用能力：

- `ecommerce-content-wireframe`：从产品信息出发，梳理详情页内容结构、详情页文案，并生成可运行的手机长图 HTML 黑白线框稿。
- `ecommerce-detail-page-visual-design`：在已有详情页文案、HTML 图、原型图、产品图或包装图的基础上，逐屏判断信息任务和视觉表达，推荐统一视觉风格，一屏一屏生成并确认，最后拼接成 750px 详情页长图。

## 当前 Skill

### ecommerce-content-wireframe

电商详情页内容黑白线框稿。

当你想梳理一个商品的电商详情页内容时使用。skill 会先要求你补充产品名、产品定位、目标人群、核心场景和核心卖点，再一步步生成详情页内容。

第一阶段：先收集精准信息

用户先填写完整产品信息表。如果暂时不确定某一项，可以写“待定”，但产品名、目标人群、核心场景和核心卖点建议尽量具体。

第二阶段：再进入共创

产品信息确认后，skill 按固定顺序逐层推进：

1. 核心价值承诺层
2. 痛点锚定层
3. 卖点强化层
4. 使用场景层
5. 产品身份卡
6. 决策收口层

最终会先整理成完整的详情页内容文档，再生成可直接运行的 HTML 黑白线框稿。

### ecommerce-detail-page-visual-design

电商详情页逐屏视觉设计与长图拼接。

当你已经有详情页文案、HTML 图、原型图、产品图或品牌包装图，希望进入视觉设计阶段时使用。skill 会按固定顺序推进：

1. 逐屏分析每一屏的信息任务
2. 判断适合的视觉表达类型
3. 梳理核心视觉元素和不允许出现的风险点
4. 推荐 3 个统一视觉风格方向
5. 按顺序一屏一屏生成详情页设计
6. 每一屏修改和确认后再进入下一屏
7. 最后纵向拼接成 750px 长图，并检查漏屏、错序、重复、文字裁切和产品裁切

这个 skill 会保留“假如你是一个电商详情页设计师……”这类可复制执行提示词，但不会把它作为 skill 的开始话术。

## 示例输入

```text
使用 ecommerce-content-wireframe，帮我梳理一款儿童电解质水的详情页内容。

产品名：小K水
产品定位：儿童日常补水与电解质补充饮品
目标人群：3-12岁儿童家长
核心卖点：低糖、好喝、补充电解质、儿童友好
```

```text
使用 ecommerce-detail-page-visual-design，我已经有详情页文案、原型图和产品图，帮我逐屏分析视觉表达，再按顺序一屏一屏生成，最后拼接成 750px 长图。
```

## 也可以这样说

```text
帮我梳理一个新品的电商详情页内容。
```

```text
用 ecommerce-content-wireframe，帮我基于完整产品信息生成详情页黑白线框稿。
```

```text
我有一个猫粮产品，帮我先整理详情页内容结构。
```

```text
我有详情页 HTML 图和包装图，帮我判断每一屏适合怎么设计。
```

```text
帮我把确认好的单屏详情页按顺序拼成长图，宽度 750px。
```

## 输出特点

- 先收集精准产品信息，再生成详情页内容
- 每一步都给多个选择，并指引用户选择、融合或补充信息
- 关键字段不足时先补齐，非关键细节不足时再做轻量假设并明确标注
- 不编造平台规则、销量、转化率、认证、竞品数据或客户案例
- 输出可以交给运营、内容、设计或商品团队继续执行
- 视觉设计流程中默认先分析、再定风格、再逐屏生成和确认
- 长图拼接后必须检查漏屏、错序、重复、文字裁切和产品裁切

## 项目结构

```text
.
├── AGENTS.md
├── commands/
│   └── ecommerce.md
├── skills/
│   ├── ecommerce-content-wireframe/
│   │   └── SKILL.md
│   └── ecommerce-detail-page-visual-design/
│       └── SKILL.md
├── .claude-plugin/
└── .codex-plugin/
```

## 赛博大福

欢迎关注公众号“赛博大福”。

用 AI 把营销重干一遍。

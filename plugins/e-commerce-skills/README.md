# e-commerce-skills｜电商详情页内容 Skill

这是一个用于梳理电商商品详情页内容的 skill。

当前可用能力是：`ecommerce-content-wireframe`。它可以根据少量商品信息，先快速生成一版可运行的手机长图 HTML 黑白线框稿，让用户先看到详情页内容效果；如果初稿不够准，再按照固定步骤逐层精修详情页内容。

## 安装

### Claude Code 安装

```text
/plugin marketplace add saibodafu/e-commerce-skills
/plugin install e-commerce-skills
```

安装后可用 `/skills` 检查是否加载成功。

### Codex 使用

在 Codex 中打开本仓库目录，即可读取 `AGENTS.md`、`commands/` 和 `skills/` 中的工作流说明。

## 当前 Skill

### ecommerce-content-wireframe

电商详情页内容黑白线框稿。

当你想梳理一个商品的电商详情页内容时使用。你可以先随便输入一点产品信息，skill 会直接生成一版可运行的手机长图 HTML 黑白线框稿。

第一阶段：先给结果

用户只要输入少量商品信息，甚至只写一句话、几个关键词或不完整字段，也会先生成详情页 HTML 初稿。

第二阶段：再进入共创

初稿生成后，用户补充更完整的产品信息表。然后 skill 按固定顺序逐层精修：

1. 核心价值承诺层
2. 痛点锚定层
3. 卖点强化层
4. 使用场景层
5. 产品身份卡
6. 决策收口层

最终会先整理成完整的详情页内容文档，再生成可直接运行的 HTML 黑白线框稿。

## 示例输入

```text
使用 ecommerce-content-wireframe，帮我梳理一款儿童电解质水的详情页内容。

产品名：小K水
目标人群：3-12岁儿童家长
核心场景：运动后、出汗后、天气热的时候
核心卖点：
1. 低糖
2. 好喝
3. 补充电解质
4. 儿童友好
```

## 也可以这样说

```text
帮我梳理一个新品的电商详情页内容。
```

```text
用 ecommerce-content-wireframe，给我生成一版详情页黑白线框稿。
```

```text
我有一个猫粮产品，先帮我出一版详情页内容 HTML 初稿。
```

## 输出特点

- 先生成可见的详情页效果，再逐步精修
- 少信息也能生成初稿
- 信息不足时做轻量假设，并明确标注
- 不编造平台规则、销量、转化率、认证、竞品数据或客户案例
- 输出可以交给运营、内容、设计或商品团队继续执行

## 项目结构

```text
.
├── AGENTS.md
├── commands/
│   └── ecommerce.md
├── skills/
│   └── ecommerce-content-wireframe/
│       └── SKILL.md
├── .claude-plugin/
└── .codex-plugin/
```

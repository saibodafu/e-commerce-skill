# e-commerce-skills — Claude Code / Codex 电商技能包

> 把商品策略、卖点提炼、详情页策划、货架内容、直播脚本、活动复盘等电商工作流沉淀成可复用的 Agent skills。

---

## 安装

### Claude Code 快速安装

在 Claude Code 中添加这个 GitHub 仓库作为插件市场来源：

```text
/plugin marketplace add saibodafu/e-commerce-skills
```

然后安装插件：

```text
/plugin install e-commerce-skills
```

重启 Claude Code 后，用 `/skills` 检查是否已加载电商技能。

### Claude Code 手动安装

```bash
git clone https://github.com/saibodafu/e-commerce-skills.git
cc --plugin-dir ./e-commerce-skills
```

也可以使用 SSH：

```bash
git clone git@github.com:saibodafu/e-commerce-skills.git
cc --plugin-dir ./e-commerce-skills
```

### Codex 使用

在 Codex 中打开本仓库目录即可使用：

```bash
git clone https://github.com/saibodafu/e-commerce-skills.git
cd e-commerce-skills
```

Codex 会读取 `AGENTS.md`、`.codex-plugin/plugin.json`、`commands/` 和 `skills/` 中的说明。后续新增具体 skill 后，可以直接说：

```text
使用 e-commerce-skills，帮我把这个商品需求整理成可执行的电商工作流。
```

---

## 使用方式

### Claude Code 命令

```text
/ecommerce <workflow> [context]
```

当前可用 workflow：

- `ecommerce-content-wireframe`：电商详情页内容黑白线框稿。用户先用少量信息一键梳理详情页内容并生成可运行 HTML 初稿，再按顺序逐层精修核心价值承诺、痛点锚定、卖点强化、使用场景、产品身份卡和决策收口。

新增具体 workflow 后，应同步更新：

- `skills/<skill-name>/SKILL.md`
- `commands/ecommerce.md`
- `README.md`
- `README.zh.md`
- `.codex-plugin/plugin.json`
- `.claude-plugin/plugin.json`
- `.claude-plugin/marketplace.json`

---

## 计划中的 Skills

可按业务优先级逐步补齐：

- 商品卖点提炼
- 货架标题与搜索词优化
- 直播带货脚本
- 达人种草 brief
- 大促活动策略
- 店铺或活动复盘

---

## GitHub 仓库

- HTTPS：[https://github.com/saibodafu/e-commerce-skills](https://github.com/saibodafu/e-commerce-skills)
- SSH：`git@github.com:saibodafu/e-commerce-skills.git`

---

## 项目结构

```text
.
├── .claude-plugin/
│   ├── marketplace.json
│   └── plugin.json
├── .codex-plugin/
│   └── plugin.json
├── commands/
│   └── ecommerce.md
└── skills/
    └── ecommerce-content-wireframe/
        └── SKILL.md
```

---

## 新增 Skill

1. 创建 `skills/<skill-name>/SKILL.md`。
2. 如果 workflow 需要复用脚本，把脚本放在 `skills/<skill-name>/scripts/`。
3. 如果需要命令入口，在 `commands/` 下新增或更新 markdown 命令文件。
4. 如果市场定位、关键词或产品描述变化，同步更新 `.claude-plugin/marketplace.json` 和 `.codex-plugin/plugin.json`。

新增 skill 时，应先澄清场景、目标用户、输入、输出、边界、触发条件和质量标准；确认方向后再写入 skill 文件。

---

## 说明

- `.claude-plugin` 用于 Claude Code 插件和 marketplace 风格描述。
- `.codex-plugin` 用于 Codex 插件清单兼容。
- `commands/ecommerce.md` 提供 `/ecommerce` 命令入口。
- `skills/` 是每个电商 workflow 的主说明。
- 输出应能直接交给商品、运营、内容、直播、投放、设计、客服或销售团队使用，不编造平台规则、GMV、转化率、行业 benchmark 或未核验的竞品数据。

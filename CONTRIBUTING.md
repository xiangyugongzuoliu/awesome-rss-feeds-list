# Contributing to awesome-rss-feeds

感谢你想为这个仓库做贡献。在你提 Issue 或 PR 之前，先了解我们的工作机制。

## 这个仓库不收 PR 修改 OPML 文件

**OPML 和 LIST.md 都是自动生成的产物**，由翔宇内部工具 `xiangyu-search-rss-cli` 每月重跑生成。直接 PR 修改这些文件会被下次重跑覆盖。

如果你想加源、报死链或建议分类，请走 **Issue 流程**。

## Issue 流程

### 1. 提一个新源

模板：[new-source.yml](.github/ISSUE_TEMPLATE/new-source.yml)

填四个字段：
- **RSS 源 URL**（必填）—— 必须是有效的 RSS / Atom feed URL
- **网站主页 URL** —— 该源所属网站
- **推荐分类** —— 从 7 类中选一：ai-and-ml / tech-and-startups / chinese-blogs / dev-and-opensource / design-and-product / news-and-finance / rss-tools
- **简短理由** —— 为什么值得收录（≤200 字）

### 2. 报告一个死链

模板：[dead-link.yml](.github/ISSUE_TEMPLATE/dead-link.yml)

填两个字段：
- **死链 URL**
- **错误状态**（404 / 超时 / 内容已变 / 域名失效）

### 3. 建议新分类

模板：[category-suggest.yml](.github/ISSUE_TEMPLATE/category-suggest.yml)

我们对新增一级分类非常谨慎——目前 7 类是在覆盖度和清晰度之间取的平衡，新增分类需要满足「至少 30 个源能填充 + 与现有 7 类边界清晰」。

## 我们的入库流程

每月 1 号左右翔宇会做一次月度审计：

1. 把上月所有 Issue 集中过一遍
2. 跑工具的 `crawl` 重新拉所有上游
3. 把社区提的源加入 `manual-add.opml` 一并入库
4. `validate` 三道闸验证
5. `categorize` 分类（人工 review）
6. `audit` 死链处理
7. `diff` 生成 CHANGELOG
8. `publish` 推送

所以你提的源不会立刻入库，会延迟 1-30 天，请耐心等。

## 决策原则

| 维度 | 标准 |
|---|---|
| 收录优先级 | 开源 / 免费 > 付费 |
| 内容质量 | 每周至少一次更新 + 至少 50% 全文 RSS（摘要型源会标注但不优先） |
| 多元性 | 同一作者 / 媒体最多 1-2 个源（避免单一来源垄断分类） |
| 政治中立 | 极端立场内容不收录 |
| 重复性 | 与 awesome-blogCN-feeds / awesome-tech-rss 等上游重复时不重复收录 |

## License

提交即代表你同意你的贡献以 CC0 公有领域协议进入本仓库。

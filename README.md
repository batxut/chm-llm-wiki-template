# LLM Wiki 模板

一个基于 **Obsidian + Claude Code（LLM Agent）** 的结构化知识库框架。

## 关于

本项目源自 [Andrej Karpathy 的 LLM Wiki 理念](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)——将知识库视为一个由 LLM 持续维护的编译产物，而非每次查询时重新检索碎片的 RAG 系统。

**核心理念：** 你负责筛选来源和提问，LLM 负责归纳整理、交叉引用和增量更新。知识被编译一次后持续维护，而非每次查询时重新推导。

该模板提供了完整的规范文件（`CLAUDE.md`）和目录结构，将 Obsidian 仓库转化为一个 LLM 驱动的 Wiki 系统。

## 快速开始

1. **克隆或 fork** 本仓库
2. **在 Obsidian 中打开** 作为仓库
3. **在此目录中配置 Claude Code**（或其他 LLM Agent）
4. 按照 `CLAUDE.md` 中的工作流操作：
   - **Ingest（消化）** — 将来源放入 `原始资料/`，告诉 LLM 处理
   - **Query（查询）** — 对知识库提问
   - **Lint（检查）** — 定期对知识库做健康检查

## 前置条件

- [Obsidian](https://obsidian.md)
- [Claude Code](https://docs.anthropic.com/en/docs/claude-code/overview) 或其他 LLM Agent

## 推荐插件

| 插件 | 用途 |
|------|------|
| Obsidian Git | 自动提交和同步 |
| Local Images Plus | 将外部图片下载到本地 |
| Marp Slides | 从知识库内容生成演示文稿 |
| Dataview | 基于 frontmatter 的动态查询 |

## 目录结构

```
CLAUDE.md              # 规范层 — 定义 LLM 如何维护知识库
原始资料/              # 源文档存放处，LLM 只读不写，你可随时手工增删改
知识库/                # Wiki 内容（LLM 全权维护）
├── 来源/              # 来源摘要页面
├── 概念/              # 概念页面
├── 实体/              # 实体页面（人物/组织/产品）
├── 对比/              # 对比/综合分析页面
├── 媒体/              # 从原始资料复制过来的图片等
├── index.md           # 内容索引（按类别组织）
├── 领域索引.md        # 按领域归类的 MOC 页面
└── log.md             # 操作日志（按时间顺序）
```

## 许可

MIT

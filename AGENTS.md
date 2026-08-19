# AGENTS.md — Repository entry point

This repository is a container for vibe-coding templates. The template content lives in [`.template/`](.template/AGENTS.md), a self-contained project with its own standing orders, doc gates, bilingual-pairing contract, and agent-note discipline.

- **Open agent sessions inside `.template/`** to load the full rules (`.template/AGENTS.md`) and run its gates (`pnpm run doc-sync`).
- Files at this root level are container-level only: this entry document and the Git metadata ([`.gitattributes`](.gitattributes), [`.gitignore`](.gitignore)). They are not part of the template's gate scope.
- To start a new project, copy `.template/` into a new directory, run `git init` and `pnpm install`, then `pnpm run doc-sync`.

# AGENTS.md — 仓库入口

本仓库是 vibe-coding 模板的容器。模板内容位于 [`.template/`](.template/AGENTS.md)，是一个自包含的项目，拥有自己的常设规则、文档门禁、双语配对契约与 Agent Note 纪律。

- **请在 `.template/` 目录内打开 agent 会话**，以加载完整规则（`.template/AGENTS.md`）并运行其门禁（`pnpm run doc-sync`）。
- 根目录仅保留容器级文件：本文档与 Git 元数据（[`.gitattributes`](.gitattributes)、[`.gitignore`](.gitignore)），不参与模板门禁范围。
- 新建项目时，将 `.template/` 复制到新目录，执行 `git init` 与 `pnpm install`，再运行 `pnpm run doc-sync`。

# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 仓库用途

该仓库当前仅包含一个最小化的 `README.md`，用于演示/验证“单一工作区同时同步到两个 git 远端（GitHub + Gitea）”的配置方式。

## 远端与同步

已配置 3 个 remote：

- `github`: `git@github.com:kaelen-hou/double-upstream.git`
- `gitea`: `git@gitea.deeplang.tech:houjialin/double-upstream.git`
- `all`: 用于“一次 push 同步两个远端”（通过 `pushurl` 绑定 GitHub 与 Gitea）

常用命令：

```bash
# 查看远端
git remote -v

# 分别推送
git push github main
git push gitea main

# 同时推送到两个远端
git push all main
```

## 代码结构（当前）

- `README.md`：仓库说明（目前内容很少）
- `CLAUDE.md`：本文件
- `.claude/settings.local.json`：本地 Claude Code 权限设置（允许 `git add` / `git commit`）

## 构建 / 测试 / Lint

当前仓库没有应用代码与构建系统（无 `package.json`/`pyproject.toml`/`go.mod` 等），因此暂无 build/test/lint 命令可记录。若后续引入具体技术栈，请在此补充对应命令。

---
name: marp-theme-builder
description: Marp 开发工作流与自动化构建配置管理技能。涵盖 SCSS 预编译构建脚本、Git hook（提交前检查）、以及接入 GitHub Actions 等 CI/CD 的持续集成配置。适用于“帮我配一下主题编译自动化”等长期项目结构诉求。
---

# Marp Skills Pro - 自动化工业流水线 (Theme Builder)

本技能是为了专业工程师构建可长久维护的 Marp 主题工程架构设计的构建库。

## 触发场景

- “帮我创建一个可以自动编译主题的 Makefile 工程结构”
- “如何将这套主题加上持续集成环境（CI/CD）？”
- “在 Git 提交时帮我做语法检查和自动转化 PDF 输出”

## 自动化工程工作流

1. **结构初始化**：建立带有规范的开发工程（如配置 `.gitignore`, `package.json`）。
2. **建立工程脚本**：写 Makefile / npm scripts 定义快速热更新与编译指令（如 `pnpm run watch`）。
3. **CI / CD 配置**：编写 GitHub Actions 的 Workflow 或 Git hook (pre-commit) 做视觉变更校验。
4. **测试**：集成基于图例差异检查的测试用例。

## 联动的技能节点

- **marp-theme-creator**: 用于创建在流水线里需要被构建的 CSS/SCSS 源文件。

## 工作流流转全貌

```
SCSS 源头 ──(Sass)──> 预编译 CSS ──(Marp CLI)──> HTML / PDF / PNG
                         │
                    入库 (Git Commit)
                         │
                 拦截层 (pre-commit hook) -> 自动执行 lint / format
                         │
                 云端构建 (GitHub Actions CI) -> 图形差异检测与自动化部署发布
```

$ARGUMENTS

# AI Marp Skills Pro (中文增强版)

专门为 Claude Code（及同类具备加载外挂技能的 AI Agent）设计的定制化**高阶 Marp 幻灯片**设计技能集。

本库不但包含完整的 Marp 知识体系，还融入了**高级网格排版系统 (Grid)**、**玻璃拟物化 (Glassmorphism)** 以及深层 CSS 预设解决方案，使 AI 能为你生成极具现代感、商业路演级的演示文稿。

## 🌟 增强版核心特性

1. **中文母语级支持**：全面重构提示词，更符合中文用户的指令习惯。
2. **Premium 级设计思维**：默认推荐与输出更高级的视觉样式，抛弃原生粗糙排版。
3. **Glassmorphism 组件**：自带对 `.glass` 类支持的 CSS 和排版结构指引。
4. **多维度问题修复**：不仅修复了原生 BUG 输出，并添加了基于网格布局等高级解法。

## 🪄 技能列表

| 技能组件 | 功能说明 |
|----------|------|
| [marp-knowledge](marp-knowledge/) | Marp 包含最新 CSS 解决方案的综合知识大脑（其他技能引用的基石） |
| [marp-markdown](marp-markdown/) | 协助你编写支持高级排版（如双列网格、卡片）的 Markdown 幻灯片 |
| [marp-visual-fix](marp-visual-fix/) | 处理文字溢出、布局破碎、图片变形等各种棘手的视觉与排版问题 |
| [marp-export](marp-export/) | 一键导出 PDF/PNG/PPTX/HTML |
| [marp-theme-creator](marp-theme-creator/) | 引导 AI 使用预置或全新的 SCSS 变量为你构建高端定制主题 |
| [marp-theme-builder](marp-theme-builder/) | 为开发团队配置和搭建主题热更新与编译环境的流水线 |

## 🏗️ 依赖与结构解析

```
                    marp-knowledge (核心知识库/增强设计指南)
                          │
          ┌───────────────┼───────────────┐
          │               │               │
          ▼               ▼               ▼
    marp-markdown   marp-visual-fix   marp-theme-creator
          │               │               │
          │               │               │
          ▼               ▼               ▼
    (输出MD/排版)  (修复溢出/高阶版式)   (输出SCSS/高定CSS)
          │               │               │
          └───────────────┼───────────────┘
                          ▼
                     marp-export & builder (最终打包出图)
```

## 🚀 安装与加载

将本目录作为自定义 Skill 指向你的 Claude Code 或同等能力的 AI Agent 系统。
使用时可直接下达类似于：“帮我写一个工作汇报的推介，带有玻璃态网格排版，用深色背景，直接生成 PDF。”的指令。

## 📄 授权协议

MIT License

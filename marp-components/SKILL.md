---
name: marp-components
description: 专门负责提供高级版图文排版组件片段（UI Snippets）的技能。通过利用 HTML 结合自定义 CSS（如 .grid 或 .glass），为文本和数据提供引人注目的商业级图表、时间轴、四宫格等排版框架。当用户需要“高级布局”、“图文并排”、“产品特性卡片”或“比较页面”时调用。
---

# Marp Skills Pro - 高阶排版构件库 (Component Library)

这是一套帮助你在 Markdown 幻灯片中插入复杂排版结构组件代码的超级预设库。

## 触发场景

- “第二页太枯燥了，有没有办法做一个四宫格的产品优势介绍？”
- “帮我排版一个时间轴（Timeline）用于展现项目计划”
- “这里有三个方案，帮我做一个对比表格，但是要好看，可以用卡片形式吗？”
- “我想要一个纯数据展示的 KPI 数据面板，数字很大那种！”

## 核心可用组件 (Snippets)

你在构思幻灯片时，只要遇到上述场景，便可直接向用户注入以下组件源码：

### 1. 黄金双列架构 (.grid & .glass)
非常适合“左图右文”或者“左功能右配图”。
```html
<div class="grid">
  <div>
    <h3>文本核心</h3>
    <p>解释说明段落位置...</p>
  </div>
  <div class="glass">
    <!-- 这里放置图片、代码或者作为视觉重心的高亮数据 -->
  </div>
</div>
```

### 2. 现代多列卡片陈列 (.cards)
用于展现多个并行的要素。必须配合 `<style>` 中的 `display: grid; grid-template-columns: repeat(3, 1fr);` 等来使用。
```html
<div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 1em;">
  <div class="glass" style="text-align: center;">
    <h1>⚡️ 300%</h1>
    <p>性能提升</p>
  </div>
  <div class="glass" style="text-align: center;">
    <h1>📱 100%</h1>
    <p>移动端适配</p>
  </div>
  <div class="glass" style="text-align: center;">
    <h1>🛡 24/7</h1>
    <p>技术支持保障</p>
  </div>
</div>
```

### 3. 时间线 / 大事记步进展现 (Timeline)
用于展示公司历程或项目规划排期。
```html
<div style="border-left: 4px solid var(--color-primary); padding-left: 20px; margin-left: 20px;">
  <h3 style="margin-top:0"><span class="tag">Q1 计划</span> 研发立项</h3>
  <p>启动底层重构工作，全面引入高频流转调度算法。</p>
  
  <h3><span class="tag">Q2 计划</span> Beta 测试</h3>
  <p>对种子企业客户开放并获取关键性能反馈日志。</p>
  
  <h3><span class="tag">Q3 计划</span> 正式商用上线</h3>
  <p>举行发布会，铺设多维市场渠道推广体系。</p>
</div>
```

### 4. 点宽全景大图配高亮字幕 (Hero Banner)
利用指令满铺背景，并将核心文字装入一个下移的透明玻璃罩内以突出科技感。
```markdown
![bg right:50% fit](https://images.unsplash.com/...)

<div class="glass" style="margin-top: 40%">
  <h3>沉浸式的客户体验</h3>
  <p>让受众第一眼就能感知到产品的震撼感和生命力。</p>
</div>
```

## 使用准则
- 永远保持排版的**呼吸感**！绝对不要在一页 PPT 中塞满超过四个卡片。
- 如需调整高度可加入 inline CSS，但优先推荐使用在主题 CSS 里已定义好的 className（如 `glass`, `grid`, `tag`）。
- 这些组件同样支持深色模式。确保 `<!--_class: invert-->` 应用时无需大量修改内联颜色（所以组件应该尽量去用透明度配合继承系统颜色 `var(--color-...)`）。

$ARGUMENTS

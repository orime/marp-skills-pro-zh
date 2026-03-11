---
name: marp-export
description: 强大的多介质成品交付功能体系。支持从极速的热编译预览转化为最终的 PDF 汇报文档、高分辨率 PNG 画像分享与 HTML 在线长文档输出引擎指引。用户说“帮我导出一个 PDF 格式的文件”即可触发。
argument-hint: "<Markdown文件路径> [输出格式: pdf|png|pptx|html]"
---

# Marp Skills Pro - 全栈矩阵输出枢纽 (Marp Export)

将优美的 Markdown 手稿直接翻译转换为用于分发和演示的高清文件的指令集与帮助指南。

## 触发场景

- “把做好的这一页转化为 PDF 给我看看”
- “全部导出为独立的高清演示图片”
- “领导要改细节，帮我出一个 PPTX 版给他们”
- “编译为一个可以左右切换的独立 HTML 网页”

## 核心交付形式矩阵

| 输出形态 | 文件尾缀 | 交付环境建议 |
|------|--------|------|
| **PDF** | `.pdf` | 商务邮件投递、打印归档（**最稳定/最推荐**） |
| **PNG** | `.png` | 新媒体推文、SNS传播预热、排版图解查验 |
| **PPTX** | `.pptx` | 提供给非技术向协作者修改原始文字（*存在些许组件格式受限可能*） |
| **HTML** | `.html` | 自托管服务器展示、无需任何播放器即可在任意客户端浏览器播放 |

## 标准化的交付执行命令推荐

通过预设或执行底层脚本，为用户直接调用输出形态：

```bash
# 职场推介：标准的 PDF 封装
marp slide.md -o slide.pdf

# 自定义主题的热映射导出：套用我们的高级主题
marp slide.md --theme ./theme.css -o slide.pdf

# 网页级交互部署：支持视频嵌入与动画翻页的单页面 HTML 
marp slide.md --html -o out.html

# 获取多张连续静态图（适合 Xiaohongshu/微博发送）
marp slide.md -o slide.png
```

## 导出阶段注意事项
- 若排版包含外置远程高分辨率图片或视频，请提醒用户使用 `--allow-local-files` 避免加载失败。
- 如果导出存在部分溢出等特殊排版降级，请联动 **marp-visual-fix** 进行 CSS 手术微调或分页。

$ARGUMENTS

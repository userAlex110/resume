# 王梓晨 · 个人简历

> 机器人工程专业 | 嵌入式 / 机器人开发实习生

基于纯静态 HTML/CSS 的单页简历网站，适配 Web 浏览与 A4 PDF 打印输出。

## 技术栈

- HTML5 语义化结构
- CSS3 自定义属性（CSS Variables）
- Font Awesome 6 图标库
- 响应式布局（桌面双栏 / 移动端单栏）
- `@media print` 打印优化

## 项目结构

```
.
├── index.html      # 简历主体（HTML 结构 + 行内打印样式）
├── style.css       # 全局样式、响应式布局、打印媒体查询
├── favicon.png     # 网站图标
└── README.md
```

## 本地预览

直接用浏览器打开 `index.html`，或使用任意静态文件服务：

```bash
# Python
python -m http.server 8080

# VS Code Live Server 插件
# 右键 index.html → Open with Live Server
```

## 导出 PDF

1. 浏览器打开 `index.html`
2. `Ctrl+P`（Mac: `Cmd+P`）
3. 目标打印机选择「另存为 PDF」
4. 确保勾选「背景图形」以保证颜色正常渲染

## 设计说明

| 项目 | 说明 |
|------|------|
| 配色 | `#2c3e50`（标题）/ `#3498db`（强调）/ `#f8f9fa`（标签底色） |
| 布局 | 侧边栏 32% + 主内容 68%，打印时自动适配 A4 |
| 字体 | 系统字体栈，优先 Helvetica Neue，中文回退至苹方/微软雅黑 |
| 图标 | Font Awesome 6.4.0 CDN 加载 |

## 许可证

MIT

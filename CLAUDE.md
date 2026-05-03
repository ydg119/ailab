# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

---

# 项目概述

这是一个静态网站项目，包含四个独立的 HTML 页面，展示了交互式应用和教程内容。

## 项目结构

```
.
├── index.html                                  # 3D 魔方交互应用
├── codex_workflow_tutorial.html               # Codex 工作流程教程
├── frontend_10_years_frontend_tutorial.html   # 前端框架发展教程
└── frontend_tech_roadmap.html                 # 前端技术栈发展路径图 (2016-2026)
```

## 页面说明

### 1. index.html - 3D 魔方应用
- **技术栈**: Three.js (v0.160.0)
- **功能特性**:
  - 完整的 3D 魔方交互（拖拽旋转切片）
  - 粒子系统和动态光照效果
  - 打乱功能（Scramble）
  - 快捷键支持（Shift + G 重置视角）
  - 响应式设计，支持触摸操作
- **核心实现**:
  - 使用 Three.js 渲染 3x3x3 魔方
  - 自定义着色器实现粒子效果
  - 动画队列系统处理旋转操作
  - Raycasting 实现精确的交互检测

### 2. codex_workflow_tutorial.html
- **内容**: 工作中正确使用 Codex 的教程
- **设计风格**: 现代深色主题，渐变背景，玻璃态效果

### 3. frontend_10_years_frontend_tutorial.html
- **内容**: 最近10年前端框架、架构与组件模块教程
- **设计风格**: 与 Codex 教程类似的现代 UI 设计

### 4. frontend_tech_roadmap.html
- **内容**: 前端技术栈发展路径图 (2016-2026)
- **设计风格**: 现代深色主题，与其他教程页面保持一致

## 技术特点

- **纯静态**: 无需构建工具或依赖管理
- **CDN 依赖**: Three.js 通过 unpkg.com 加载
- **现代 CSS**: 使用 CSS 变量、渐变、backdrop-filter 等特性
- **响应式**: 所有页面支持移动端访问

## 开发指南

### 本地预览
直接在浏览器中打开任意 HTML 文件即可预览。

### 修改建议
- **魔方应用**: 主要逻辑在 index.html 的 `<script type="module">` 标签内
- **教程页面**: 内容和样式都在单个 HTML 文件中，便于独立维护

### 部署
可以直接部署到任何静态托管服务：
- GitHub Pages
- Netlify
- Vercel
- 或任何支持静态文件的服务器

## 注意事项

1. **Three.js 版本**: 当前使用 v0.160.0，如需升级请测试兼容性
2. **浏览器兼容性**: 需要支持 ES6 模块和 WebGL 的现代浏览器
3. **网络依赖**: Three.js 从 CDN 加载，需要网络连接（首次访问）

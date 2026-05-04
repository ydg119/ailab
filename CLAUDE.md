# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

---

# 项目概述

这是一个 AI 生成的静态网站项目集合，包含 9 个独立的 HTML 页面，展示了交互式应用、动画效果和教程内容。所有文件均为自包含的单文件应用（HTML + CSS + JS 都在一个文件中）。

## 项目结构

```
.
├── index.html                                  # 3D 魔方交互应用（Three.js）
├── aquarium.html                               # 水族馆动画
├── rocket_launch.html                          # 火箭发射动画
├── storybook.html                              # 故事书交互页面
├── photography-portfolio.html                  # 摄影作品集展示
├── plugin_registry_gateway.html                # 插件注册网关界面
├── codex_workflow_tutorial.html               # Codex 工作流程教程
├── frontend_10_years_frontend_tutorial.html   # 前端框架发展教程（最近10年）
└── frontend_tech_roadmap.html                 # 前端技术栈发展路径图 (2016-2026)
```

## 页面分类

### 交互式应用
- **index.html** - 3D 魔方应用
  - 技术栈: Three.js (v0.160.0) 从 unpkg.com CDN 加载
  - 核心功能: 3x3x3 魔方拖拽旋转、切片操作、打乱功能
  - 特效: 粒子系统（自定义着色器）、动态光照
  - 交互: Raycasting 实现精确点击检测、动画队列系统处理旋转
  - 快捷键: Shift + G 重置视角
  - 所有逻辑在 `<script type="module">` 标签内

- **aquarium.html** - 水族馆动画
- **rocket_launch.html** - 火箭发射动画  
- **storybook.html** - 故事书翻页效果
- **photography-portfolio.html** - 摄影作品展示
- **plugin_registry_gateway.html** - 插件注册界面

### 教程页面
所有教程页面使用统一的设计风格：现代深色主题、渐变背景、玻璃态效果（backdrop-filter）

- **codex_workflow_tutorial.html** - 工作中使用 Codex 的教程
- **frontend_10_years_frontend_tutorial.html** - 前端框架、架构与组件模块教程
- **frontend_tech_roadmap.html** - 前端技术栈发展路径图

## 架构特点

- **纯静态**: 无构建流程，无依赖管理，无 package.json
- **自包含文件**: 每个 HTML 文件包含所有 CSS 和 JavaScript，完全独立
- **外部依赖**: 仅 index.html 依赖 Three.js (v0.160.0)，通过 unpkg.com CDN 加载
- **现代浏览器特性**: ES6 模块、WebGL、CSS 变量、backdrop-filter
- **响应式设计**: 所有页面支持移动端和触摸操作

## 开发工作流

### 本地预览
直接用浏览器打开任意 HTML 文件，无需本地服务器。

### 修改代码
每个页面都是单文件应用：
- HTML 结构、CSS 样式、JavaScript 逻辑都在同一个文件中
- 修改后刷新浏览器即可看到效果
- index.html 的核心逻辑在 `<script type="module">` 标签内

### 部署
直接部署到静态托管服务（GitHub Pages / Netlify / Vercel）。

## 重要约束

1. **Three.js 版本锁定**: index.html 使用 v0.160.0，升级需测试兼容性
2. **首次加载需联网**: Three.js 从 CDN 加载
3. **浏览器要求**: 需支持 ES6 模块和 WebGL
4. **AI 生成内容**: 所有文件由 AI 生成，仅供学习研究使用

# ailab

一个静态网站项目集合，包含多个独立的交互式应用和教程页面。

## 项目结构

```
.
├── index.html                                  # 3D 魔方交互应用
├── aquarium.html                               # 水族馆动画效果
├── rocket_launch.html                          # 火箭发射动画
├── storybook.html                              # 故事书交互页面
├── photography-portfolio.html                  # 摄影作品集展示
├── plugin_registry_gateway.html                # 插件注册网关界面
├── codex_workflow_tutorial.html               # Codex 工作流程教程
├── frontend_10_years_frontend_tutorial.html   # 前端框架发展教程
└── frontend_tech_roadmap.html                 # 前端技术栈发展路径图 (2016-2026)
```

## 页面说明

### 交互式应用

- **index.html** - 3D 魔方交互应用
  - 技术栈: Three.js (v0.160.0)
  - 功能: 完整的 3D 魔方交互、粒子系统、打乱功能、快捷键支持

- **aquarium.html** - 水族馆动画效果页面

- **rocket_launch.html** - 火箭发射动画页面

- **storybook.html** - 故事书交互页面

- **photography-portfolio.html** - 摄影作品集展示页面

- **plugin_registry_gateway.html** - 插件注册网关界面

### 教程页面

- **codex_workflow_tutorial.html** - 工作中正确使用 Codex 的教程
  - 现代深色主题，渐变背景，玻璃态效果

- **frontend_10_years_frontend_tutorial.html** - 最近10年前端框架、架构与组件模块教程

- **frontend_tech_roadmap.html** - 前端技术栈发展路径图 (2016-2026)

## 技术特点

- **纯静态**: 无需构建工具或依赖管理
- **CDN 依赖**: Three.js 通过 unpkg.com 加载
- **现代 CSS**: 使用 CSS 变量、渐变、backdrop-filter 等特性
- **响应式**: 所有页面支持移动端访问

## 本地预览

直接在浏览器中打开任意 HTML 文件即可预览。

## 部署

可以直接部署到任何静态托管服务：

- GitHub Pages
- Netlify
- Vercel
- 或任何支持静态文件的服务器

## 注意事项

1. **Three.js 版本**: 当前使用 v0.160.0，如需升级请测试兼容性
2. **浏览器兼容性**: 需要支持 ES6 模块和 WebGL 的现代浏览器
3. **网络依赖**: Three.js 从 CDN 加载，需要网络连接（首次访问）

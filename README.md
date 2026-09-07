# BioAgent OS · 产品介绍网站

[BioAgent OS](https://bioagent-new.7otech.com/) 的官方介绍站点 —— 面向生命科学研究的 AI 智能体操作系统。

## 技术栈

- **Vue 3** — 组合式 API + `<script setup>`
- **Vite 6** — 构建与开发服务器
- **Tailwind CSS 4** — 样式（通过 `@tailwindcss/vite` 插件接入）

## 快速开始

```bash
# 安装依赖
npm install

# 启动开发服务器（默认 http://localhost:5173）
npm run dev

# 构建生产产物（输出到 dist/）
npm run build

# 本地预览构建产物
npm run preview
```

## 页面结构

| 区块 | 组件 | 内容 |
|---|---|---|
| 导航栏 | `NavBar.vue` | 锚点导航 + 进入门户，移动端汉堡菜单 |
| Hero | `HeroSection.vue` | 主标语「可复现 · 可审计 · 可进化」+ 关键指标 |
| 六大模块 | `ModulesSection.vue` | 项目 / 会话 / 画布 / 报告 / 数据 / 技能 |
| 工作流 | `WorkflowSection.vue` | 从问题到报告的四步闭环 |
| 记忆与知识 | `MemorySection.vue` | 自进化记忆体系 + 编辑器示意 |
| 安全治理 | `GovernanceSection.vue` | 数据红线 / 信任档位 / 审计 / 执行环境 |
| CTA | `CtaSection.vue` | 引导进入门户 |
| 页脚 | `FooterSection.vue` | 版权信息 |

## 设计规范

- **主题**：暗色（科研密度定位）
- **语义色**：紫色 `accent`（AI 身份）· 蓝色 `run`（运行态）· 绿色 `done`（完成态）
- **自定义色板**：在 `src/style.css` 的 `@theme` 中定义（`ink` / `accent` / `run` / `done`）

## 目录说明

```
├── index.html          # 入口 HTML
├── vite.config.js      # Vite 配置（vue + tailwindcss 插件）
├── src/
│   ├── main.js         # 应用入口
│   ├── App.vue         # 页面组装
│   ├── style.css       # Tailwind 导入 + 主题定义
│   └── components/     # 各区块组件
└── dist/               # 构建产物（已 gitignore）
```

## 部署

`npm run build` 后，将 `dist/` 目录部署到任意静态托管服务即可。

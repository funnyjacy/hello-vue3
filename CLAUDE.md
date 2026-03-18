# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 常用命令

```bash
# 安装依赖
npm install

# 启动开发服务器（热重载）
npm run serve

# 生产环境构建
npm run build

# 代码检查与自动修复
npm run lint
```

## 技术栈

- **Vue 3**（Composition API / Options API 均可）
- **TypeScript**（strict 模式开启）
- **Vue Router 4**（History 模式，`@/router/index.ts`）
- **Vuex 4**（`@/store/index.ts`，目前状态为空，扩展时使用 modules 结构）
- **Less**（CSS 预处理器）
- **Vue CLI 5** 构建工具（基于 webpack）

## 项目结构

```
src/
├── main.ts          # 入口：createApp().use(store).use(router).mount('#app')
├── App.vue          # 根组件
├── router/index.ts  # 路由配置，AboutView 使用懒加载
├── store/index.ts   # Vuex store，使用 modules 扩展
├── views/           # 页面级组件（对应路由）
└── components/      # 可复用组件
```

路径别名 `@` 指向 `src/`。

## 代码风格

- Prettier：不加分号、单引号
- ESLint：`plugin:vue/vue3-essential` + `@vue/typescript/recommended`
- `console` / `debugger` 在生产环境触发警告，开发环境允许使用
